# Patch Notes - 2019

[Suggest Edits](/edit/patch-notes-2019)The patch notes listed here are from 2019. They are listed in descending order, with the most recent at the top.


# VRChat 2019.3.2p3


Release - 12 Dec 2019 - Build 866


## Client


### Fixes


* Safety and security changes


# VRChat 2019.3.2p2


Release - 2 October 2019 - Build 864


## Client


### Fixes


* Fixed issue with not seeing users sitting properly on your avatar station


# VRChat 2019.3.2p1


Release - 1 October 2019 - Build 862


## Client


### Fixes


* Fixed an issue where "PC Placeholder" Quest avatar would not show up properly
* Fixed an issue where blocked avatars would not IK properly
* Fixed an issue where users could sit in their own stations


# VRChat 2019.3.2


Release - 18 September 2019 - Build 860


## Client


### Features


* When in Full-Body Tracking mode, the Sit/Stand button converts to a Calibrate button
* Pressing this button clears the calibration, reloads the current avatar, and prompts for a fresh calibration
* Lots of tuning to Full-Body Tracking in general. Check out the Fixes section to learn more
* **Due to these changes, some "Full-body Hacks" may cause issues.** See the Known Issues section to learn more


### Changes


* The Upper Chest now moves more naturally, as opposed to previous behavior where it would not rotate in an expected manner
* Content uploaded with versions greater than what VRChat supports (as of 2019.3.2, Unity 2017.4.28f1) will not load in the client. Worlds will be inaccessible, and avatars will be replaced by a placeholder, unless there is a previous version available that is compatible


### Fixes


* Full-Body Tracking: Improved behavior of viewpoint in various situations. Your headset's viewpoint should now more reliably track to your avatar viewpoint
* Full-Body Tracking: Several other smaller tweaks to improve behavior during calibration and usage
* When looking down, neck bending should behave more naturally when compared to previous behavior
* Fixed an issue where very small avatars would not be able to see the Avatar Performance Stats text
* Fixed an issue where Reporting a user could result in a NullRef and error despite the Report still sending
* Fixed an issue where the Voice Cone calculation was incorrect


### Ongoing


* Safety and Security fixes
* Further iteration on Networked IK is occuring in closed testing


### Known Issues


* Avatars that utilize "Full-body Hacks" such as flipped hips, extra leg bones, zero-length or unweighted necks, or other similar changes may encounter undocumented behavior. We recommend against the use of these types of changes, as they will cause problems during future updates to the Full-Body Tracking system. For ensuring your avatar's rig is ready for full-body usage, please consult [the Full-Body section of our Rig Requirements](/docs/rig-requirements#section-full-body-tracking) and the [Full-Body Tracking system guide](/docs/full-body-tracking).


## SDK


### Fixes


* Fixed an issue where user-defined dynamic prefabs would be wiped from the [VRC\_SceneDescriptor](/docs/vrc_scenedescriptor) during scene building


# VRChat 2019.3.1p5


Release - 11 September 2019 - Build 852


## Client


### Fixes


* Updated video helper binaries


# VRChat 2019.3.1p4


Release - 5 September 2019 - Build 850


## Client


### Fixes


* Fixed a crash that would occur often upon world change or avatar loading
* Fixed an issue that appeared in [2019.3.1p3](/docs/vrchat-201931p3) that prevented livestreams from playing in [VRC\_SyncVideoStream](/docs/vrc_syncvideostream) players


# VRChat 2019.3.1p3


Release - 4 September 2019 - Build 848


## Client


### Fixes


* Safety and Security fixes


# VRChat 2019.3.1p2


Release - 28 August 2019 - Build 845


## Client


### Fixes


* Multiple changes made to address crashes during world or avatar loading
* Some further optimizations to asset bundle loading
* Fixed incorrect Mesh and Skinned Mesh Renderer counts for "Good" avatar rating


# VRChat 2019.3.1p1


Release - 22 August 2019 - Build 842


## Client


### Fixes


* Fixed an issue where some users could not log in with certain characters in usernames
* (Client update not required) Fixed a bug causing issues with accessing the Quick Menu, low performance, and other issues


# VRChat 2019.3.1


Release - 22 August 2019 - Build 840


## Client


### Features


