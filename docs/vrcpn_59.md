# Latest Release - VRChat 2022.2.1

Release - 25 May 2022 - Build 1201

[Suggest Edits](/edit/latest-release)**Introducing VRChat IK 2.0!** We've completely revamped the IK system, improving every aspect of tracking in VRChat.


This update includes a **huge** upgrade for our IK system that's been in a compatible-with-Live beta for a long time. Thanks to the amazing feedback from our Full Body Tracking community, we've managed to fine-tune our IK system into a best-in-class tracking system. **Everyone benefits from these changes**, not just full-body tracking users!


Learn more about the IK 2.0 update in the [documentation page](/docs/ik-20-features-and-options) we set up for it! We've also updated the [Full-Body Tracking](/docs/full-body-tracking) doc page to get it up to date with the new system. You can also just watch this video.



In addition, we've made tons of other improvements along the way, including **doubling the amount of avatar parameter space available**, increasing the sync rate of avatar parameters for desktop users, a significant boost to PhysBones performance, big improvements to our input system (that should help us net that vaunted "Steam Deck Verified" checkmark, c'mon Gabe!), and more! 



> ### 🚧Configuring your Height with IK 2.0
> 
> **If you had previously set a "User Real Height" that differs from your actual real-life height, please enter your actual height before giving feedback or submitting bug reports!** 
> 
> If you have issues with scaling, we recommend using the Avatar Measurement toggle to measure by avatar height for a perfect fit. Alternatively, it's possible to set a custom scale with the `--custom-arm-ratio=` [launch option](/docs/launch-options) (more details below).
> 
> 


# Client


## Features


* Added support for **up to 11 points of tracking!**
	+ The newly supported tracking points are: **chest, knees, and upper arms**
	+ Chest tracking will twist the chest based on your tracker's rotation
	+ However, when you use the "lock all" IK option, the chest will use both tracker rotation and position
	+ For upper arms, a single tracker simultaneously controls the elbow and shoulder. **To use shoulder tracking, you must wear your tracker above your elbow!**
* Implemented **Per-tracker IK combinations!** It's now possible to mix and match most combinations of tracker locations!
	+ For example, if you have only two trackers and would like to track just your elbows without your lower body, that's now possible
	+ Asymmetric tracking is also supported: with just a single tracker you could track just your left foot if you choose
	+ Asymmetric combinations such as just your right foot and just your left elbow are possible
	+ If a tracker disconnects or is turned off, the per-tracker IK will readjust to mix and match tracking and IK for whichever trackers are still available
	+ If that tracker is later powered on again, tracking will be restored with the previous calibration intact (even if this happens after switching avatars!)
* Users without elbow tracking (including non-full-body PC and Quest users) can enjoy **automatic prevention of elbows clipping** through the avatar's torso.
* Full body users have **new configuration options for FBT in the QM settings tab.**
	+ **Lock-hip option**: This option prioritizes hip tracking, allowing the head to drift slightly to avoid odd neck or spine crunching.
	+ **Lock-head option**: This option prioritizes head tracking *ensuring no view-point drift*, but allowing the hip to drift slightly to avoid odd neck or spine crunching.
	+ **Lock-all option**: This option strictly enforces both head and hip tracking. If the trackers get close together the spine will bend in any way necessary to have both align simultaneously. Depending on your avatar's rig, this might cause odd posture. This option works best with a chest tracker
* Added a toggle to measure avatar scale by either arm-span or by height. The default is to measure by arms, switching this to measure by height can give an improved fit for avatars in full body
* A legacy IK toggle is available in the quick menu to restore old IK solving behavior. This does not revert calibration and tracker changes. Eventually this legacy toggle may be removed.
* **Implemented Calibration saving!**
	+ **After calibrating once, your calibration is saved for all avatars**
	+ When switching to a new avatar, the calibrated set of trackers is proportionally remapped to that avatar and you do not have to calibrate again
	+ In general, you should be able to calibrate a single time per session, and switch avatars endlessly!
* **Full body users will now start up in 3pt (head and hands) IK rather than stuck in a TPose**
* **Calibration now ignores trackers unreasonably far from the body during calibration**
	+ In other words, it's possible to have trackers powered on without them being forced into the VRChat calibration process
	+ Calibration now ignores trackers located precisely at coordinates (0,0,0) to prevent binding to some trackers that will appear there in SteamVR when powered on but not tracking
