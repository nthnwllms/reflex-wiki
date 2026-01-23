# Console Commands

List of console commands, examples, and recommended settings for Reflex Arena.


## Reflex Arena - Console Commands											
### Contents
1. Reflex's Command Console
2. How to open the console
3. Command name completion
4. Check on default settings
5. Valid bindable `<key>` names

### Reflex's Command Console
Reflex Arena features a developer console, letting users change settings and bind keys using an extensive set of console commands.

### How to open the console
To open the console, run the game, then in game mode or editor mode (does not matter), hit the key to the left of the keyboard (left of 1 and under Esc), on the US keyboard that should be the ~-key on a German keyboard it is the ^-key.
Command name completion

Start typing the name of a command, and Reflex will suggest commands that begin with the typed letters, hit the Tab-key to auto-complete the command name. Hit Tab-key twice for a complete list of commands.
Check on default settings

To find out the current settings / parameters of a command, enter its name and hit Enter without any arguments. Note that some commands have no parameters attached.

### Example
cl_crosshair + Enter-key
will show the currently used crosshair style number seen in the HUD, and
cl_crosshair 0 + Enter-key
will turn off the crosshair altogether.
Valid bindable <key> names
The list of valid <key>s used by the bind commands are listed in Keylist.

== ASCII-formatted Command overview ==
This slightly outdated overview page is being kept for nostalgia reasons mostly. Allows a quick lookup of the commands though. (AEon)
See Alphabetical List of Reflex Console Commands for the latest updated information.

// Legend
<#>         Commands take a number as argument, range varies.
<0/1>       Command can only be turned on = 1, or off = 0.

```
+attack
+back
+crouch
+forward
+jump
+left
+right
+showscores
-attack
-back
-crouch
-forward
-jump
-left
-right
-showscores
+editorcameradrag
+editorfacemode
+editormultiselect
+editorprimary
+editorroll
+editortimelinedrag
+editorvertical
-editorcameradrag
-editorfacemode
-editormultiselect
-editorprimary
-editorroll
-editortimelinedrag
-editorvertical
addbind
bind
bindResetToDefaults
callvote
```


### Client Commands
```
cl_camera_freecam			//
cl_camera_next_player		//
cl_camera_player			//
cl_camera_prev_player		//
cl_color_enemy
cl_color_friend
cl_color_relative
cl_country				    // Set country flag
cl_error_correct_angles_speed
cl_error_correct_position_speed
cl_error_decay_angles
cl_error_decay_position
cl_events <0/1>			    // Toggle event effects
cl_gibs_expire_time <#>		// 10.0 default
cl_gibs_maxcount <#>		// 128 default, min value 1
cl_input_subframe <0/1>		// 0: input is processed per frame, 1: at 1kHz
```

### Matchmaking
```
cl_mm_include_bots
cl_mm_lobby
cl_mm_playlists
cl_mm_proving_grounds
cl_mm_regions
cl_mm_start
cl_mm_stop
cl_mm_turbo
```

### Player Customization
```
cl_playerarms
cl_playerboltrifle
cl_playerburstgun
cl_playerplayercolor1
cl_playerplayercolor2
cl_playerplayercolor3
cl_playergrenadelauncher
cl_playerhead
cl_playerplayerioncannon
cl_playerlegs
cl_playermelee
cl_playerplasmarifle
cl_playerrocketlauncher
cl_playershotgun
cl_playerstate				// switch to EDIT from game (see toggleeditor); bind mouse3
cl_playerteam
cl_playertorso
cl_predict_items
cl_ragdoll_expire_time
cl_replaymarker			    // Add a marker to the replay file, jump to markers while viewing a replay; bind m
cl_show_gun <0/1>			// toggle weapon model off/on;             bind h,j
cl_show_hud <0/1>			// toggle HUD off/on;                      bind u,i
cl_show_lagmeter <0/1>		//
cl_show_profiler <0/1>		//
cl_show_traffic <0/1>		//
cl_text_group				// Groups damage numbers of burst, shotgun, and ioncannon, 5 5 5 5 it comes up as 20
cl_text_time <#>			// How long damage numbers will stay on screen.
cl_weapon_bob <0/1>         // Enables/disables weapon bob while moving.
cl_weapon_kickback <0/1>    // Enables/disables weapon kickback while firing.
cl_weapon_offset_x <#>      // 5.0, weapon left/right offset.
cl_weapon_offset_y <#>      // -10.0, weapon vertical offset.
cl_weapon_offset_z <#>	    // 5.0, weapon forward/back offset.
cl_weapon_rotation <0/1>	// Enables/disables weapon bounce/sway while moving/jumping.
cl_weaponcycle		        // enables/disables weaponnext/weaponprev from being able to cycle back to beginning/end
```