* Greatly improved behavior for the [Minimum Displayed Performance Rank](/docs/avatar-performance-ranking-system#section-minimum-displayed-performance-rank) system
	+ Instead of blocking the whole avatar, the system now gracefully degrades avatar features depending on what component's limit is being passed
		- As an example, if an avatar has too many Lights on it, all Light components on the avatar will be removed
		- As before, your preference for the Minimum Displayed Performance Rank can be adjusted in `Safety > Performance Options > Avatar Performance`
		- **Please read the [detailed documentation](/docs/avatar-performance-ranking-system#section-minimum-displayed-performance-rank) for more info**
* Lots of fixes for the SDK, including a UI overhaul! Check out the [section below](/docs/latest-release#section-sdk) for details


### Changes


* ***On all control schemes, "Grip" no longer triggers OnInteract.*** This means that on Rift / Rift S / Index, you can no longer sit in chairs or set off Interact triggers by using Grip. Use your controller's Trigger instead!
	+ This was done to solve some UX issues, as well as to bring all control schemes into line
* Calibrating Full-Body Tracking now requires pulling *both triggers* on all controller schemes. Previously Index would calibrate on both grips being squeezed
* Updated required bindings version to invalidate older binds. This shouldn't affect your currently-used binding, but if you maintain an uploaded Community binding, ***you may have to upgrade your shared SteamVR binds!***
* Changed Announcement screen placeholder text to be a bit less keyboard-smashy ([Feedback Item](https://vrchat.canny.io/feature-requests/p/unfriendly-anouncement-error-message))
* Avatar Performance Stat calculation for "Bounds" should no longer consider Trail or Line renderers in its calculation
* Due to the above change, "Bounds" Avatar Performance Stat calculation can now push your avatar into "Very Poor" rank. However, the [Minimum Displayed Performance Rank](/docs/avatar-performance-ranking-system#section-minimum-displayed-performance-rank) does not affect avatars as a result of Bounds size being exceeded, so avatars will never be blocked or modified due to Bounds size
* Added a new loading screen interstitial to promote [Two-Factor Authentication](/docs/setup-2fa)
* Added an option in Settings to "Show Community Labs". If you disable this, you will not be shown Community Labs worlds in the Worlds UI
* Added both VC2010 and VC2015 runtime prerequisites. These will be handled at install-time on whatever platform you're on
* Further reduction of redundant or excessive logging
* Updated video helper binaries


### Fixes


* Greatly improved avatar loading time
* Corrected issue where audio sources on avatars using certain custom curves would ignore the world's Far distance limit
* Optimized behavior of physics syncing in some situations
* Improved consistency between LODBias for Desktop and VR clients for LODGroups ([Bug Report](https://vrchat.canny.io/bug-reports/p/lodbias-is-effectively-much-lower-in-vr-than-desktop-which-makes-lodgroups-drop-))
* Fixed various issues with the "Back" button not working as expected
* Fixed a memory leak issue with [VRC\_Panorama](/docs/vrc_panorama)
* Fixed an issue with Quest where the Terms of Service would not properly load in rare situations
* Fixed an issue with ban message not appearing for some users
* Fixed an issue where Index controller wireframes would sometimes get stuck in user's hands
* Fixed an issue where bounds size was incorrectly calculated when Unity scale was not set to 1.0


### Ongoing


* Safety and Security fixes
* Further iteration on Networked IK is occuring in closed testing


### Known Issues


* There are some known issues with the SDK layout. In particular, there are problems:
	+ ... when the Control Panel is docked
	+ ... when using a resolution lower than 1080p
	+ ... when viewing assets with excessively long names
* We are planning on releasing some further fixes for the SDK within the coming days. For now, we recommend that users encountering layout issues do not dock the Control Panel UI, and instead use the window undocked/floating


## SDK


### Changes


* UI overhaul for several parts of the SDK! We plan on iterating on this further
* [VRC\_Pickup](/docs/vrc_pickup) now has text fields for Interaction text and Use text. Interaction text appears when you hover over the pickup, and Use text appears when an Equippable object is equipped/grabbed
* [VRC\_SceneDescriptor](/docs/vrc_scenedescriptor) Dynamic Material properties are cleared and regenerated upon each scene build instead of building up on previous entries ([Bug Report](https://vrchat.canny.io/sdk-bug-reports/p/sdkscene-descriptor-can-keep-references-to-unused-materials-alive)
* Removed the ability to change API to "Beta", as it is currently not in use
* Added dropdown toggles and a **search field** for the Content Manager panel
* If spatialization is turned off for a [VRC\_SpatialAudioSource](/docs/vrc_spatialaudiosource), always use the Audio Source's curve
* "Auto-spatialize Audio Sources" is now deprecated and defaults to False
* Changed VRC\_Chair prefab to use the VRChat Mobile Diffuse shader by default
* Added seperate warnings and fixes for ONSP conversion and when no VRC\_SpatialAudioSource is present
* Added a check for 2D vs 3D audio, and use that result to determine if we should enable spatialization


### Fixes


* `VRCWorld` prefab had an extraneous [VRC\_EventHandler](/docs/vrc_eventhandler) removed ([Bug Report](https://vrchat.canny.io/sdk-bug-reports/p/vrcworld-prefab-has-vrcevent-handler-on-it-and-tells-you-that-is-incorrect))
* Resolved an issue where [VRC\_Pickup](/docs/vrc_pickup) did not properly use the Use text
* Resolved an issue where running a custom trigger action on a disabled object would result in a NullReference exception
	+ As a side-note: Per Unity's established behavior, VRC\_Triggers on disabled GameObjects do not run their per-frame updates. As such, we do not support Triggers on disabled GameObjects performing actions.
* Fixed an issue where a Trigger with a Null receiver would target itself
* Fixed an issue where `EditorOnly` tag was ignored when applied to objects on avatars. It is no longer ignored, and objects on avatars with the `EditorOnly` tag are now ignored on upload
* Removed extraneous error from SDK when Upper Chest was mapped on an avatar
* Resolved an issue where the SDK would cause lag hitches due to waiting on extraneous API calls
* Fixed an issue where [VRC\_Trigger](/docs/vrc_trigger)'s randomize function could lock up the Editor
* Fixed an issue with using the default [VRC\_Station](/docs/vrc_station) prefab in the SDK's examples where it would throw naming warnings
* Fixed an issue where the SDK may not work properly when operating in filesystems that are not case-agnostic
* Fixed several issues where having the SDK's Build Control Panel open would cause intermittent lag/hitching in Editor
* Fixed an issue where some [Trigger](/docs/vrc_trigger) actions were missing when used alongside a [VRC\_Station](/docs/vrc_station) component on the same GameObject
* Fixed an issue where the image thumbnails in the SDK were too dark
* Fixed an issue where world details would not be cleared in SDK Builder panel if Blueprint ID was detached in Scene Descriptor component
* Fixed an issue where network events would not work on objects named with Korean characters (or other extended character sets)


# VRChat 2019.2.5


Release - Build 825 - 31 July 2019


## Client


### Features


* We've revamped and updated our audio system! Audio spatialization has been re-tuned and several new features and components are available
	+ A focus on improvement of user voice, fixing issues with spatialization, and improving audio overall
	+ Improved the default voice falloff parameters
	+ Added a compressor/limiter to avatar audio channel to prevent maliciously loud audio
	+ Added a (separate) compressor/limiter to user voice channel to prevent maliciously loud audio
	+ Added a low-pass filter for voice audio at long range
	+ Some adjustments to the Gain on various sound channels for better audio balance
	+ Removed "Voice Prioritization" option
	+ Changed voice falloff behavior. For details, see our [documentation](/docs/vrc_playeraudiooverride#section-vrchat-falloff-curve-adjustments) regarding our voice falloff curve
	+ Check out the SDK section for changes relevant to world and avatar creators, namely the addition of the [VRC\_SpatialAudioSource](/docs/vrc_spatialaudiosource) and [VRC\_PlayerAudioOverride](/docs/vrc_playeraudiooverride) components
	+ Further changes to prepare for later audio upgrades
* Added some new summer emoji!


### Changes


* Streamlined audio mixer
* There are now only 5 volume sliders: Master, Menu, Voice, World, and Avatar
	+ Default values for these sliders will be adjusted on first launch:
		- Master: 100%
		- Menu: 100%
		- Voice: 75%
		- World: 70%
		- Avatar: 60%
* Master volume setting can be overdriven to 125%. Going over 100% will cause the text to turn red. Be very careful setting Master above 100%!
	+ This change is intended to accomodate for various hardware setups. If you swap devices, re-check this setting
* Removed menu "cyber" background sound
* Optimized use of UI audio sources for Quest
* Added controller wireframe models for new Touch controllers, Index controllers
* Improved IK performance in low-FPS situations
* Added new World Report reasons
* Updated to Oculus Unity Integration 1.37
* Updated video helper binaries (three times, just to make sure)


### Fixes


* Fixed an issue where blendshape visemes would sometimes get stuck locally after mic input was completed
	+ This fix also involves a very small change in blendshape viseme behavior. Your default model state should be "non-speaking", and the `sil` blendshape should be essentially unchanged from that, aside from one vert slightly moved to prevent Unity from removing the empty blendshape on import. This is because we now reset all viseme blendshapes to zero when speaking is complete. We don't expect this to impact many users, but we're putting this info here just in case
	+ As an aside, the `sil` blendshape is what is used when silence is detected but the mic is still open. When mic activity stops (the icon goes out), all viseme-related blendshapes are set to zero.
* Fixed an issue preventing Fixed Foveated Rendering from working on Oculus Quest
* Fixed an issue where Line Renderers were being counted improperly in the Avatar Perf Stats system
* Fixed an issue where tooltips on controllers were sometimes incorrect
* Fixed an issue where some components were not reliably blocked using the Safety system


### Ongoing


* Safety and Security fixes
* Further iteration on Networked IK


### Known Issues


* If a GameObject on an avatar with a 2D Audio Source starts as disabled, it will be 3D when enabled. To work around this, enable/disable the Audio Source component, not the GameObject it is attached to
* Some menu sounds may be slightly louder than others in some situations
* Valve Index Controller users may find that their controllers are stuck in their hands during some launches
* Quest users may encounter audio "slowing down" in particularly crowded instances


## Website


### Changes


* Small flow improvements to the account creation and verification process
* Error page added for cases where an attempt to verify an email address fails
* Improvements to the ToS agreement process on the VRChat website


## SDK


### Changes


* Added `VRC_ObjectSync.Respawn`, which is accessible via the SendRPC event on [VRC\_ObjectSync](/docs/vrc_objectsync)
* Allow multiple Triggers/Trigger types on the same `VRC_Trigger` component
* `VRC_Trigger` will now default to "Default" layer mask and "TriggerIndividuals"
* Audio Changes
	+ Added component [VRC\_PlayerAudioOverride](/docs/vrc_playeraudiooverride), to allow customizing voice and avatar audio behavior using Trigger zones or globally. You can use this to customize scene-wide falloff, create a performance stage for wider-reaching audio, or adjust falloff based on the part of the world the user is in. Check [the documentation](/docs/vrc_playeraudiooverride) for details
	+ Added component [VRC\_SpatialAudioSource](/docs/vrc_spatialaudiosource) which replaces `ONSPAudioSource`. Check [the documentation](/docs/vrc_spatialaudiosource) for details
	+ Using the "Enable 3D Spatialization" button in the Build Control Panel will now apply [VRC\_SpatialAudioSource](/docs/vrc_spatialaudiosource) instead of `ONSPAudioSource` (and will convert existing ONSP sources)
	+ Removed "custom voice falloff range" from world descriptor, this option is no longer supported. Use a [VRC\_PlayerAudioOverride](/docs/vrc_playeraudiooverride) with Global toggled on instead.


### Fixes


* Fixed a bug where onStation triggers weren't appearing in list
* Fixed issue where sometimes importing the SDK would cause Unity Editor to hang


# VRChat 2019.2.4-SDK1


SDK-only Release - 19 June 2019


## SDK


### Changes


* Removed upload-preventing polygon limits for avatars in SDK.
* This does not change behavior in the client. Although you can upload content that goes beyond client limits (for example, the Quest polygon limit), it will not render in VRChat according to the Minimum Performance Rank setting


# VRChat 2019.2.4


Release - Build 801 - 18 June 2019


## Client


### Features


* **VRChat has been upgraded to Unity 2017.4.28f1!** Please update your Editor! See [Setting up the SDK](/docs/setting-up-the-sdk) for links for Unity Hub and direct-download installs
* **[You can now block avatars based on their Performance Ranking!](/docs/avatar-performance-ranking-system#section-minimum-displayed-performance-rank)** Choose your Minimum Avatar Performance Rank in the Performance Options menu in the Safety tab.
	+ Depending on the level you set, avatars that rank worse than your setting will be hidden with a special placeholder avatar.
	+ For PC, the default minimum rank is "Very Poor". No avatars will be hidden by default
	+ For Quest, the default minimum rank is "Medium". "Poor" ranked avatars will not show unless you change the setting to "Poor". "Very Poor" avatars will never show on Quest
	+ You can bypass this for individual users by using "Show Avatar" in your Quick Menu after selecting the user
* **You can now Save Searches for later use!** These Searches will appear in your Worlds menu as new rows
	+ Save a search by clicking "Save Search" in the top right after performing a search
* **Implemented updated Avatar Performance Ranking levels for Oculus Quest.** See the stats for each performance rank in our [Avatar Performance Ranking System](/docs/avatar-performance-ranking-system) doc
	+ Because "Very Poor" avatars will never show on Quest, any avatar that goes above the limits given for "Poor" will not be displayed on Quest.
	+ Short version: **The default polygon limit on Quest is 7,500, optionally raise-able to 10,000** via the Minimum Performance Rank in the Performance Options menu
* **Attention Avatar and Game World authors:** You can now define yourself as an avatar or game world! Simply use `avatar` or `game` as one of your tags, and you'll show up in the appropriate row
	+ If your world is currently marked as an avatar or game world, the tag will be migrated appropriately
* **You can now use Account Link to link your Oculus account to your VRChat account**, similar to how Steam users can link their account. Linking your Oculus account to your VRChat account will "merge" your account data into your VRChat account! Start the process in your Settings menu in the bottom right while logged into your Oculus account.


### Changes


* Thanks to the Unity upgrade, **you can once again switch your microphone using the Settings menu!**
* Avatar Performance Ranking and Stats are now more accurate
* **Disabled objects and components are now counted in the Avatar Performance Stats readout.** For example, if a Light is on an avatar but is disabled until it is enabled by an animation, it will still count towards the Performance Stats for that avatar, and therefore will affect its rank
	+ As a result, the current Performance Rank of avatars that contain disabled components may decrease
* Some Index controller refinements
	+ Triggering Gesture Overrides no longer requires squeezing the grip, only posing your fingers
	+ Your thumb now moves side-to-side depending on which thumb capsense sensor you touch (buttons, touchpad, thumbstick)
	+ Default thumb pose tweaked slightly. If your min/max thumb pose is still off, try adjusting the min/max muscle limits as set in the Unity Rigging "Muscles & Settings" window
* Prefab instantiation now has a "cooldown" period of one second per prefab per player
* Changed the way that we obtain/retrieve rows in the Worlds tab to allow for easier, dynamic updating of row types, sorting, and other features
* Removed the ability for Desktop users to set user height (as it has no effect)
* Updated video helper binaries


### Fixes


* Fixed a (very old) bug that prevented locomotion from cancelling emotes
* Fixed a bug preventing Holoport from working while using Valve Index Controllers
* Fixed a bug causing Touch controllers to display the wrong model when used in SteamVR
* Fixed a bug preventing VRC\_OscButtonIn from functioning properly
* **Fixed a bug preventing avatar rows from paginating properly**
* Fixed a bug causing odd offsets to occur during normal play while using Valve Index Controllers
* Fixed an issue where a user using Desktop mode, launching VRChat from a desktop shortcut, and using a short avatar/setting user height too low would prevent use of the the menu/UI
* **Attention shader authors:** The Unity 2017.4.28f1 upgrade fixed a bug with Unity where `SV_IsFrontFace`/`VFACE` was wrong when viewed in cameras or mirrors. If you were compensating for this bug (by flipping face normals when in a mirror, for example), things will now be broken and lighting will not behave properly. You'll need to update your shaders!
	+ For users, this means you might have to update your shaders on your avatar if things look off in mirrors.
* Fixed issue where a client restart was required to see an updated world.


### Ongoing


* Safety and Security fixes
* Further iteration on Networked IK


## SDK


### Changes


* Implemented Quest Avatar limits. If your avatar is ranked as "Very Poor", you will not be able to upload the avatar.
	+ If you do upload an avatar beyond the "Very Poor" limits, it will not render in VRChat Quest regardless


# VRChat 2019.2.3p1


Release - Build 793 - June 7, 2019


## Client


### Fixes


* Fixes to prevent faulty client disconnects in some cases


# VRChat 2019.2.3


Release - Build 791 - June 5, 2019


## Client


### Features


* **Valve Index Controller Support!** - We now have first-pass support for the upcoming Valve Index Controllers, including finger tracking! Ensure that you are using the default mapping for Index Controllers in the SteamVR `Settings > Controller Binding > VRChat` menu. Check out our documentation on the **[Valve Index control scheme here](/docs/valve-index)**. We've also got a post about our Index Controller support that you can find **[on our blog](https://medium.com/@vrchat/vrchat-valve-index-support-and-the-gesture-toggle-system-742ec3ae016e)**.
	+ **Keep in mind that this support is an "interim" step**, and we've reserved a lot of controller space for future features. As we stated in our Dev Stream, we're continuing to work towards a new UX for things like emojis, emotes, gestures, and other avatar features.
	+ **Important:** If you do not change to the default Valve Index Controller binding for VRChat available in the SteamVR `Settings > Controller Binding > VRChat` menu, you will run into issues! We have set these bindings as the default, but Steam is taking a while to propagate these changes
	+ If your default binding is still called "VRChat - Knuckles", look in the Community binding list for "5% Squeeze Release" towards the bottom, with the description "Official VRChat Bindings..." This is the correct binding to use.
	+ The default bindings are called "VRChat Bindings for Index (Grip Release)", which refers to the method used to pick up objects. There is an alternate binding called "VRChat Bindings for Index (Open Hand Release)" which uses your fingers on your capsense to pick up objects instead. Try both to see which you like more. Read more about these two bindings in our **[Valve Index Controllers](/docs/valve-index#section-alternate-bindings)** documentation
	+ You can also adjust many settings in the SteamVR Controller Bindings menu, including the required strength for grip. Tune these settings if you feel like things are a bit off
	+ There is currently a bug on the SteamVR Beta branch that causes the Controller Binding menu to malfunction. You can access the settings by opening [this page](http://127.0.0.1:8998/dashboard/controllerbinding.html) in your browser with SteamVR running. You can also just swap back to SteamVR's release branch
	+ If you have any feedback regarding our Valve Index Controller support, please post on our [**Valve Index Controller Feedback Canny board**](https://vrchat.canny.io/index-feedback)!
* **Gesture Toggle Button** - ***This is only enabled for Valve Index controllers at this time.*** Press in your left thumbstick to Toggle Gesture overrides on and off. An indicator will appear on your screen showing that Gesture Toggle has been turned on or off
	+ ![Gesture Toggle On Icon](https://i.imgur.com/7c52RaX.png "Gesture Toggle On")![Gesture Toggle On Icon](https://i.imgur.com/7c52RaX.png "Click to close...")**Gesture Toggle On** - Fingers will move with Valve Index controller inputs. In addition, if your gesture matches one of the hand poses you have set a Gesture Override to, it will play that animation on your avatar. However, your hand pose will remain as it is input from the controller
	+ ![Gesture Toggle Off Icon](https://i.imgur.com/w748vGS.png "Gesture Toggle Off")![Gesture Toggle Off Icon](https://i.imgur.com/w748vGS.png "Click to close...")**Gesture Toggle Off** - Fingers will move with Valve Index controller inputs. Your Gesture Overrides will not play
	+ *Example:* You have a Gesture Override that changes "RockNRoll" to a closed fist and a set of blendshapes.
		- With *Gesture Toggle On*, you must hold the "RockNRoll" hand gesture on your controller (Index finger and pinky finger up, with thumb, middle, and ring finger down) to perform the gesture. Your animation on the face will play, but your hand will remain in the "RockNRoll" gesture pose, retaining finger pose state
		- With *Gesture Toggle Off*, no Gesture Override will play and your hand will remain in the "RockNRoll" pose
	+ If you Gesture Toggle while holding a hand pose that triggers an animation override, that override *will remain on until you Gesture Toggle again*
* **Added an Advanced Settings Menu button** in the Settings menu. This currently contains information on your current cache size, as well as a button to clear your cache. You can also reset your cached settings and preferences in this menu


### Changes


* Changed placeholder avatar for when an avatar is not available on your platform. It now displays the avatar image thumbnail on the chest of the avatar, so users on other platforms can have an idea of what the avatar looks like
* Debug info hotkeys can now be set in the Unity Settings Window, which is accessed by holding Shift while launching VRChat. By default, you access this debug info by pressing `RightShift + Backquote + Number`, but you can change `RightShift` and `Backquote` to any other listed two keys. You can also set them to the same button, if you only want to use one button as the modifier
* Added "loading screen overlays" for the SteamVR and Oculus platforms that will appear instead of a black screen while loading content
* When viewing a portal that leads to a world that doesn't support your platform, a red ring and graphic will display indicating that it isn't accessible to you
* Documentation - Large portions of the **[VRChat Documentation](https://docs.vrchat.com)** have been rewritten or revised


### Fixes


* Further fixes to notifications not being received
* Fixes for connection timeouts and "loading loops"
* Some changes to improve connection durability
* Fixes for issues with the Camera
* Fixed an issue preventing moderation tools (warn, kick, etc) from working properly
* Fixed an issue where audio source limit per-scene was set too low. If you're experiencing this issue, the world or an avatar has too many audio sources playing at once
* Fixes for audio issue where voice slows down or gets crackly in certain situations


### Ongoing


This section is new! If something is in the Ongoing section of our patch notes, we're calling out that we are actively continuing work on the system and expect to have further work in near-future releases. This isn't a hard rule, however-- many of our systems (like new features) will almost certainly require ongoing work. If a feature isn't listed in here, it doesn't mean that it is done.


* Safety and Security fixes
* Significant changes to Networked IK to improve latency, precision, delay, and resolve other issues


### Known Issues


* Rarely in populated instances, a single user will appear "stuttery" as if their IK update is very low. This persists until the user rejoins. If you experience this, please make a **[Canny post on the Bug Reports board](https://vrchat.canny.io/bug-reports)** with both the local *and* remote user logs-- in other words, the output logs from your POV (the observer) and the problem user's POV (the "stuttery" person)


## SDK


### Features


* Added a `VRChat/Mobile/Standard Lite` for use on Oculus Quest avatars
	+ Standard Lite offers slots for Diffuse, Normal maps, Metallic+Smoothness maps, and optional Emission maps
	+ Uses a simplified version of BRDF for lighting
* Added "Take Ownership of Action Objects" to [VRC\_Trigger](/docs/vrc_trigger). When checked, this option will tell the trigger to automatically take ownership of objects if the action requested requires it


# VRChat 2019.2.2


May 15, 2019


## Client


### Features


* **Networked IK is back!** Your IK is now calculated locally and the results are transmitted to remote clients. This means that IK is now a lot more performant!
	+ You may notice that IK acts a little differently as a result-- we're paying close attention to these changes and will tune the Networked IK system as needed
	+ *To be clear, "IK" is "inverse kinematics", and is how your avatar's pose is calculated based on how your headset, controllers, and trackers are positioned and oriented. Those calculations are expensive! Now, you only do them for yourself and send the results to other users, instead of everyone doing everyone's calculations.*
* **Several major optimizations to various systems**
* **Added support for cross-platform content** such as icons indicating what platforms an avatar/world supports
	+ Icons will appear on the following content indicating platform compatibility:
		- World thumbnails
		- Portals
		- Avatar thumbnails (including pedestals)
		- User thumbnails indicating what platform they're currently on
		- "Clone Avatar" button
	+ If you attempt to access content that isn't available for your platform, you'll receive a popup message informing you as such
* **Previous default avatars have been moved to a "Legacy" row**
	+ This may not happen immediately with release, but should happen soon after
* **New Featured avatars sourced from our Quest Featured Avatar program have been placed into the Featured row!**
	+ This may not happen immediately with release, but should happen soon after
* **Added new "utility" avatars that appear in certain error or info conditions** such as an avatar not being available for your platform
* **Changed to a new "loading" avatar**


### Changes


* Updated video helper binaries
* Debug info hotkey combo changed from Menu/Application key to Right Shift+Backquote


### Fixes


* Safety and Security fixes
* Fixed an issue that caused users to inadvertently end up in the #1 instance of a world in various disconnect cases
* Some additional fixes to assist with missing notifications
* Holoport fixes
	+ Now ignores the "Water" layer and user layers (all layers rendered below "reserved4", or layers 22-31) as walkable layers
* Resolved memory leak issues with menu caching too aggressively
* More voice handling optimization
* More UI/menu optimization
* More nameplate optimization
* More Holoport optimization


## SDK


### Features


* Added links to the splash screen leading users to our Quest documentation
* Added Quest shaders to SDK, available under "VRChat" category.
	+ Quest will only support these shaders on avatars. If you use any other shader, you'll get a warning in the SDK. If you try to use the shader anyways, it will fail to load in the client.
	+ You can read more about these shaders in our [documentation](/docs/quest-content-limitations)
* Added warnings when attempting to use unsupported shaders on Quest
* Added errors when you attempt to upload content too large for Quest (50mb for worlds, 10mb for avatars). Build size is determined after package is created. This will also be enforced in-client for Quest


### Changes


* Updated splash screen changelogs


# VRChat 2019.2.1p5


24 April 2019


## Client


### Changes


* Updated video helper binaries


# VRChat 2019.2.1p4


23 April 2019


## Client


### Fixes


* Fix for hanging at black screen during world load


# VRChat 2019.2.1p3


## Client


### Fixes


* Safety and Security fixes


# VRChat 2019.2.1p2


16 April 2019


## Client


### Fixes


* Changes to networking protocols and behavior to help alleviate some ongoing server issues


# VRChat 2019.2.1p1


12 April 2019


## Client


### Fixes


* Fix for desktop mouse lock when using menu. [Reported via Canny](https://vrchat.canny.io/bug-reports/p/show-avatar-author-softlock-desktop-only)
* Fixed an issue that caused the quick menu to be unusable for a short period after loading into some worlds with specific setups. [Reported via Canny](https://vrchat.canny.io/bug-reports/p/746-menu-does-not-appear-when-using-steam-in-certain-worlds-using-desktop-or-ocu)
* Improved performance while using Holoport. [Reported via Canny](https://vrchat.canny.io/bug-reports/p/3p-locomotion-drops-lots-of-frames-on-some-places)
* Fix for users not receiving notifications. [Reported via Canny](https://vrchat.canny.io/bug-reports/p/invite-request-notifications-do-not-show-up)


# VRChat 2019.2.1


10 April 2019


## Client


### Changes


* Updated video playback handler binaries
* "Community Spotlight" has been renamed "Spotlight" and its location has changed slightly in the Worlds tab
* "Avatar Worlds" row is now a randomly sorted list of recently updated Avatar Worlds
* VRChat on Steam will now automatically install the 2010 Visual C++ Redistributable, as some of our components depend on it. [Reported via Canny](https://vrchat.canny.io/bug-reports/p/steamoculus-client-dont-install-ms-vc-redistributable-2010-x86-as-a-dependency)


### Fixes


* Safety and Security fixes
* Fixed several VRC\_Trigger issues:
	+ Fixed OnEnable no longer working. [Reported via Canny](https://vrchat.canny.io/bug-reports/p/trigger-onenable-no-longer-working)
	+ Fixed buffered triggers failing to buffer properly. [Reported via Canny](https://vrchat.canny.io/bug-reports/p/buffered-triggers-fail-to-buffer)
	+ Fixed deferred triggers breaking execution order. [Reported via Canny](https://vrchat.canny.io/bug-reports/p/deferred-triggers-break-execution-order)
	+ Fixed OnTimer trigger issues. [Reported via Canny](https://vrchat.canny.io/bug-reports/p/ontimer-reset-on-enable-does-not-reset-its-started-time). As an aside, the example provided in the Canny post is not set to Repeat. If you set the trigger to Repeat in the Trigger Editor, then it will repeat
* The Camera will now properly display Post Processing v2 effects in the viewfinder and images taken. [Reported via Canny](https://vrchat.canny.io/bug-reports/p/the-effects-of-post-processing-stack-v2-cannot-be-reflected-on-photo-camera)
* Fixed an issue causing notifications to stick if no action was taken on them
* Fixed an issue which caused Jaw Flap Bone to stop working properly
* Fixed an issue with using multiple clients (with different accounts) on the same machine. This should work now! [Reported via Canny](https://vrchat.canny.io/bug-reports/p/same-pc-multi-accounting-override) [twice, apparently](https://vrchat.canny.io/bug-reports/p/multi-client-bugs)
	+ However, you can no longer use multiple instances of the same account in the same instance


# VRChat 2019.1.4p2


Build 738 - 29 March 2019


## Client


### Fixes


* Fixed an issue causing low-resolution mirrors in some hardware or software configurations
* Fixed an issue causing avatar stations to misbehave
* Fixed an issue causing output log spam when sibling objects share the same name in a scene/avatar hierarchy
* Fixed an issue causing OnNetworkReady triggers to misbehave
* Added additional logging to help track down some further issues


## SDK


### Fixes


* Fixed an issue causing redundant error messaging when informing the user that there are objects that share the same path


# VRChat 2019.1.4p1


Build 737 - 27 March 2019


## Client


### Fixes


* Fixed an issue causing blurriness, odd behavior on screen-space shaders, and issues using the camera while on the Oculus client
* Fixed an issue leading to some triggers not working properly
* Fixed an issue where notification icons weren't dismissing properly
* Fixed an issue where, upon first load (such as entry into a world), avatars would not "blue man" and would be stuck into the ground until the avatar fully loaded
* Fixed an issue causing problems with Dynamic Bone update order in some specific cases


# VRChat 2019.1.4


Build 735 - 26 March 2019


## Client


### Features


* You can now limit the number of Dynamic Bones and Colliders shown on avatars (or disallow them completely). Read more about our [Avatar Dynamic Bone Limit](/docs/avatar-dynamic-bone-limits) system in our docs
	+ Access the setting in the Safety Tab, using the "Performance Options" button in the top right of the window
	+ This system defaults to the "On" state
	+ The default limit values are 32 Dynamic Bone Transforms and 8 Dynamic Bone Collider Checks
		- These values were chosen to match up with the Medium Performance Rank. See our [Avatar Performance Ranking System](/docs/avatar-performance-ranking-system) docs for details on what precisely these values mean
	+ You can change your limits to fit your needs (or disable Dynamic Bones completely) by editing the configuration file. Read the [docs](/docs/avatar-dynamic-bone-limits) to learn how


### Changes


* Updated video helper binaries
* As long as you've opted into Community Labs at least once, you can now Search for Community Labs worlds
* Significant changes to how Notifications work which should provide quicker response times. If you're interested in a bit of tech chatter, read more about these changes in our [blog post](https://medium.com/@vrchat/developer-blog-websockets-b5f0b424d379).


### Fixes


* Safety and security fixes
* Some optimizations regarding mirror VRAM allocation
* Fixed some headsets having oddly offset object selection highlights


### Known Issue


* Small graphical issue with some of the icons in the Safety menu


## SDK


### Changes


* Some additional tooltips in VRC\_Mirror inspector for clarity
* Added a field for a custom shader on mirrors, allowing the mirror shader to be overridden without the need to swap materials using an animator
* Added a drop-down option for mirrors allowing for the setting of lower fixed resolutions


# VRChat 2019.1.3


12 March 2019


## Client


### Features


* VRChat Community Labs Stage 1 is now Live! Read more about [VRChat Community Labs](/docs/vrchat-community-labs) in our documentation
	+ This is a **massive change** for the way that you get worlds into Public. [Please read the documentation carefully!](/docs/vrchat-community-labs) We also have a FAQ available


### Changes


* Updated video helper binaries


### Fixes


* Safety and security fixes
* Fixed an issue that prevented content from being unloaded properly
* Fixed an issue that broke static batching
	+ This may very rarely cause issues with shaders acting oddly, mostly ones that do object-space vertex deformations. This is because batching transforms all geometry into world space, so “object space” is lost. [If this occurs, try adding `"DisableBatching"="True"` to the shader's tags.](https://docs.unity3d.com/Manual/SL-SubShaderTags.html)
* Fixed some issues that would cause Friend Groups not to display users reliably


## SDK


### Features


* Implemented features to enable usage of Community Labs
	+ Added Community Labs checkbox in the Publish World screen
* Publishing a world no longer changes its release status. If you update a Public World, it now remains public


### Changes


* Changed and updated SDK UI in some places


### Fixes


* Mirrors should now display properly in the editor as we've moved the necessary shader into place


## VRChat Home Website


### Features


* World authors can now view detailed statistics on their worlds!
* You can now publish worlds to Community Labs from the website on the World page.
* You can remove a world from Community Labs (or Public) by pressing the "Unpublish" button.


# VRChat 2019.1.2


26 Feb 2019


## Client


### Features


* We've added a fourth Playlist! You can now save a grand total of 128 worlds to go back to later, or share them with friends


### Changes


* The Link Launcher helper application (the dialog box that pops up after exiting VRChat) now has an option that tells it not to ask you again. If you want to run it again, find it in your VRChat installation directory
* Updated video helper binaries


### Fixes


* Safety and security fixes
* Fixed some World rows that weren't showing up properly
* Interactable highlight has had several optimizations
* Mirrors now use ARGBHalf textures so that they properly capture HDR values
* Mirror disable/enable behavior has been slightly optimized. Enabling a mirror after the first enable/disable cycle should hitch less
* Some fixes to the UI cursor's raycast to improve behavior


# VRChat 2019.1.1p1


7 Feb 2019


## Client


### Fixes


* Fixed an issue where if your avatar could not load for various reasons, you were stuck and unable to move unless you entered Safe Mode or used the `Ctrl-\` Default Avatar shortcut
* Fixed an output log issue
* Fixed an issue where some Standard Assets components were disabled unintentionally


# VRChat 2019.1.1


7 Feb 2019


## Client


### Changes


* World filesize now shows with two decimal places, and displays with the appropriate unit
* When a user is online in a private world, the user's world image now reflects this instead of never loading
* Output logs will now be tagged with a timestamp, and will retain when restarting VRChat. Any log greater than a day old will be deleted
* Updated video helper binaries


### Fixes


* Safety, security, and networking fixes
* Fixed various issues with Playlists
* When you add or remove a favorite friend, your groups and friends list should now update as expected
* Fixed an issue where users had to restart the client in order to get a new world version
* Some fixes to fallback shaders to prevent unwanted behaviour with post-processing
* Some fixes to the "Blue Man" loading avatar that were causing visual issues in worlds with post-processing
* Fixed an issue that prevented users with very high ping from connecting to VRChat
* The keyboard now properly respects input from the physical keyboard no matter what IME is being used
* Issues with IK evaluation order that caused problems with components like VRC\_IKFollower have been fixed
	+ [Documentation on VRC\_IKFollower has been updated](/docs/vrc_ikfollower) to clarify best practices and proper usage
* Avatars should no longer appear prone remotely after spawning
* Fixed some issues with VRChat eye tracking/eye look
* Fixed some issues with voice that would cause loss of quality in various situations


## SDK


### Changes


* Content Manager now behaves better when resizing the window and scales the contents appropriately
Updated 3 months ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [VRChat 2019.3.2p3](#vrchat-201932p3)
		- [Client](#client)
	+ [VRChat 2019.3.2p2](#vrchat-201932p2)
		- [Client](#client-1)
	+ [VRChat 2019.3.2p1](#vrchat-201932p1)
		- [Client](#client-2)
	+ [VRChat 2019.3.2](#vrchat-201932)
		- [Client](#client-3)
		- [SDK](#sdk)
	+ [VRChat 2019.3.1p5](#vrchat-201931p5)
		- [Client](#client-4)
	+ [VRChat 2019.3.1p4](#vrchat-201931p4)
		- [Client](#client-5)
	+ [VRChat 2019.3.1p3](#vrchat-201931p3)
		- [Client](#client-6)
	+ [VRChat 2019.3.1p2](#vrchat-201931p2)
		- [Client](#client-7)
	+ [VRChat 2019.3.1p1](#vrchat-201931p1)
		- [Client](#client-8)
	+ [VRChat 2019.3.1](#vrchat-201931)
		- [Client](#client-9)
		- [SDK](#sdk-1)
	+ [VRChat 2019.2.5](#vrchat-201925)
		- [Client](#client-10)
		- [Website](#website)
		- [SDK](#sdk-2)
	+ [VRChat 2019.2.4-SDK1](#vrchat-201924-sdk1)
		- [SDK](#sdk-3)
	+ [VRChat 2019.2.4](#vrchat-201924)
		- [Client](#client-11)
		- [SDK](#sdk-4)
	+ [VRChat 2019.2.3p1](#vrchat-201923p1)
		- [Client](#client-12)
	+ [VRChat 2019.2.3](#vrchat-201923)
		- [Client](#client-13)
		- [SDK](#sdk-5)
	+ [VRChat 2019.2.2](#vrchat-201922)
		- [Client](#client-14)
		- [SDK](#sdk-6)
	+ [VRChat 2019.2.1p5](#vrchat-201921p5)
		- [Client](#client-15)
	+ [VRChat 2019.2.1p4](#vrchat-201921p4)
		- [Client](#client-16)
	+ [VRChat 2019.2.1p3](#vrchat-201921p3)
		- [Client](#client-17)
	+ [VRChat 2019.2.1p2](#vrchat-201921p2)
		- [Client](#client-18)
	+ [VRChat 2019.2.1p1](#vrchat-201921p1)
		- [Client](#client-19)
	+ [VRChat 2019.2.1](#vrchat-201921)
		- [Client](#client-20)
	+ [VRChat 2019.1.4p2](#vrchat-201914p2)
		- [Client](#client-21)
		- [SDK](#sdk-7)
	+ [VRChat 2019.1.4p1](#vrchat-201914p1)
		- [Client](#client-22)
	+ [VRChat 2019.1.4](#vrchat-201914)
		- [Client](#client-23)
		- [SDK](#sdk-8)
	+ [VRChat 2019.1.3](#vrchat-201913)
		- [Client](#client-24)
		- [SDK](#sdk-9)
		- [VRChat Home Website](#vrchat-home-website)
	+ [VRChat 2019.1.2](#vrchat-201912)
		- [Client](#client-25)
	+ [VRChat 2019.1.1p1](#vrchat-201911p1)
		- [Client](#client-26)
	+ [VRChat 2019.1.1](#vrchat-201911)
		- [Client](#client-27)
		- [SDK](#sdk-10)
