# Patch Notes - 2020

[Suggest Edits](/edit/patch-notes-2020)The patch notes listed here are from 2020. They are listed in descending order, with the most recent at the top.


# VRChat 2020.4.4p3


Release - 8 January 2021 - Build 1033


## Client


### Changes and Fixes


* Fixed an issue causing performance and networking issues when opening menus with large lists of items
* Safety and security fixes


Some users have noted confusion on how to properly disable/enable avatar stations on avatars. Please see the page on [VRC\_Station](/docs/vrc_station) for information on the expected method to disable/enable avatar stations.


# VRChat 2020.4.4p2


Release - 16 December 2020 - Build 1032


## Client


### Changes and Fixes


* Fixed an issue causing [VRC\_PlayerAudioOverride](/docs/vrc_playeraudiooverride) to not function properly in SDK2 worlds.
* Fixed an issue causing the SDK3 AVPro `UseLowLatency` option to not work properly
* Fixed an issue where stations on avatars were being removed
* Fixed some rare cases where terrain would not render properly


# VRChat 2020.4.4p1


Release - 11 December 2020 - Build 1031


## Client


### Changes and Fixes


* Fixed an issue preventing Holoport locomotion from functioning properly
* Fixed an issue that caused avatar favorites over 50 to not display properly
* Fixed an issue preventing the user volume setting not persisting after avatar loads or world changes
* Fixed some further issues with user volume settings
* Fixed an issue causing players to persist too long in worlds after exiting or terminating the VRChat application


# VRChat 2020.4.4


Release - 11 December 2020 - Build 1030


## Client


### Features