```
com_idlesleep               // for dedicated servers, will very slightly reduce latency at the expense of pretty much maxing out your CPU. It was for testing and I'm surprised it's still in there (newborn).
com_logclearonstart
com_logfilename
com_maxfps                  // define the maximum frame rate of Reflex
connect <IP>                // Connect directly to a Reflex Arena server using the IP address
connect_lobby               //
crash
disconnect                  // disconnect from server;                 bind f12
```

```
editorclone                 // duplicate selected brush;             bind space
editordelete                // delete selected brush;         bind backspace, q
editorredo                  // redo an editor operation;                 bind x
editortoggleclipmode		// ??? (unimplemented);                      bind c
editortogglevertexmode      // toggle to vertex mode;                    bind v
editorundo                  // undo last editor operation;               bind z
forfeit
```

```
forge
forge_description
forge_foldername
forge_load
forge_name
forge_paint_style
forge_pattern_col0
forge_pattern_col1
forge_pattern_col2
forge_pattern_col3
forge_pattern_offset_max_x
forge_pattern_offset_max_y
forge_pattern_offset_min_x
forge_pattern_offset_min_y
forge_pattern_offset_x_fromseed
forge_pattern_offset_y_fromseed
forge_pattern_rotation_fromseed
forge_pattern_rotation_max
forge_pattern_rotation_min
forge_pattern_scale
forge_pattern_texture
forge_save
forge_seed
forge_type
gconst_armor100_faratten
gconst_armor150_faratten
gconst_armor50_faratten
gconst_beam_damage
gconst_beam_distance
gconst_beam_knockmult
gconst_beam_knockmult_airbourne
gconst_beam_trace_radius_entities
gconst_beam_trace_radius_world
gconst_bolt_damage
```

```
hud_vote_x				// 20,
hud_vote_y				// 300,
ip
keylist					// list of "bind"able keys (see first post on page)
loadconfig <config>			// loads <config>.cfg file from main game folder
```

```
m_advanced <0/1>			// enable advanced mouse/accel settings; KovaaK's Reflex acceleration wizard: http://mouseaccel.blogspot.com/2015/12/reflex-mouse-accel-configuration-wizard.html
m_advanced_acceleration <#>	// amount of mouse acceleration
m_advanced_angle <#>		// mouse acceleration angle
m_advanced_input_frequency <#>	// set input frequency of mouse
m_advanced_offset <#>		// mouse acceleration offset
m_advanced_postscale_x		// mouse acceleration scale for x axis
m_advanced_postscale_y		// mouse acceleration scale for y axis
m_advanced_power			// mouse acceleration curve, defaults to 2 (linear)
m_advanced_sensitivity_cap		// sets max sensitivity for mouse acceleration
m_advanced_sensitivity_cap_min
m_enable				// ???
m_invert <0/1>			// 0, invert up/down mouse movement in view
m_speed <#>				// 32.0, set the mouse sensitivity to movement in view
map editor
map <map>				// launches server loading <map>.map file
me_activealbedo <HEX>		// set current material color
me_activematerial <mat>		// define active material on console manually e.g. internal/editor/textures/editor_nolight
me_breakprefab				// Breaks selected prefab into it's components
me_createprefab <name>			// Turns selected items into a prefab, avoid putting pickups in prefabs as it is known to cause issues 
me_createtype “worldspawn teleporter jumppad target effect pickup pointlight playerspawn prefab racefinish racestart reflectionprobe volumeselect weaponrestrictor workshopscreenshot”
me_destroyprefab
me_getmaterial				// gets texture from active brush;   bind mouse5, k
me_listprefabs					// list prefabs in map file
me_purgeprefabs				// purge unused prefabs in a map
me_refmodel					// These are just dev commands that allow you to put an unselectable mesh in the middle of a map. Pretty useless for users since they can't actually create the meshes anyway. Should probably be moved to our debug only commands (newborn).
me_refmodelalpha				// 
me_rotate_dec
me_rotate_inc
me_segments
me_segments_dec
me_segments_inc
me_setentityproperty <entityid> <propertyname> <propertyvalue>    // sets the properties of an entity
me_setmaterial				// puts texture on active brush;     bind mouse4, m
me_showclip <0/1>				// Shows/hides clip brushes while in editor
me_showproperties 1				// opens property window for selected item;  bind n
me_snapangle <#>				// set the angle in degrees for rotating objects
me_snapdistance
me_startbridge
me_texcoords_dec_offset_x		//                                        bind left
me_texcoords_dec_offset_y		//                                        bind down
me_texcoords_dec_rotation		//                           bind mousewheelup or ,
me_texcoords_dec_scale_x		//                                      bind insert
me_texcoords_dec_scale_y		//                                      bind delete
me_texcoords_flip_scale_x		//                                      bind pageup
me_texcoords_flip_scale_y		//                                    bind pagedown
me_texcoords_inc_offset_x		//                                       bind right
me_texcoords_inc_offset_y		//                                          bind up
me_texcoords_inc_rotation		//                         bind mousewheeldown or .
me_texcoords_inc_scale_x		//                                        bind home
me_texcoords_inc_scale_y		//                                         bind end
me_texcoords_lock <0/1>		// 0, ???
me_updateprefab <name>			// updates specified prefab with currently selected objects
me_volumeselect_apply			// applies selection to current objects within volumeselect brush
```