* To enable full body, users must manually press the calibrate button in the quick menu to start the calibration processes
* The AV3 TrackingType parameter will now update depending on per-tracker-ik status. For now this still only uses the old 6-point system and the goal is keeping compatibility with existing custom animators. When both feet are tracked, TrackingType will be 6. If one or more foot is not tracked, but a chest or hip tracker is active, TrackingType will be 4. Otherwise TrackingType will be 3. (There are no changes to the rare cases that can still cause TrackingType to be 0, 1, or 2. See [https://docs.vrchat.com/docs/animator-parameters#trackingtype-parameter](/docs/animator-parameters#trackingtype-parameter) for details on those situations)
* Added a bunch of launch options for customization of IK 2.0 features. These launch options may later be integrated into the UI, but for now we've added them here
	+ **`--custom-arm-ratio="0.4537"`** - Adjusts the ratio used to scale the avatar when using measure-by-arms mode. "0.4537" is default, smaller values around "0.415" may give improved fit.
	+ **`--disable-shoulder-tracking`** - Use this to avoid issues with some types of IMU-only based arm trackers
	+ **`--enable-ik-debug-logging`** - Adds additional output to the log regarding IK. Use this when reporting bugs or issues with IK
	+ **`--calibration-range="0.6"`** - Determines the distance from predicted supported binding points that the calibration will search (in meters). The default value defines a `0.6` meter (`60` cm) sphere. This applies to feet, thighs, hip, upper arms, and chest trackers
	+ **`--freeze-tracking-on-disconnect`** - Enabling this will cause trackers to freeze in place relative to the player when they are disconnected. To remove frozen trackers you can calibrate again. If all your trackers have disconnected so the calibration option is no longer visible, cycling the Avatar Measurement option will also unfreeze them
* **Significant adjustments and improvements have been made to input in VRChat!**
	+ Gamepad, keyboard and mouse input now goes through the Unity Input System
	+ Gamepad input has been brought up to feature parity with Keyboard and Mouse
	+ Action Menu Support has been added for Gamepads
	+ Implemented a new mapping scheme for Gamepads
	+ Thumbstick vertical look is no longer affected by framerate
	+ Implemented virtual, stick-controlled mouse cursor to navigate menus
	+ Implemented support for the "Player Select" system
	+ Implemented support for various controller schemes (PS3, PS4, PS5, Switch Pro, Xbox, Steam Controller, Steam Deck and more!)
	+ Tooltip icon prompts are now based on the button mapped to that action and based on which controller is connected
	+ Implemented object rotation using middle-click followed by mouse movement
	+ Implemented the Steam Deck on-screen keyboard in menus that require typing


## Changes, Improvements, and Fixes


* PhysBones have received a **significant performance improvement!**
* **Max avatar parameter memory space has been doubled from 128 to 256 bits!**
* Avatar Parameters are now updated in Desktop Mode as quickly as they are in VR
* Various fixes and improvements to internal memory management processes
* Fixed issues with upper body positional desync on some setups in FBT
* Added/refined support for upper-chest humanoid bone in FBT
* Fixed calibration binding causing tilted angles at the hips on some rigs in FBT
* Fixed issues with chest rotation when the user lies down in FBT
* Fixed issues with chest rotation when the user spins quickly in FBT
* Fixed issues with chest rotation when the user turns upside-down in FBT
* Avatar Dynamics: Fixed an issue where the left and right foot was swapped in avatar setup
* Fixed an issue where tracker binding would shuffle between different trackers when a tracker loses connection
* Default base standing animations in full-body tracking no longer cause odd toe bending when crouching
* Improved anatomical modeling of shoulder bone motion. Avatars with long shoulder bones should now look much better than previously
* Reaching beyond the avatar's arm length no longer causes the torso to be pulled to rotate or lean towards the hands
* Users will no longer lose tracking when opening the SteamVR overlay
* Improved Force Rejoin behavior after waking Steam Deck from sleep mode
* Fixed an issue where the Quick Menu button to add the current world to a Playlist wasn't working properly
* Fixed an issue where PhysBones would vibrate unintentionally due to issues with high framerates


# SDK


## Changes, Improvements, and Fixes


* **Max avatar parameter memory space has been doubled from 128 to 256 bits!** So good we listed it twice.
* OSC debug console has been doubled to match the increase to 256 bits
* Added height back to the PhysBone Collider Capsule shape type
* Fixed a NullReferenceException related to serialization
* Fixed object and player grouping not working as intended, along with some improvements
* Fixed SyncPhysics issues with syncing Gravity / Kinematic and coming out of sleep
* Significantly reduced the amount of allocations in Udon Sync
* Arrays having entries change no longer cause an OnVariableChanged event
* Array references are no longer invalidated on Sync
* Fixed sync errors caused by cloning scene UdonBehaviours using Instantiate. Cloned UdonBehaviours are now forced to None sync


# Documentation


* Added the [IK 2.0 Features and Options](/docs/ik-20-features-and-options) page
* Updated the [Full-Body Tracking](/docs/full-body-tracking) page
* `--disable-friendsync` removed from the [Launch Options](/docs/launch-options) documentation. Its functionality was removed with the UI 1.5 update but was not documented
Updated 4 days ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Features](#features)
		- [Changes, Improvements, and Fixes](#changes-improvements-and-fixes)
	+ [SDK](#sdk)
		- [Changes, Improvements, and Fixes](#changes-improvements-and-fixes-1)
	+ [Documentation](#documentation)