* [At player request](https://feedback.vrchat.com/feature-requests/p/adjust-volume-of-individuals), ***we've added volume sliders you can adjust for other users!***
	+ A new volume slider has been added to the Quick Menu. Click on someone's capsule to see and adjust their volume level.
	+ You'll also see a small bar beneath the user volume settings. This indicates the user's current volume from their voice output. It'll adjust in real-time as you turn the user's volume up and down.
	+ User volume settings persist for the current session. They reset when VRChat is restarted. (If you find yourself constantly adjusting someone, you might want to ask them to check their mic volume and settings!)
	+ When the Quick Menu is open, the user volume will display below their name tag. These won't display if the player is muted, or if the player's volume is currently at 100%.
	+ The Settings section of the Main Menu has an option to reset all stored volumes at once. This is disabled when no volumes have been modified.
* The Settings section of the Main Menu now has a meter to show you how loud you sound through your current selected device! Local muting (as in, turning off your mic via VRChat) doesn't affect this, so you can test your mic without bothering others.
	+ Your local nameplate (visible when you open your Quick Menu and look up) now shows the talking effect when you speak.
* When a user's avatar is not visible due to the asset not being available for the platform you are on, the gray "proxy avatar" robot will now instead have a colored tint.
	+ There are a number of geo and color variants of proxy avatars. When you change avatar, a proxy is assigned to that avatar and remains the same variant until you change avatars again
* When a user's avatar is not visible due to the [Avatar Performance Ranking System](/docs/avatar-performance-ranking-system#minimum-displayed-performance-rank), the gray "proxy avatar" robot will have a *slight* colored tint.


### Changes and Fixes


* Tentative fix for master voice stutter
* Various minor performance improvements. More on the way in the new year!
* Fixed issues with the Upright parameter on remote players
* Continued Safety and Security changes


### Known Issues


* Holoport may not work properly after changing worlds
* Exiting the application may cause your avatar to stay in world for longer than intended
* User volume setting may not persist correctly after avatar load or world change


## Udon


* **Important**: All events which have a name starting with underscore `_` will be blocked from being triggered via the network. If you have custom events that start with an underscore, they will not fire via network calls anymore.
	+ If you want to specifically prevent a method from being called over the network, use `_` as the first character of the method name. Existing Udon / VRCSDK methods are reserved, so don't use those.
* Exposed UseLowLatency for AVPro via Udon hooks
* Fixed an issue with multiple entry points connecting to a For loop
* Fixed assigning GameObjects to a public GameObject[] variable


# VRChat 2020.4.3p1


Release - 8 December 2020 - Build 1027


## Client


### Features


* At player request, ***all players can now favorite their own private avatars!***
	+ Select one of your uploaded avatars in the Avatar menu and click Favorite
	+ Avatars you've uploaded will have an icon indicating that it is your creation to differentiate them from your favorited public avatars
	+ If you have VRChat Plus, you can use your additional avatar favorite rows to favorite your personal creations!
* Added file size display (in megabytes) to avatar loading bar


### Changes


* Adjusted appearance of favorite avatar slots in VRC+ rows when the VRC+ subscription has lapsed


### Fixes


* Fixed issues with user camera icon while using a camera in one-handed controller mode
* The `<`, `>`, and `*` symbols should now display properly in nameplates


# VRChat 2020.4.3


Release - 3 December 2020 - Build 1026


## Client


### Features


* **Introducing VRChat Plus!** If you'd like to support the continuing development of VRChat, you now have an option to do so by subscribing to VRChat Plus. In return, you'll get some cool new features, with more on the way! **Read more at our [blog post](https://medium.com/vrchat/vrchat-plus-is-now-live-c8efdf796f2d).**
	+ VRChat Plus costs US$9.99 per month, or US$99.99 per year.
	+ VRChat Plus is available on the Steam platform. We are working towards implementing VRChat Plus on other platforms.
* **All VRChat players** can now store up to **25 favorite avatars** in their first avatar favorites row!
* **VRChat Plus Benefit** - Active VRChat Plus Supporters have a total of **100 favorite avatars** in four rows!
* **New nameplates** with an updated design, new voice effect, automatic distance and name-length scaling, mode switching, and more!
	+ **Customize the appearance of your nameplates** in the Quick Menu (under UI Elements) or in the Action Menu. Adjust the size, opacity, and display mode of the nameplates.
	+ **Switch to icon-only mode** for a more compact look. Users with an icon will only show their icon, and users without an icon will show the first part of their name.
	+ Revamped the **friend icon** to be more visible at range, and to get out of the way when you're close.
	+ **VRChat Plus Benefit** - Active VRChat Plus Supporters will have the ability to **add an icon to their nameplate!**
	+ This icon appears on the left side of your nameplate.
	+ Take a picture in VRChat by selecting the User Icons button on the side of your Quick Menu and use it as your icon!
	+ Upload an image of your own on the [VRChat Home](https://vrchat.com/home) website!
	+ **Store up to 64 different icons** and swap whenever you want for a fresh look!
* **VRChat Plus Benefit** - **Show off your support** with a "VRChat Plus Supporter" indicator in your Social details.
	+ When VRChat Plus goes Live, **players who support us early on will receive a "VRChat Plus Early Explorer" badge** in thanks! It will be visible in your Social details. This badge will only be available for a limited time.
* **VRChat Plus Benefit** - Supporting VRChat via VRChat Plus will confer a small one-time boost to your Trust. You're supporting us, so we'll support you. *This feature will not be live until VRChat Plus launches.*
	+ If you are a Visitor [Trust Rank](/docs/vrchat-safety-and-trust-system), it will boost you to New User, permitting uploading avatar and world content. If you are at or above New User, it will confer a small amount of Trust that may or may not increase your Trust rank. At ranks exceeding User, the trust boost is unlikely to change your Trust rank.


### Changes


* Added "VRC+" option to the main menu.
* Added VRC+ menu section. When not a VRChat Plus Supporter, this page will list the VRC+ benefits and features. When viewing as a currently-active VRChat Plus Supporter, this page will list details of the subscription.
* Added User Icon image to the Quick Menu. If you are a currently-active VRChat Plus Supporter, you can click the icon in the top right to take a new picture for your user icon. It will display your currently-chosen user icon.
* Added User Icon management page, where you can select from your previously-uploaded icons. There is a limit of 64 icons. You can disable your icon by selecting the "blank" icon, which is displayed as the first few letters of your name.
* Added UI to support taking an image in VRChat for your User Icon.
* Added "User Icon" report reason for users.
* Moved the "My Creations" row above the Favorites row in the Avatars menu.
* **VRChat Plus Benefit** - Added three additional favorite rows for avatars. These rows will display the number of avatars saved in that row, and show the number of avatars in that row.
* The Friend icon is no longer visible in Full mode when you're nearby. It will appear in Icon-only mode, and when you get far away from the nameplate. Friends are indicated by yellow names instead of the standard white color.
* Trust Rank is no longer visible on nameplates by default. Open your Quick Menu to see the Trust Rank of a user.
* Added User Icons to the Safety menu as a new category. If you choose to hide user icons for a specific rank, they will be obfuscated with a mosaic effect.
* Avatar Favorite Groups are now collapsed further while empty.
* Added VRCat to a bunch of places in the menu. They get lonely, give them a few clicks every so often!


## SDK


### Udon


* Fixed Strafe Speed in default World Prefab
* Fixed issue where example prefabs didn't have their programs attached
* Fixed issue where Set Variable nodes would reset their in-line values


# VRChat 2020.4.2p1


Release - 16 November 2020 - Build 1017


## Client


### Fixes


* Fixed an issue preventing the alpha transparency filters from working properly
* Fixed an issue preventing local test and local "fallback" avatars from working properly


# VRChat 2020.4.2


Release - 16 November 2020 - Build 1016


## Client


### Features


* When avatars are blocked due to not having an asset available, performance, or other reasons, **the "gray robot" should now scale down or up to the avatar's height**
	+ This scaling has upper and lower bounds-- as in, it will only grow/shrink to a certain point
* Added support for **Rich Presence in Discord and Steam!**
	+ Discord Rich Presence will display instance user count in your Discord status where appropriate, respecting your VRChat status and instance type
	+ You can send VRChat instance invites to users through Discord if you are in a Public or Friends+ instance. You can post an invite link to a Invite or Invite+ instance if you are the instance owner
	+ Steam Rich Presence will group Steam friends by instance, respecting status and instance type
	+ You can right-click Steam friends and "Join Game" when appropriate
	+ You can also right click friends on Steam and send them invites to your VRChat instance where appropriate. This needs testing, but should work!
	+ Rich Presence can be disabled entirely by adding the item `"disableRichPresence": true` to your [Configuration File](/docs/configuration-file)
* Added smoothed first-person camera mode for VR! Access it via your Camera menu. (Shout-out to RubberRoss for the suggestion!)
* Replaced the "spiral" filter on the camera with a "local user only" alpha filter, so the camera will only show you! (Shout-out to Drumsy and many others for the suggestion!)


### Changes


* Miscellaneous updates have been made to better support Quest 2
* A hardcoded particle limit for avatars has been enabled on Quest 1/2 to protect from malicious use. The settings match our recommended settings for the [Avatar Particle System Limits](/docs/avatar-particle-system-limits) system
* Favorite avatars that are not supported on your current platform can now be removed
* Some changes made to fix the FOV of screenshots taken in VR mode
* Removed some unnecessary logging that made it difficult to share output logs


### Fixes


* Fixes to local display of avatars that use jawflap
* Fixes to properly display pending friend requests in the social menu
* Fixed issues where root transform animations weren't working correctly with Valve Index hardware
* Fixes made to avatar cloning. The "Allow Cloning" setting should be much more reliable and fast to update now


## SDK3 - Worlds


### Udon


* Added support for various TextMeshPro hooks
* Added SetStrafeSpeed, GetStrafeSpeed


# VRChat 2020.4.1p5


Release - 4 November 2020 - Build 1010


## Client


### Fixes


* Fixed an issue causing users in full-body tracking to not sync their animations and other avatar properties correctly
* Fixed an issue causing full-body tracking users to cause crashes when sitting in a station
	+ Since the above issue has been fixed, we have re-enabled stations for FBT users


# VRChat 2020.4.1p4


Release - 30 October 2020 - Build 1008


## Client


### Fixes


* Minor adjustments have been made to prevent cases where VRChat would crash unexpectedly
* Stations will temporarily not be able to be entered while hip tracking or full-body tracking is in use


# VRChat 2020.4.1p3


Release - 30 October 2020 - Build 1007


## Client


### Fixes


* Fixed several issues related to undesired AV3 behavior such as repeating sounds, repeating animations
* Fixed an issue causing the run-time Avatars 3.0 FX layer replacement to be incorrectly blank
* Fixed an issue where newly created AV3 avatars did not have visemes appear in mirror properly sometimes
* This fix went out last night in a server-side patch, but we'll list it here anyways: Made changes to voice chat infrastructure that should stabilize connections between users


##### Known Issues


These are the major issues we've already got tracked-- it isn't all of them, but we put some of them here to ensure you know about it and that we're working on it.


* Interrupting an animation by changing avatars can cause problems
* Avatars that use jawflap movement for speaking are not visible locally, but still work remotely


### SDK3 - Avatars


Note regarding Write Defaults:  

Here's some clarifications on this change. Before 2020.4.1, the SDK's example controllers had the setting "Write Defaults" enabled. This causes a lot of problems with things like stations and consistency between Playable Layers. We made the decision to change the example controllers to have Write Defaults disabled. In short, **if your AV3 avatar has all of the slots for Playable Layers set to custom controllers, this change won't affect you.**


However, if you leave the Playable Layer in the "button" state where it says "Default LAYERNAME", then the controller is replaced at run-time. This means that they are replaced with a layer that has Write Defaults *off*. 


In short, if you want to have your avatar to have behavior that is durable through SDK and client changes, *it is best to fill in all the slots for Playable Layers*, even if you just use the SDK's example controllers provided in `VRCSDK\Examples3\Animation\Controllers`.


# VRChat 2020.4.1p2


Release - 29 October 2020 - Build 1006


# Client


## Changes


* Improved the latency of your voice to local visemes in mirrors, cameras, etc


## Fixes


* Additional fixes to voice that should help resolve cases where users can't hear each other
* Some more fixes for situations where users would stop receiving notifications and friend updates after some time


# VRChat 2020.4.1p1


Release - 28 October 2020 - Build 1005


## Client


### Fixes


* Tentative fix for issue where social menu/notifications stop receiving updates after a while
* Fix for friends not displaying in menu correctly when in "active" state (using VRChat website but not in-app)
* Fix for some cases where world info wasn't displayed correctly
* A variety of fixes made to voice processing that should fix cases where you can't hear another user that is speaking
* Tentative fix for still hearing users after blocking them
* Fixed issue where local visemes would be slow/delayed in some cases
* Fixes and improvements to IK, mostly in relation to crouching and auto-footsteps
* Fixed issues that would occur when joining a world while someone was in a station


## SDK3


* Fixed issue where AV3 Playable Layers would be offset by 1
* Fixed issue where AV3 avatar animation layers wouldn't work as expected


# VRChat 2020.4.1


Release - 27 October 2020 - Build 1004


## Client


### Features


* Major improvements to your Social menu! **Friend sync is live!**
	+ Friends and favorite friends lists should update instantly when your friends come online, change instances, and change status
	+ The "in-room" Social list should update much more quickly
	+ Fixed a few issues where users would not update information properly
* An "ear" icon will now appear on users in the "In Room" Social display when they are receiving your audio and can hear you


### Fixes


* Large amount of changes to improve performance and reduce overall CPU usage
* Users on slow connections will no longer see others in the wrong avatar if they swap while the avatar is still downloading


## SDK3 - Worlds


* [Cinemachine](https://unity.com/unity/features/editor/art-and-design/cinemachine) has been whitelisted in VRChat, allowing for unprecedented control over cameras in your world! Check out the [Unity feature page on Cinemachine](https://unity.com/unity/features/editor/art-and-design/cinemachine) for more details.
	+ Cinemachine components have been whitelisted for SDK3 worlds
	+ Added Udon control nodes for Cinemachine
* Stations have had a major rework for SDK3, including full compatibility with SDK3 avatars. Check our [VRC\_Station](/docs/vrc_station) documentation for more information


### Udon


* Added the [Player Audio](/docs/player-audio) system to Udon, allowing creators to adjust the voice and avatar audio of individual users with Udon!
	+ Udon can now control the Player Voice and Avatar Audio settings on individual players, like the audio override feature from SDK2
	+ This can be used to create stages with louder audio, audience areas with lowered audio range, microphones that boost your voice when held/nearby, and more!
* Node Graph: Simplified node names in search windows
* Node Graph: Split node names to two lines in graph
* `UdonBehaviour.enabled` and `Animator.enabled` exposed
* `UnityEngine.Rect` exposed
* `PlayableDirector.time` exposed. This enables sync and control for Timelines
* `VideoError` Udon Nodes added for easier handling of errors


## SDK3 - Avatars


* New animator parameters available for Avatars 3.0! Please see the Avatars 3.0 documentation on [Animator Parameters](/docs/animator-parameters) for more details
	+ [`TrackingType`](/docs/animator-parameters#trackingtype-parameter) - Returns a value depending on the tracking in use by the wearer
	+ `VRMode` - Returns `1` if the wearer is in VR, `0` if the user is in Desktop mode
	+ `MuteSelf` - Returns `true` if the wearer has muted their microphone, `false` if the wearer is not currently muted
	+ `InStation` - Returns a value depending on if the avatar is in a station or not
	+ `AvatarVersion` - Used for station animators. Returns a value depending on the version of the avatar worn by the user using the station.
* Example / default animators no longer use "Write Defaults" in their states. Read [our updated docs](/docs/avatars-30#write-defaults-on-states) for more info


## SDK2


* Stations have been adjusted to accommodate for AV3 avatars. New documentation is pending.
	+ Please note: This does not fix "dance world" stations as they currently operate. The method that these worlds use is not supported and is non-optimal. The new station setup allows this kind of behavior, but you may need documentation (which again, is pending!) to get this working. We appreciate your patience!


## SDK Fixes


* Fixed Unity Video Player not handling more than one audio track
* RTSP and RTSPT Video URL loading fixed


# VRChat 2020.3.3p2


Release - 1 October 2020 - Build 996


## Client


### Changes


* Soundcloud added to SDK3 URL whitelist, BunnyCDN and Cloudfront removed


### Fixes


* Various improvements to overall application and networking performance, including major improvements to the VRChat menus
* Fixed minor issue with loading local avatars


## SDK


### Fixes


* SDK2 / SDK3: OnPlayerJoin and OnPlayerLeave are no longer called twice
* SDK2: [VRC\_PlayerAudioOverride](/docs/vrc_playeraudiooverride) fixed


# VRChat 2020.3.3p1


Release - 25 September 2020 - Build 994


## Client


### Fixes


* SyncVideoStream should now auto-start properly
* Remote user camera lens will now show up in the proper location
* Avatars loaded from cache will now show their file size instead of 0MB
* Some fixes to missing avatar file size on download
* Fixed minor issue with loading local avatar files
* Fixes for head tracking and wand input for Vive Focus
* Fixed some networking problems on objects that are spawned as disabled
* Various changes and fixes to reduce unnecessary error messages in logs
* Fixed the program that enables VRChat launch links so it no longer appears each time VRChat is closed


## SDK3


* Editor Play mode filtering has been restricted to SDK3
* Added TextMeshPro and TextMeshProUGUI to set text via UI
* Added RTSP, RTMP, RTSPT to the allowed schemes for video player URLs
* Udon: Added error code to OnVideoError (InvalidURL, AccessDenied, PlayerError, RateLimited)


# VRChat 2020.3.3


Release - 18 September 2020 - Build 992


## Client


### Features


* Added video players to SDK3, **powered by Udon**!
	+ You can use our example Video Player for either the built-in Unity video player, or use AVPro to support live streams
	+ You can use our example method for syncing, or **build your own sync method**
	+ Check out the SDK3 section below for more details!
* **Added a button to the Settings menu called "Allowed Untrusted URLs"** which bypasses the site whitelist (see below) for SDK3 video players
	+ This will allow playback of a video hosted on any compatible source. The compatibility list is similar to SDK2
	+ In the future, we will be adding a pop-up user consent to access web sources. This is being done to make it easier to play videos and will be used for other future components like dynamic web images
* **Added a site whitelist for** ***SDK3 / Udon*** **video players.** If a video is requested and it is hosted on a site in the whitelist, it will play. **This does not affect SDK2 video players.**
	+ If a video is hosted on a site that is not on the whitelist, it will not play, unless "Allow Untrusted URLs" is checked in Settings
	+ With the example SDK3 video player, if the instance master has the whitelist on and a video is requested that is off-whitelist, it will not play
		- User-created video players may want to change sync ownership to whoever requested to video to avoid this issue
	+ [The service whitelist can be viewed in our documentation](/docs/www-whitelist). **This whitelist is temporary**, and will be removed at a later date when a pop-up user consent is implemented
* **Added the ability for desktop users to rotate objects while holding them!** While in Desktop mode, pick up an object, and:
	+ Press I / K to adjust pitch of the held object (rotate along X axis)
	+ Press J / L to adjust yaw of the held object (rotate along Y axis)
	+ Press U / O to adjust roll of the held object (rotate along Z axis)
	+ Roll the mouse wheel to move the object forward/back (translate along Z axis)


### Fixes


* Significant improvements and fixes to displayed text, including fallback behavior for unsupported characters
* Fixes made to portals, as well as general improvements to the world-join process
* The VRChat link installer now saves the VRChat executable path to the registry
* Fixed a bug affecting birth date entry during platform account (Steam, Oculus, Viveport) first-time login


## SDK3


* **Video players are now available in SDK3!** Check out our [Video Players](/docs/video-players) documentation for more information
* SDK3 no longer logs unnecessary warnings on Assembly Reload
* **Unity Timeline support!** (No Udon control yet, but we're working to add it soon)
* **Some UI events have been disabled and will no longer work properly.** To see the full list of accessible UI events, please see the [UI Events](/docs/ui-events) documentation. **This only affects SDK3 worlds.**
* Animation events are now being filtered. To see the full list of accessible animation events, please see the [Animation Events](/docs/animation-events) documentation. **This only affects SDK3 worlds.**


### Udon


We've added new nodes and events to handle player collision and haptic controller vibration! Momo has created a new video demoing both features and how to use them with an "Automatic Door" example.


# VRChat 2020.3.2p6


Release - 11 September 2020 - Build 986


## Client


This patch is Steam-only.


### Fixes


* Fixed an issue preventing Steam accounts from being able to log in for the first time


# VRChat 2020.3.2p5


Release - 1 September 2020 - Build 984


## Client


### Changes


* Added a configuration option to set your own cache directory. This is an advanced user feature intended to allow easily changing where your cache is stored. You can use this to assign your cache to another drive, if you wish!
	+ To set this, you need to create a file called `config.json` (also used for the [Avatar Particle Limits System](/docs/avatar-particle-system-limits) and [Avatar Dynamic Bone Limiter](/docs/avatar-dynamic-bone-limits) configuration)
	+ This file must sit in the `%AppData%\..\LocalLow\VRChat\vrchat` folder, and must be named `config.json`
	+ In this file, you'll need to set the option `cache_directory`
	+ If the directory does not exist, it will be created
	+ If you have a `config.json` already, add the `cache_directory` property at the root level of the configuration file and define it


### Fixes


* Fixed an issue preventing local testing of worlds from working properly
* Fixed an issue preventing the cache from being cleared properly
	+ To clear your cache, you will be prompted to restart VRChat. The cache will not clear until you do so
* Putting both thumbs up will now properly play the animation / set the animation state assigned to Thumbs Up
* Removed some error log spam when there were no eye bones assigned, but blink was enabled


# VRChat 2020.3.2p4


Release - 28 August 2020 - Build 982


### Features


* **We have changed the default bindings for Oculus Touch and Valve Index controllers.** Left and Right joystick click now has no action assigned. Access your Action Menu by long-pressing the Quick Menu button on either controller. Of course, you might want to change that, so...
* **We have added a "Bindings" button to the Settings menu!**


	+ When you click on this menu, you'll see the bindings for your current controller
	+ **Predefined Bindings:** If you are using the Oculus Touch or Valve Index, you will get some alternate controller binding "Types" you can select from
	+ **Custom Bindings:** You can also choose "Custom" and change the bindings and some other settings
	
	
		- On Oculus Touch, you can customize the A/X buttons and the joystick click-in on either hand
		- On Valve Index, you can customize the A buttons and the joystick click-in on either hand
		- You can assign the following actions: Gesture Toggle, Jump, Mute, Action Menu, None
		- "Use lighter grip for grabbing" only appears for Valve Index, and will reduce the grip "strength" required to grab and hold an object
		- "Hold Quick Menu for Action Menu" will enable or disable the ability to call up the Action Menu by holding down the Quick Menu button
	+ If you are on SteamVR, you can select the "SteamVR" binding type if you want to use SteamVR Input to customize your controls!
	
	
		- When using other controllers (including keyboard), you will get a graphic displaying the bindings and a message telling you that if you want to customize your bindings, you must use SteamVR controller configuration
	+ Not all controllers have binding graphic images. We're working on adding more for the future
* The HTC Vive Wand controller now has "hidden" bindings for Toggle Mute, Jump, and Gesture Toggle. This means you can customize these bindings and assign them via SteamVR controller configuration, if you wish
* **When opening the Action Menu on one hand, you can move around with the controls on your other hand!**


	+ A UI will appear on the other hand to assist with showing how to turn and move
	+ There is an option in the Action Menu Config section to disable this feature


### Changes


* Adjustments to IK to further improve behavior, including fixes to the "hip snap" issue
* "AFK Enabled" option in the Action Menu Config section renamed to "AFK Detection"
* Improvements to loading speeds and memory usage in some situations


### Fixes


* Fixed the "Zzz" emote missing from the Action Menu
* Fixed an issue where the analog fist gesture was "blending" when it should not have been (AV2 and AV3)
* Slightly relaxed height for desktop users to avoid standing on tiptoes
* Fixed an issue where squat/wide-stanced avatars would have strange leg/foot behavior


# VRChat 2020.3.2p3


Release - 14 August 2020 - Build 976


## Client


### Changes


#### Avatars / IK


* Avatars 2.0: Adjusted and tweaked AV2 behavior to more closely replicate pre-2020.3.2 behavior. This should solve many of the "knee-knock" and related issues. There may still be some differences-- we'll continue to tweak based on your feedback and our internal testing as time goes on and we release more patches


### Fixes


* Fixed an issue that was preventing analog trigger values being read on the Vive Wand controller
* Fixed an issue with the default Valve Index bindings that was preventing analog weight from the triggers from working properly. In order to use this, you must get the latest updated bindings in SteamVR


# VRChat 2020.3.2p2


Release -13 August 2020 - Build 974


Thank you for all the Avatar 3.0 feedback! We've been working on some refinements to the Action Menu and its controls. We've also included some IK updates and general bug fixes. Expect another patch early next week with the ability to bind controls and one-handed navigation-- check after the patch-notes for more info!




---


## Client


### Changes


* We have published default bindings for Valve Index, Oculus Touch, Windows Mixed Reality, and Vive Wands to the SteamVR platform. To use these, switch your controller binding to Default in SteamVR settings
* We've improved our world search technology to deliver more relevant results. We will continue to enhance search over the next few weeks


#### UI


* Emotes have been added back to the Quick Menu for AV2 avatars
* The Emote menu shows some additional dialog indicating that it has been moved when using an AV3 avatar
* Emote Menu has a button to quickly open the Action Menu


#### Action Menu


* Action Menu "root" has been named "Home", and has been simplified into Options, Expressions, and Emojis
* Close button removed from Action Menu Home
	+ To close the Action Menu, either press the Quick Menu button or your binding for Action Menu again
	+ This is to help simplify the UX of opening/closing the action menu and the "Home"
	+ This also makes it easier to close the Action Menu and open it back up where you left off
* Gesture Toggle moved to Options section. See the note at the end of the patchnotes regarding upcoming rebinding system
* Mic Mute added to Options section of Action Menu
* Puppet menus can now be exited with the Quick Menu button
* Added shortcut: Short-press the Quick Menu button to close the Action Menu
* Added tooltip to Action Menu to indicate that you can close it by pressing the Quick Menu (or "Menu") button. You can also close it by pressing your binding for Action Menu again
* Closing the Action Menu and re-opening it will open the page you previously had open
* Pressing down on the right Vive Wand touchpad no longer opens the Action Menu. Open the Action Menu on Vive by holding down the Quick Menu button


#### Avatars / IK


* Crouching and Prone in 3-point tracking should track the head much better. Leaving Crouch pose should leave the standing pose a bit nicer now (it was leaning forward a bit before, causing problems like standing on tip-toes and misaligned head during Seated Play)
* Full-Body Tracking should not track the head during locomotion to avoid leg dragging and other issues
* Improved sitting height measurement when swapping from Standing to Seated play
* Sped up playback and transition of jump landing


### Fixes


* Added missing emojis to Action Menu
* Fixed an issue where hands felt like they were slightly off-angle
* Sitting in a station now properly clears parameters `Grounded`, `VelocityX/Y/Z`, and `AngularY`


## SDK3


### SDK3 - Avatars


A new SDK3-Avatars package is available on the VRChat Home site. **Remember to perform an in-place upgrade per [the instructions in our documentation](/docs/updating-the-sdk).** Not doing so will result in the loss of avatar setup data!


* Various cleanups done to all example motion animations to improve and smooth blending and to implement fixes from the Client section into the example controllers
* Example animation controllers updated to account for various changes. If you based your controller off the example controllers, you'll have to rebuild your controller to get the benefit of the changes




---


We plan on releasing another patch within the next week that includes a simple method to choose between a few binding types or customize your bindings. Rebinding will be initially available for Oculus Touch and Valve Index controllers.


Using this, you should be able to bind **Gesture Toggle**, the **Action Menu**, **Mute**, and **Jump** to either lower button (A on Index, A/X on Oculus) or Joystick Click, or leave those buttons empty. Our default binding will not have actions on joystick click, and you will access your Action Menu via long-pressing the Quick Menu (or just "Menu") button. You can choose to customize this!


Of course, SteamVR users will still be able to customize their bindings via SteamVR, but will have to use a specific in-game binding to ensure no conflicts occur. 


In addition, we plan on providing a method to locomote using a one-handed locomotion mode when you have one Action Menu open.


We will provide more details on these features once we get closer to releasing the patch! Keep an eye on our [Discord](https://discord.gg/vrchat) for the most up-to-date information.


# VRChat 2020.3.2p1


Release - 7 August 2020 - Build 970


## Client


### Changes


* AV3 avatars that don't customize their avatar expressions will automatically be provided with the "standard" avatar emotes, assuming the avatar follows these conventions:
	+ All blend shapes are assumed to be on a Skinned Mesh named `Body`
	+ `eyes_closed` used in the `proxy_eyes_die`, `proxy_eyes_shut`, `proxy_eyes_open` animations
	+ The `proxy_eyes_die` animation is meant to be played simultaneously with the `proxy_die` animation for transforms (which is in the default Action layer)
	+ `mood_happy` `mood_surprised` `mood_sad` `mood_angry` are in a blend tree using the `VRCFaceBlendH` and `VRCFaceBlendV` parameters for a Two-Axis Puppet menu
* Added a new dedicated camera shutter sound when taking photos


### Fixes


* Fixed an issue where AV2 avatars using the female animation set were using the male set instead
* Fixed an issue where [VRC\_SpatialAudioSource](/docs/vrc_spatialaudiosource) was incorrectly being removed from avatars
* Debug menu now correctly reports Mouth and Jaw tracking state
* Fixed some issues with avatar file size display being incorrect
* Fixed an issue where some component types were missing from Avatar Performance Stats and Performance Rank calculation
* Fixed some issues with user view height encountered when using Seating/Standing toggle


## SDK3


### SDK3 - Worlds


* Made Build Callbacks work with Build & Test (Hi Merlin!)


# VRChat 2020.3.2


Release - 6 August 2020 - Build 968


## Client


### Features


* **We've released Avatars 3.0!** This is a whole new framework of avatar creation, intended to allow creators to make powerful new avatars that allow players to be expressive, control their avatars, and a ton more! Check out more info at our docs page: [What is Avatars 3.0?](/docs/what-is-avatars-30)
	+ If you want to learn how to make an Avatars 3.0 avatar, you've got a bunch of resources:
		- [Read this blog post!](https://medium.com/vrchat/introducing-avatars-3-0-c9d2de010177)
		- Check out our [documentation!](/docs/avatars-30)!
		- Check out our [Walkthrough series](https://ask.vrchat.com/t/av3-walkthrough-index/2148) on our Ask forums!
		- Log on to our [Discord](https://discord.gg/vrchat) and talk to other AV3 creators in the Avatars 3.0 category!
* Added an Avatar Download Size statistic to Avatar Performance Stats. This file size is the compressed package download size of the avatar package. It does not affect Performance Rank yet
* Added an Avatar Download Size Limit to the Performance Options. You can adjust the limit in the Safety > Performance Options window
	+ Clicking the arrows will increase/decrease the limit by 5MB at a time
	+ The limit is set to 200MB by default. Setting it to zero will disable the system
	+ This limit applies to all players, including your friends
	+ If an avatar exceeds this file size, it will not be downloaded, and the avatar will be replaced with a "Performance Blocked" placeholder
	+ If an avatar is filesize-blocked, you won't have the other Performance Stats, because you don't have the avatar downloaded
	+ You can override this limit on a per-player basis by using "Show Avatar"


### Changes


* **Large amount of changes and improvements for Full Body Tracking.** See the Full Body Tracking section below for full details
* Improved eyelook behavior for all avatars
* Upgraded to latest spatializer and lipsync libraries
* Portals now increment to hard-cap (2x capacity) instead of soft-cap
* Allow re-joining your own world (via clicking the text at the top of the Worlds menu) when the world is over soft-cap
* Adjusted default player limit in SDK from 8 to 16
* Enforce 48KHz application audio output setting to avoid some edge-case issues


### Fixes


* Fixed noisy feedback when switching avatars


### Ongoing


* Safety and Security fixes


### Known Issues


We plan on releasing patches soon to address these issues.


* Stations do not work on AV3 avatars just yet
* Download size is inaccurate for avatars that have already been downloaded
* Some (very important) emojis are missing from the Action Menu Emoji selector. All emojis are still accessible via the Quick Menu
* Performance stats menu is missing some readouts


## SDK 3


### Features / Changes


* Addition of [Avatars 3.0](/docs/what-is-avatars-30) to VRCSDK3
* ***SDK3 has been split into two packages***. There is now a version for Avatars and one for Worlds
	+ Upgrading your AV3 project will take some careful upgrading to avoid losing your state behaviors again. Told you they were fragile! We included instructions above the SDK links to help you migrate, so follow those.
	+ Both versions will be available for download on the site
	+ You can load both the Avatars and Worlds SDK into the same project, *but we do not recommend doing so*


## Full Body Tracking


* **Calibration has changed!** This affects both AV2 and AV3 avatars.
	+ **When calibrating, your avatar is attached to your HMD.** This *greatly* improves viewpoint replication even while laying down.
	+ ***Calibrate with your playspace zeroed out (not moved by OVRAS/Playspace Mover), and ensure your height is correct in your Settings menu.*** This is wildly important. If you calibrate with a zeroed out playspace and the proper height, you avoid a lot of issues.
	+ ... that being said, if you're having issues with your height being slightly off, this is because you weren't lying and you ACTUALLY ARE five foot, 11*-and-a-half* inches tall! You should calibrate first with zeroed playspace and proper height, then use something like OVR Advanced Settings to adjust your playspace height up or down. You shouldn't have to do this any more than 1/2 of an inch (~1.3cm) up or down.
	+ Here's some tips on how to calibrate using the new system:
		- Look down at your feet. Use either the tracking balls within VRChat or look down at your IRL feet to ensure you've got the same spacing as your avatar.
		- Remember that when you look back up, your avatar is going to shift a little forward-- so you should expect your feet trackballs to be a little farther forward than you'd expect.
		- Look straight forward, stand straight, and pull both triggers. Like before, putting your arms out in T-Pose is optional, but it can help with orientation.
		- Done!
	+ If you have issues of your instep not being in the correct position, the proper way to fix that is to adjust the T-Pose of your avatar. If you try to adjust it using another method, you may lose tracking fidelity because angles on your measurements will be incorrect.
	+ If you have issues where you're "on stilts", the proper way to fix this is to adjust the proportions of your avatar's rig. See our documentation on [Full-Body Tracking](/docs/full-body-tracking) for more info.
	+ If you prefer the old calibration method for some reason, use the `--legacy-fbt-calibrate` launch option. In Steam, you set this in the Properties for VRChat.
* Various tuning done to FBT to improve behavior. This affects both AV2 and AV3 avatars.
* **Added some additional options to the Avatar Descriptor** for AV3 avatars to assist with tuning behavior
	+ **"Use Auto Footstep"** is on by default. It only applies to 3-point or 4-point tracking. Turning it off means you're disabling the procedural lower body animation for room-scale movement.
		- This procedural animation is what plays when you move around in room-space while in 3 or 4-point tracking
		- Leaving "Auto Footsteps" on (which is the default state) will still allow you to enable/disable tracking via the Tracking Control state behavior
		- If "Use Footsteps" is off, enabling/disabling tracking on your legs and hips won't do anything, and you're relying on your animations to drive your lower body at all times.
	+ **"Force Locomotion Animations"** is on by default. It only applies to 6-point tracking (Full-Body Tracking).
		- When "Locomotion Animations" is on, locomoting in FBT (as in, moving your joysticks) will play a walking/running animation, as it does in Live currently.
		- When "Locomotion Animations" is off, locomoting in FBT will NOT play the walking/running animation. This is useful if you wish to "mime" your walking with your full-body tracking movement
		- **If you are turning off "Locomotion Animations", do not use the default Base and Additive layers.** You're expected to make your own!
* ***WARNING:*** Remember when I told you to stop using rig hacks last year? I'm telling you again. Stop it! If you have things like zero-length necks/hips, flipped hips, etc, **you are going to have major problems.**
	+ As a reminder, ensure you have your correct height specified in Settings, and ensure your playspace is both properly calibrated for your floor and zeroed-out (not moved by Playspace Mover or OpenVR Advanced Settings).
	+ ***All reports of FBT weirdness or issues will require that you replicate and test with a standard rig, reasonable proportions, correct height, and properly-calibrated playspace.***
	+ If you're confused about what a "rig hack" is and want to know how to set things up, check out our documentation on [FBT Rigging Requirements](/docs/full-body-tracking#rigging-requirements).


# VRChat 2020.3.1


Release - 16 July 2020 - Build 956


## Client


### Changes


* Performance improvements made to logging
* Small adjustment to in-app moderation messages
* AVPro is now disabled when using VRChat on Linux via SteamPlay/Proton
	+ This should enable fairly stable VRChat usage on Linux via Proton! We don't officially support Linux as a platform just yet, but we hope this will hold you over 🐧


### Fixes


* Fixed a local date format issue that caused issues when creating an account in countries with different date formats


### Ongoing


* Safety and security fixes


### Known Issues


* When spawning into a world, newly joining players will appear at world origin for a moment before teleporting to spawn


## SDK


### Features


* The SDK now checks to see if your avatar has been imported with incorrect blendshape normal import settings. If it is incorrect, it will prevent upload until you fix it. An "Auto Fix" button has been provided
	+ This is done to help mitigate an issue where users are mistakenly importing models with blendshape normals set to "calculate", which causes mesh sizes to be very large in both download size and in-memory size
	+ This check only runs on avatars. For worlds, you should ensure that any skinned meshes you're using are imported either using "Import" for blend shape normals, or you check on the "Legacy Blendshape Normals" option. If you don't, you are going to have inflated download/in-memory size!


## Udon


### Features


* A brand new Udon Node Graph! For a great overview, check out this [awesome video](https://youtu.be/IVjEx_H5BZc) by VRChat Developer MomoTheMonster
* Many additions in the new Udon Node Graph:
	+ Zoom
	+ Variables Window
	+ Groups
	+ Drag and Drop GameObjects, Components and Variables
	+ Search Improvements
	+ Comments improved
	+ Compiler Status Improvements
	+ Overall Styling
* New Udon Operator Nodes:


# VRChat 2020.2.3p1


Release - 18 June 2020 - Build 946


## Client


### Fixes


* Fixed: Camera does not take an image when holding and pulling trigger
* Fixed: Camera grab behavior regression
* Fixed: Udon Instantiation not working properly
* Fixed: Networked Udon events not firing properly


# VRChat 2020.2.3


Release - 17 June 2020 - Build 944


## Client


### Features


* Implemented an automatic update system for video helper binaries
	+ VRChat will check for updates to these files upon start. If a new version is detected, it will be downloaded and installed automatically
	+ This will permit much faster updates to these files, and allow us to fix video playback more quickly


### Changes


* General improvements to VRChat Udon performance at runtime
* Updated bundled content, lowering base installer size
* Quality of life changes to login flow


### Fixes


* Fixed: Avatar stations do not work unless enabled by an animator
* Fixed: Mic toggles on/off when pressing Ctrl-V
* Fixed: User voice issues when in moving stations
* Fixed: User voice does not emit from the head of the avatar in some situations


### Ongoing


* Safety and security fixes


### Known Issues


* When spawning into a world, newly joining players will appear at world origin for a moment before teleporting to spawn
* Camera does not take an image when holding camera object and pulling trigger


## VRCSDK3 + Udon and VRCSDK2


### Changes


* Udon: Added support for many more methods that use out parameters


### Fixes


* Fixed: When locally testing with multiple clients, clients will not be in the same instance
* Fixed: Inconsistent behavior with the execution of SDK2 broadcast events for late joiners
* Fixed: Inconsistent behaviour for Owner and Master SDK2 broadcast events
* Fixed: Various bugs with Animator Sync state syncing
* Fixed: Inconsistent behavior with SDK2 triggers on Object Instantiator template objects that are disabled at start and enabled after cloning
* Fixed: Unable to set components on existing struct types


# VRChat 2020.2.2p1


Release - 8 June 2020 - Build 933


## Client


### Changes


* Updated video helper binaries to fix an issue with playing Twitch streams


# VRChat 2020.2.2


Release - 28 May 2020 - Build 932


## Client


### Changes


* Updated Visual C++ Redistributable package requirement to 2019 on Steam and Oculus, which should help fix some voice and video player issues


### Fixes


* Fixed: Camera nameplate does not display as many characters as the user nameplate
* Fixed: Camera jitters when locomoting
* Fixed: Avatar moves away from stations/viewpoint when in a moving station


### Ongoing


* Safety and Security fixes


# VRChat 2020.2.1p1


Release - 15 May 2020 - Build 928


## Client


### Changes


* Updated video libraries
* Several miscellaneous reliability fixes to video libraries


### Fixes


* Fixed: [VRC\_SyncVideoStream](/docs/vrc_syncvideostream) does not support Mixer and some other sites that have warnings when attempting manual link resolution


### Ongoing


* Safety and Security fixes


# VRChat 2020.2.1


Release - 12 May 2020 - Build 926


## Client


### Features


* Replaced the "extender" button on the camera with a Lock button. This button locks the camera into player space (so it will move with you) and prevents it from being accidentally grabbed until the camera is unlocked


### Changes


* Improvements to mirror performance
* Improved station behavior, stabilized viewpoint position when moving in stations
* System specifications and application version are now logged in the output log


### Fixes


* Fixed: Camera lens indicator sometimes doesn't appear on/for other players
* Fixed: Nameplates are cutting off an extra character after 2020.1.1 update


### Ongoing


* Safety and Security fixes


## VRCSDK3 + Udon and VRCSDK2


* Improved visibility of platform compatibility in the Builder window
* Added a button to swap platforms in the Builder window
* Added information on current platform compatibility in the Builder window


# VRChat 2020.1.1p5


Release - 5 May 2020 - Build 924


## Client


### Fixes


* Fixed an issue causing world rows to be out of order unexpectedly
* Safety and security fixes


## VRCSDK3 + Udon


### Changes


* Unity Video Players have been removed from SDK3. Video Players present in SDK3 worlds will be removed on scene load in the VRChat client
	+ Video Players will be re-added with new supporting systems in an upcoming release


# VRChat 2020.1.1p3.2


Release - 30 Apr 2020 - Build 922


## Client


### Fixes


* General optimizations, changes, and fixes to improve the experience on Quest and greatly reduce crashes


# VRChat 2020.1.1p3


Release - 17 Apr 2020 - Build 920


## Client


### Fixes


* Fixed: Camera filters do not work
* Fixed: Connecting to VRChat fails with certain regional settings (often observed with systems set to Thai locale)
* Fixed: Render queue issues affecting in-world avatar when viewing an avatar in Avatar menu preview
* Fixed: Local mic volume slider does not work
* Improved behavior of [VRC\_SyncVideoPlayer](/docs/vrc_syncvideoplayer) and [VRC\_SyncVideoStream](/docs/vrc_syncvideostream) to improve/fix syncing behavior
* Improvements to Animator syncing
* Further fixes to reduce random crashing
* Safety and security fixes


## VRCSDK2


### Changes


* Added option "Lerp on Remote Client" to TeleportPlayer action. When checked, players that teleport will interpolate between their start and end position when viewed from a remote client. When unchecked, players that teleport will instantly appear at their new target location when viewed from a remote client.
* Added "Force Non-VR" option to local testing


## VRCSDK3 + Udon


### Changes


* Added bool `lerpOnRemote` to `VRCPlayerApi.teleportTo`. When true, players that teleport will interpolate between their start and end position when viewed from a remote client. When false, players that teleport will instantly appear at their new target location when viewed from a remote client.
* Added "Force Non-VR" option to local testing


### Fixes


* Fixed: `SendCustomNetworkEvent` does not work if there is more than one UdonBehaviour on an object
* Fixed: Some nodes cause compiler to fail consistently


# VRChat 2020.1.1p2


Release - 9 Apr 2020 - Build 918


## Client


### Fixes


* Fixed: Random, common crashes with no error or output log
* Fixed: Degraded avatar load speed and frame "hitches" while loading complex avatars
* Fixed: Private avatars/worlds cannot be removed from favorites list
* Fixed: Synced objects between PC and Quest do not work in some situations
* Fixed: Presentation Room not functioning properly
* Fixed: Various issues with sprite packing
* ... which means that the infamous "red dot" on the loading screen is no more! 🥳
* Fixed: Issue with setSyncType Trigger on `VRC_SyncVideoStream` players
* Fixed: Generic avatars do not animate remotely while locomoting
* Some tweaks made to reduce potential for crashes on Oculus Quest
* Networking values have been tweaked to improve the function of some pickups (such as drawing pen prefabs)
* Further networking tweaks to help with aligning player IK and trigger timing
* Some tweaks to memory management to improve usage on all platforms
* Video helper binaries updated
* Safety and security changes


### Known Issues


* Some users may experience problems connecting to VRChat with certain specific hardware or OS setups
* Using `vrchat://` launch links may cause issues with Oculus controllers while using SteamVR. Work around this by making sure SteamVR is running before using the launch link.


## SDK


### Fixes


* VRCSDK2: Fixed bug with teleport player and onAvatarHit resulting in odd behavior


### Changes


* Combined SDK3 Prefabs and Udon Examples into a new "VRChat Examples" folder in the root.
* Added a new Prefabs example scene with common World Settings (jump, run/walk speed), an avatar pedestal, and a mirror toggle button
* Some other updates and additions to SDK examples
* Udon can no longer access built-in Unity primitive meshes. If you need to access meshes directly, import your own copy as an FBX or other asset in your project
* Udon: Security improvements


# VRChat 2020.1.1p1


Release - 3 Apr 2020 - Build 916


## Client


### Fixes


* Fixed: Joining a hard-capped instance locks you in a black screen until client restart
* Fixed: Menu soft-locks when reporting content
* Fixed: Content rows turn invisible while scrolling when they have a large number of items
* Fixed: Hips not locked in place on stations/seats
* Fixed: VRC\_SyncVideoPlayer and VRC\_SyncVideoStream components do not work properly in some rooms


**If you have uploaded a new version of your world with the new SDK released with 2020.1.1 and it contains [VRC\_SyncVideoPlayer](/docs/vrc_syncvideoplayer) or [VRC\_SyncVideoStream](/docs/vrc_syncvideostream) components, you will need to follow these steps:**


1. Update your SDK from the [VRChat Home website](https://vrchat.com/home/download), following the steps given in [Updating the SDK](/docs/updating-the-sdk).
2. Open your world project and scene
3. For every component that is a SyncVideo **or** which has a Trigger that references one:  

Change any value in the component and then change it back to its previous value
4. Save your scene
5. Reupload


* Fixed: Users in Ask Me status get told to ask the instance owner to invite friends who request invites from them even though they can invite people directly
* Fixed: Issues with Battle Discs world
* Updated: Video helper binaries
* Various adjustments to networking to improve usage and behavior
* Various adjustments to reduce hitching and frame drops
* Safety / Security Fixes


### Known Issues


* Some users may experience problems connecting to VRChat with certain specific hardware or OS setups
* Some users may experience frame drops when opening the Quick Menu, selecting another user, and then moving their selection laser to other users
* Using `vrchat://` launch links may cause issues with Oculus controllers while using SteamVR. Work around this by making sure SteamVR is running before using the launch link.


## SDK


### Fixes


* Fixed: Misc Udon compiler issues


# VRChat 2020.1.1


Release - 1 Apr 2020 - Build 912


## Client


### Features


* **VRChat Udon**, a custom programming language just for VRChat, has been released into **Open Alpha**! Read more about Udon on our [Getting Started with Udon](/docs/getting-started-with-udon) doc page.
* **VRChat has moved to Unity 2018.4.20f1!** Please update your Editor accordingly
	+ If you require assistance migrating to the latest Unity LTS build, please see [Migrating from 2017 LTS to 2018 LTS](/docs/migrating-from-2017-lts-to-2018-lts)
	+ **Your content may require re-upload!** Please consult the [Migration Guide](/docs/migrating-from-2017-lts-to-2018-lts) to see what might trigger the need for a re-upload.
* **Some new features and changes to the Status system, [as described in our blog](https://medium.com/vrchat/upcoming-status-system-changes-ed7f824e96ff)**
	+ Added "Ask Me" status, which allows friends to request invites
	+ Renamed "Busy" to "Do Not Disturb". Do Not Disturb hides all invite requests
	+ "Do Not Disturb" and "Ask Me" statuses hide your location no matter what instance type you're in
	+ Status colors tweaked for readability and contrast
* **A new Networking and IK system!** This is an entirely revamped networking and IK system designed to improve fidelity while lowering bandwidth requirements and ping sensitivity. Read more about it on our [blog post](https://medium.com/vrchat/vrchat-unity-2018-networking-ik-udon-and-more-445688972335) regarding the 2018 update (scroll to the bottom)
* People that are closer to you should have smoother IK
* Improved remote drawing using avatar hands
* Improved remote painting in worlds like [Just Graffiti](https://vrchat.com/home/launch?worldId=wrld_96851736-d35a-46d6-8d17-da920a329537)
* People far away or that aren’t visible use less bandwidth so people closer and visible can use more
* Improved replication of pose, particularly in hand positioning
* Improved replication of pose during fast or quickly-changing movements for people that are nearby and in-view
* Designed to be tweakable and changeable while live, meaning we can adjust values to improve general behavior without having to issue a new client version
* Improved network performance of synced objects
* Increased performance overall
* Player voice chat now adjusts quality dynamically based on available bandwidth and other factors
* Added the following components to the SDK2 avatar whitelist, and the **SDK3** world whitelist. SDK2 worlds do NOT have access to these components.
	+ `AimConstraint`
	+ `LookAtConstraint`
	+ `ParentConstraint`
	+ `PositionConstraint`
	+ `RotationConstraint`
	+ `ScaleConstraint`
* Added `ParticleSystemForceField` to **SDK3** world whitelist. SDK2 worlds do NOT have access to this component.


### Changes


* **Post Processing Stack v1 has been removed by Unity.** If its scripts are present in a world, they will be removed. As a result, the world may look different until the author migrates to Post Processing v2
	+ It is expected that users migrate to Post Processing Stack v2, which is present in the Unity Package Manager
* There have been a few changes to the world component whitelist. See a full list in our [Whitelisted World Components](/docs/whitelisted-world-components) doc page. Depending on what SDK the world is built with, components from these packages are no longer supported and will be removed:
* Removed from all SDKs (including current worlds): Dynamic/Volumetric Fog and Mist, Post Processing v1
* Not supported in VRCSDK3: PhysSound, Realistic Eye Movements, Unity Standard Assets
* Updated Steam Networking to latest version to support relays, preventing user IP leaks
* Updated supporting libraries for SyncVideoStream player, which fixes YouTube Live Streaming
* Updated video helper binaries
* Some changes to Debug menu features
* Debug menu buttons are now disabled unless you run VRChat with `--enable-debug-gui`
* Added `--enable-udon-debug-logging` command line argument to enable Udon heap and stack dumps in the client. Usually only enabled in editor
* Added new network and event debug displays; debug keys 7 and 8; only available to the world author or in local testing worlds
* Removed AMD graphics card check, it is no longer required
* Various performance improvements to the menu
* Added `--enable-sdk-log-levels` which enables a large amount of SDK2 world logging for world creators
* Changes made to resolve some cases of excessive RAM usage
* Network performance enhancements across the board
* Multiple adjustments to logging, reducing spam
* Improvements to crash logging details
* Many memory leaks have been plugged up (but not all, we're still hunting)
* Work done to improve CPU usage in many situations
* Lots of small changes across the board to improve RPC and networking behavior
* Security: VRChat will now check to make sure that the youtube-dl binary shipped with VRChat is being used on startup. If a mismatch is detected, a warning is issued. We only support the use of the youtube-dl binary shipped with VRChat


### Fixes


* Fixed a bug where local lag would occur when hand gesture animations ran incorrectly
* Fixed a bug where gesture-based animations would sometimes not show properly in mirror
* Fixed some issues with avatar favorites
* Fixed some issues with avatars rigged as Generic not animating properly
* Fixed an issue on Oculus Quest where permissions dialog would appear at the wrong time
* Some tuning regarding how RAM is used and cleared when downloading asset bundles (like avatars)
* Fixed a long-standing issue that should greatly reduce or eliminate VRChat hanging when shut down
* Spurious delays in executing triggers are reduced
* Out-of-order issues with executing events are reduced
* Numerous bugs in ownership have been addressed


### Ongoing


* Safety and Security fixes
Updated 3 months ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [VRChat 2020.4.4p3](#vrchat-202044p3)
		- [Client](#client)
	+ [VRChat 2020.4.4p2](#vrchat-202044p2)
		- [Client](#client-1)
	+ [VRChat 2020.4.4p1](#vrchat-202044p1)
		- [Client](#client-2)
	+ [VRChat 2020.4.4](#vrchat-202044)
		- [Client](#client-3)
		- [Udon](#udon)
	+ [VRChat 2020.4.3p1](#vrchat-202043p1)
		- [Client](#client-4)
	+ [VRChat 2020.4.3](#vrchat-202043)
		- [Client](#client-5)
		- [SDK](#sdk)
	+ [VRChat 2020.4.2p1](#vrchat-202042p1)
		- [Client](#client-6)
	+ [VRChat 2020.4.2](#vrchat-202042)
		- [Client](#client-7)
		- [SDK3 - Worlds](#sdk3---worlds)
	+ [VRChat 2020.4.1p5](#vrchat-202041p5)
		- [Client](#client-8)
	+ [VRChat 2020.4.1p4](#vrchat-202041p4)
		- [Client](#client-9)
	+ [VRChat 2020.4.1p3](#vrchat-202041p3)
		- [Client](#client-10)
	+ [VRChat 2020.4.1p2](#vrchat-202041p2)
	+ [Client](#client-11)
		- [Changes](#changes-3)
		- [Fixes](#fixes-6)
	+ [VRChat 2020.4.1p1](#vrchat-202041p1)
		- [Client](#client-12)
		- [SDK3](#sdk3)
	+ [VRChat 2020.4.1](#vrchat-202041)
		- [Client](#client-13)
		- [SDK3 - Worlds](#sdk3---worlds-1)
		- [SDK3 - Avatars](#sdk3---avatars-1)
		- [SDK2](#sdk2)
		- [SDK Fixes](#sdk-fixes)
	+ [VRChat 2020.3.3p2](#vrchat-202033p2)
		- [Client](#client-14)
		- [SDK](#sdk-1)
	+ [VRChat 2020.3.3p1](#vrchat-202033p1)
		- [Client](#client-15)
		- [SDK3](#sdk3-1)
	+ [VRChat 2020.3.3](#vrchat-202033)
		- [Client](#client-16)
		- [SDK3](#sdk3-2)
	+ [VRChat 2020.3.2p6](#vrchat-202032p6)
		- [Client](#client-17)
	+ [VRChat 2020.3.2p5](#vrchat-202032p5)
		- [Client](#client-18)
	+ [VRChat 2020.3.2p4](#vrchat-202032p4)
	+ [VRChat 2020.3.2p3](#vrchat-202032p3)
		- [Client](#client-19)
	+ [VRChat 2020.3.2p2](#vrchat-202032p2)
		- [Client](#client-20)
		- [SDK3](#sdk3-3)
	+ [VRChat 2020.3.2p1](#vrchat-202032p1)
		- [Client](#client-21)
		- [SDK3](#sdk3-4)
	+ [VRChat 2020.3.2](#vrchat-202032)
		- [Client](#client-22)
		- [SDK 3](#sdk-3)
		- [Full Body Tracking](#full-body-tracking)
	+ [VRChat 2020.3.1](#vrchat-202031)
		- [Client](#client-23)
		- [SDK](#sdk-2)
		- [Udon](#udon-5)
	+ [VRChat 2020.2.3p1](#vrchat-202023p1)
		- [Client](#client-24)
	+ [VRChat 2020.2.3](#vrchat-202023)
		- [Client](#client-25)
		- [VRCSDK3 + Udon and VRCSDK2](#vrcsdk3--udon-and-vrcsdk2)
	+ [VRChat 2020.2.2p1](#vrchat-202022p1)
		- [Client](#client-26)
	+ [VRChat 2020.2.2](#vrchat-202022)
		- [Client](#client-27)
	+ [VRChat 2020.2.1p1](#vrchat-202021p1)
		- [Client](#client-28)
	+ [VRChat 2020.2.1](#vrchat-202021)
		- [Client](#client-29)
		- [VRCSDK3 + Udon and VRCSDK2](#vrcsdk3--udon-and-vrcsdk2-1)
	+ [VRChat 2020.1.1p5](#vrchat-202011p5)
		- [Client](#client-30)
		- [VRCSDK3 + Udon](#vrcsdk3--udon)
	+ [VRChat 2020.1.1p3.2](#vrchat-202011p32)
		- [Client](#client-31)
	+ [VRChat 2020.1.1p3](#vrchat-202011p3)
		- [Client](#client-32)
		- [VRCSDK2](#vrcsdk2)
		- [VRCSDK3 + Udon](#vrcsdk3--udon-1)
	+ [VRChat 2020.1.1p2](#vrchat-202011p2)
		- [Client](#client-33)
		- [SDK](#sdk-4)
	+ [VRChat 2020.1.1p1](#vrchat-202011p1)
		- [Client](#client-34)
		- [SDK](#sdk-5)
	+ [VRChat 2020.1.1](#vrchat-202011)
		- [Client](#client-35)