```
memreport				// ???
name <player name>			// set the player name
nav_build
nav_cancel
nav_debug
notready				//
play					// Play a replay file
profileplay				// Plays a replay and tells you how many FPS you averaged during it (newborn).
quit					// exit Reflex
renderer
r_adapter				// Specifies video adapter?
r_bloom <0/1>				// 1, turn on/off bloom effect
r_decals <0/1>			// 1, show decals
r_depth_export_scale <#>		// 13.5,
r_desktop_composition		// ???
r_dynamic_lights <0/1>		// 1, show lights rendered in real time (expensive)
r_effect_quality <0/1/2>		// sets quality of game effects; 0 - low, 1 - medium, 2 - high 
r_fog <0/1>				// enables/disables depth fog
r_fov <#>				// 110, the field of view
r_fullscreen <0/1>			// 1, switch between window (desktop) and full screen mode
r_fullscreen_forcestretched <0/1>	// forces stretched resolution in fullscreen
r_fxaa <0/1/2/3>			// fast approximate anti-aliasing; 1-3 is low to high quality
r_gamma
r_hbao <0/1>				// enables/disables HBAO ambient occlusion
r_high_vis <0/1>			// 1, Activate "high visibility" render mode/Remove block effect 
r_listmodes				// ???
r_lm_build				// perform lightmap compile of the map;      bind f4
r_lm_clear				// ???, delete the lightmap file?
r_lm_probe_batch_count <#>		// 128, ???
r_lm_showprobe_correct
r_lm_showprobes <0/1>		// 0, show the light probe spheres (for dynamic lights) in map
r_lm_stats <0/1>                   // 0, show compile stats, texels/s, compile duration, bounces
r_mesh_quality <0/1/2>              // sets quality of meshes; 0 - low, 1 - medium, 2 - high                                    
r_occlusion                        // enables/disables occlusion culling
r_profiler <0/1>                   // (not working), shows usage cpu/gpu on time spend in rendering
r_refreshrate <#>                  // 60.0, set the monitor's refresh rate
r_resolution_fullscreen <x> <y>    // set fullscreen resolution
r_resolution_windowed <x> <y>      // set windowed resolution
r_shader_quality <0/1/2>           // sets quality of effect shaders ; 0 - low, 1 - medium, 2 - high 
r_shadow_quality <0/1/2>           // sets quality of shadows, high is very resource intensive ; 0 - low, 1 - medium, 2 - high 
r_shadow_resolution
r_showfps <0/1>                    // 0, display the number of frames per second in HUD
r_showlights <0/1>                 // black map, light entities show (items, TP, ...)
r_silhouette                       // shows/hides team/spectating player silhouttes through walls.
r_smaa <0/1/2/3>                   // spatial anti aliasing; ; 1-3 is low to high quality
r_stats 1                          // real-time stats: # lights, materials, drawcalls, shadowmaps, fps
r_sun <0/1>                        // enables/disables sun lighting
r_sun_intensity <#>                // sets sun intensity, higher makes it brighter
r_rexture_memory_stream_cache
r_texture_quality
r_texture_resolution
r_vsync <0/1>                      // synchronize game frame rate with monitor refresh rate
r_windowed_fullscreen 0/1
r_zprime <0/1>                     // ???
```

```
rcon
rcon_address
rcon_password
```

```
replays
re_add_keyframe               // adds animation/camera movement keyframe
re_edit_toggle                // toggles keyframe editor (a sub-mode like vertices in map editor)
re_export			// starts dumping frames to disk as TGAs
re_export_depth
re_export_frame_rate		// sets the framerate used for re_export
re_next_frame			// moves replay 1 frame forward;  bind ]
re_next_keyframe		// moves to next keyframe
re_next_marker		// move to next marker
re_prev_frame			// move replay 1 frame backward;          bind [
re_prev_keyframe		// moves to previous keyframe
re_prev_marker		// moves to previous custom marker
re_remove_keyframe		// deletes keyframe created with add_keyframe
re_save			// hopefully this will save to an external keyframe/telemetry file
re_seek_to			// moves replay to specific time
re_set_angle			// set camera angle
re_set_angle_lerp		// sets the interpolation method used when changing angles between keyframes (newborn)
re_set_fov
re_set_fov_lerp
re_set_player_attached_to		// attach camera to specific player
re_set_player_looking_towards	// set camera position/angle to look in certain direction
re_set_position		// set camera position
re_set_position_lerp		// sets the interpolation method used when changing position between keyframes (newborn)
re_setentityproperty
re_speed #			// stop replay
re_spline_visible_travel_time // shows camera path waypoints
re_zero_roll			// sets the roll of the camera back to 0, difficult to do otherwise (newborn).
```

