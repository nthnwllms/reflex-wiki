# Reflex's Netcode

Overview of Reflex Arena's networking, latency, interpolation, and how to configure it for competitive play.

(Replace this with technical information about the netcode and links to resources.)


## Where to aim with lag

The new Reflex netcode uses a combination of extrapolation and backwards reconciliation in attempt to keep what you're seeing consistent across clients and servers. This lag compensation has an upper limit of 80ms -- if you have more than an 80ms ping, you'll need to lead by ping - 80ms. I.e, if your ping is 100ms, you'll need to lead by 20ms. Our backwards reconciliation has the same limit -- if your enemy has a ping of over 80ms, they won't be able to shoot you from 500ms in the past. 


## How Reflex Arena's netcode works

Time(0): player shoots locally

Time(1): client sends packet to server saying he shot

Time(2): server receives packet saying player shot

Time(3): server steps player forward, including creating any projectiles player fired. The projectiles are fired at the time the player moved which is behind the current server time.

Time(4): gamestate is sent from server -> client

Time(5): client receives gamestate with new projectile in it. Projectile is displayed at the scene time.
Key points:

1. player is half-ping behind server (in best case) in time 3. So here your rocket will be swept forward by half ping on next server step

2. in time 5, rocket is actually extrapolated ahead so it's perfectly in sync with rest of scene

3. the 80ms cap will on scene extrapolation will cause more complicated issue here, but the cap is for the greater good :)

So ultimately, rockets will look to come out further in front of you. I believe quake doesn't do the extrapolation as hard as us, which is the cause, but I could be wrong, i'm more familiar with reflex code. 

## Technical Breakdown
In a [Reddit thread](https://web.archive.org/web/20241208004818/https://np.reddit.com/r/truegaming/comments/2ruqba/advances_in_fps_netcode/cnkhpyg/), Reflex's lead programmer explains how the netcode in Reflex works.

We both extrapolate and backwards reconciliate by half ping.
Explanation: (halfping is clients half ping) 

```
time N
1a. server has a position for all players
1b. server sends position of all players to clients in gamestate update
```
```
time N + halfping
2a. server steps time forward to time N + halfping, and records newplayers positions
2b. client receives gamestate informing it where players were at time N
2c. client draws frame at time N + halfping (this is extrapolating timeN -> time N + halfping)
2d. client presses fire.
2e. client sends fire event in packet.
```
```
time N + halfping * 2
3a. server receives clients fire event for time time N + halfping
3b. server rewinds time to KNOWN state (time N + halfping) which it didin 2a.
3c. server applies fire that client provided in 2e.
3d. server restores players positions to time time N + halfping*2.
```

as you can see:
- the extrapolation is done in 2c, by HALF ping, on the clients screen.(i.e. it's extrapolating time N -> time N + halfping)
- the backwards reconciliation done in 3b, to put the player at theright time for when the player did the fire. (i.e. it's rewinding fromtime N + halfping*2 -> time N + halfping)

Yes it's curious to note that you could either extrapolate twice as much to avoid the need for BR, or BR twice as far to remove the need for extrapolation. However that would double the error in extrapolation or double the time for "getting shot around a corner" (the known BR downside).

It's also important to notice that the BR state is 100% correct as it's server authored, yet the client extrapolation state is not necessarily correct (as it's extrapolated), but we're had good results thus far :) 