```
ready				// bind f3
reconnect			//
referee				// enter referee mode
reset_vars			// reset settings to default
roll				// roll a number, define a range
```

```
sound
s_announcer_volume
s_effects_volume
s_music_volume
s_rot
s_volume			// 0.4, set the volume
```

```
saveconfig			// saves current config, or saves config with specified name
savemap			// quicksaves the current map;              bind f5
savemap <mapname>           // manually saves map under <mapname>.map
say				// open chat window;                  bind space, t
sayparty
sayteam			// open team chat window;                    bind y
screenshot			// saves screenshot in base\screenshots\ as TGA file
screenshotClean		//
screenshotWithDepth		// takes two screens, normal, and depth represented in grey scale
showscorescursor		// shows cursor in scoreboard
showscorescursorhook	// allows showscorecursor to hook into jump/attack key
suicide
```

```
server
sv_addbot
sv_allowcallvote
sv_allowcallvotemapmode
sv_allowcallvotemutators
sv_allowedit <0/1>			// Allow players to edit maps on the server
sv_allowmodes			// List of modes to allow on the server
sv_allowrulesets
sv_autorecord <0/1>			// 1, Automatically records replays on server
sv_country				// set country flag
sv_gameport 25787			// 
sv_hostname <servername>		// name server shown on server lists
sv_kickallbots
sv_matchmaking_game
sv_matchmaking_key
sv_maxclients <#>			// 8, maximum number of clients that can connect to server
sv_mode
sv_mutators
sv_password
sv_refpassword
sv_report_back_missing_client_packets
sv_ruleset
sv_startmap				// the <map>.map file to load on server launch
sv_startmode
sv_startmutators
sv_startrotation			// starting server rotation
sv_startruleset
sv_startwmap				// workshop map to start on
sv_steam				// enable/disable steam integration
sv_timelimit <#>			// 600; time limit for each game round
sv_timelimit_round			// 90; time limit for round-based modes (a1v1/affa/atdm etc)
sv_timelimit_round_override
toggleeditor				// toggle between editor and game;      bind mouse3
user interface
ui_connect_showpassword
ui_crosshairs_g
ui_crosshairs_g
ui_crosshairs_r
ui_crosshairs_type
ui_crosshairs_typehit
ui_hide_all				// hides all UI widgets
ui_hide_widget			// hides specified UI widget
ui_list_widgets				// lists installed widgets
ui_matchpicker_selectedfilter
ui_menu_show_server_empty
ui_menu_show_server_locked
ui_menu_show_server_mm
ui_menu_show_server_old
ui_menu_show_widget_properties_height
ui_menu_startbot1-8
ui_menu_training_multiplayer
ui_reset				// resets ui
ui_scoreboard_leaderboard		//
ui_set_widget_anchor <name> <x> <y>    // sets the grid anchor of widget
ui_set_widget_offset <name> <x> <y>    // sets x/y offset of widget
ui_set_widget_scale  <#>               // sets scale of widget
ui_set_widget_zindex <#>               // sets priority(?) of widget
ui_show_axis                           // shows axis of widgets on screen, useful for positioning
ui_show_mouse_regions                  // shows clickable regions on menu ui
ui_show_widget                         // shows specified widget
ui_viewport_height                     // sets viewport height for screen
Weapons
weapon 1			// Axe;                                   
weapon 2			// Burstgun;                                
weapon 3			// Shotgun;                                
weapon 4			// Grenade Launcher;                              
weapon 5			// Plasma Gun;                                    
weapon 6			// Rocket Launcher;                            
weapon 7			// Ion Cannon;                                  
weapon 8			// Bolt Rifle;                                      
weapon 9			// Stake; Currently removed from game.                      
weaponnext			// switch to next available weapon
weaponprev			// switch to previous available weapon
```

```
unbind <key>			// Unbinds a <key>, use keylist for a list of valid keys
unbindall			// Unbinds all keys previously defined
unreferee			// Exit referee mode
vote_no			// bind F2
vote_yes			// bind F1
wmap <id>			// Load a map using the map’s workshop ID
```