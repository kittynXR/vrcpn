# VRChat 2022.1.2

Release - 21 April 2022 - Build 1189

[Suggest Edits](/edit/vrchat-202212)# Client


**Introducing [Avatar Dynamics](/docs/avatar-dynamics)!** This is a whole new category of systems that adds interactive features to VRChat avatars. 


**Check out our [blog post](https://hello.vrchat.com/blog/avatar-dynamics-live) first!**



> ### 🚧Important SDK Note: Hey, Shader Authors!
> 
> The previous version of the VRCSDK compiled shader variants for Mono and Single-Pass Stereo. Further upgrades to Unity require variants for Single-Pass Stereo Instanced, which aren't currently compiled and don't exist for uploaded content. From now on, the SDK will also compile variants for SPS-I to make future upgrades easier/possible. This is not the only measure being taken to help with future upgrades, but is still an important step.
> 
> **Creators:** UPDATE YOUR SDK. It is very important that you update your SDK to account for this change, otherwise future Unity engine version upgrades *will* break your content. The sooner, the better.
> 
> Additionally, if you want to preserve the shaders on your older avatars as well as possible, you should reupload them at some point in the future.
> 
> If you see shader errors after building content in the SDK now, it's because you're using shaders that don't properly support SPS-I. The content will still function correctly in VRChat if those errors appear, but please reach out to shader authors to make sure these errors are fixed!
> 
> **Shader Authors:** Please refer to this [Unity documentation page](https://docs.unity3d.com/Manual/SinglePassInstancing.html) for instructions on properly supporting SPS-I. **Please do this** ***as soon as possible*** **and encourage your users to upgrade to fixed shader versions.** Any content built without SPS-I support will not work properly in future Unity versions.
> 
> One specific fix is worth mentioning, `_CameraDepthTexture` must use `UNITY_DECLARE_DEPTH_TEXTURE(_CameraDepthTexture);` instead of `sampler2D`.
> 
> 


## Features


* **Implemented [PhysBones](/docs/physbones)!** PhysBones is a component that allows secondary movement for a more realistic depiction of things like hair and tails! [Check the docs](/docs/physbones) for technical details and important implementation notes!
	+ *This system is available on all platforms--* **yes, including the Quest!!** We managed to get PhysBones working on Quest with some limits. See those limits in the [Avatar Performance Ranking System](/docs/avatar-performance-ranking-system#quest-limits) docs
	+ You can set up PhysBones to be grabbed, pulled, stretched, and posed!
	+ You can interact with other people's PhysBones, letting you push around and pose affected bones. Want to give your friend a new hairdo? Easy!
	+ You can set up custom **[PhysBones](/docs/physbones) colliders** for various different effects!
	+ We've defined default finger and hand colliders for **all avatars**, listed in our [PhysBones](/docs/physbones) docs, so you've always got a way to interact with PhysBones
	+ We've integrated a UI to customize these predefined colliders on your avatar descriptor, so you can turn off ones you don't want at avatar creation time
	+ You can use [PhysBones](/docs/physbones) to affect [Animator Parameters](/docs/animator-parameters) on your avatar, so you can detect when someone is grabbing, pulling, or posing one of your PhysBones!
	+ PhysBones are **highly performant**, offering orders-of-magnitude better performance than Dynamic Bones
* **Implemented [Contacts](/docs/contacts)!** Contacts allow you to define volumes of space that will send or receive signals. These signals can then be used to drive [Animator Parameters](/docs/animator-parameters) on your avatar!
	+ This system is available on **all platforms-- yes, including the Quest!!**
	+ Contact Senders **send** a signal. For a successful collision to occur, both the sender and receiver need at least one matching pair of strings. Collision tags are case sensitive.
	+ Contact Receivers **receive** a signal. As noted above, both the sender and receiver need at least one matching pair of strings.
* Implemented **Avatar Dynamics Permissions**! The [Permissions and Settings](/docs/permissions-and-settings) interface allows you to select who can interact with your Avatar Dynamics systems on your avatar-- nobody, your friend, or everyone! **Permission must be granted by both users** for interaction to be enabled
	+ By default, only Friends can interact with your avatar
	+ A new icon will appear on users' nameplates to indicate the state of interaction permissions
	+ If the hand is lit up, interactions are enabled!
	+ If the hand is not lit up, interactions are not enabled
* Implemented a **runtime auto-converter for Dynamic Bones to PhysBones!**
	+ Best attempts are made to convert Dynamic Bones to PhysBones, including Bone and Collider components
	+ The methods, variables, and mathematics are different between the two systems, so conversion may not work perfectly for all avatars. Some complicated setups may require that the avatar author re-upload a new version
	+ This system is *enabled by default.* You can disable this system via the [VRChat Performance Options](/docs/vrchat-configuration-window) window. When the system is disabled, you will no longer locally be running the DB->PB converter and Dynamic Bones will be running-- in other words, this choice is local
* **Per-User Avatar Dynamics permissions!**
	+ The Avatar Dynamics button has replaced the Emoji button in the launchpad. It pauses all AD interactions now instead of cycling through global settings
	+ Added an interaction play / pause button in the Quick Menu settings
	+ Added per-user controls to the Quick Menu when selecting a user to override global setting. It is a three-way toggle, similar to the Show Avatar control


## Changes, Improvements, and Fixes


* Favorites have been fully refactored under-the-hood to be more responsive and stable. This should hopefully solve most (if not all) of the Favorites bugs we've seen!
* Improvements to simulation time, which should improve networking behavior overall and fix a handful of edge-case networking-related bugs
* Input is less dependent on framerate
* If an avatar has defined a VRChat built-in parameter, an error will be printed to log and the avatar's definition of that parameter will be ignored
* If an avatar re-defines an already-defined parameter, an error is printed to log and only the first definition is used
* Added a new button to the Quick Menu dashboard for setting Avatar Interaction, replacing the Emotes button
* Added callouts in the Quick Menu to Interactions Settings
* Fixed issue where some Main Menu thumbnail lists (ex. World Favorites) wouldn't show all results
* Safety and Security fixes


## Notes for Creators


* PhysBones acts a bit differently than Dynamic Bones. As such, we've provided some usage tips on the [PhysBones](/docs/physbones) documentation page, please refer to it!
* In order to use Avatar Dynamics, you must update your SDK!
* Avatar Dynamics systems are only available in SDK3.


# SDK


The SDK now requires that the Burst and Mathematics packages are installed. If they aren't installed, the SDK will install them for you on import. This may result in errors during first installation, but they will go away after a restart or a log clear.


## Features


* Avatar Dynamics components implemented
	+ [VRC\_PhysBone](/docs/physbones) and colliders, [Contact](/docs/contacts) senders and receivers
	+ **An example avatar is available in the SDK: `VRCSDK\Examples3\Dynamics\Robot Avatar`**
* Implemented some additional controls and settings on the Avatar Descriptor for Avatar Dynamics
* Implemented auto-conversion for Dynamic Bones to PhysBones, offered on the Build screen if Dynamic Bones are detected on the avatar
* **DB to PB Conversion was added to Unity menu.** `VRChat SDK/Utilities/Convert DynamicBones to PhysBones`. You must select the avatar for this to work
* Implemented warnings and errors for performance regarding Avatar Dynamics systems.
	+ If the [Very Poor limits](/docs/avatar-performance-ranking-system#quest-limits) are exceeded when building a Quest Avatar, the SDK will warn you that the components will not work when in VRChat


## Fixes & Improvements


* Enabled Single Pass Stereo Instanced compilation for all shaders at build-time
* Avatar parameters are checked for validity before creating the array of parameters
* Fixed SPS-I rendering for built-in Mobile-ToonLit shader


# Legacy SDK2


SDK2 is considered deprecated and legacy. It will only receive occasional maintenance updates, and will no longer be available or permitted for use in the future. Please migrate to the latest VRChat SDK as soon as you can.


## Improvements


* Enabled Single Pass Stereo Instanced compilation for all shaders at build-time


# Documentation


## Changes


* [Avatar Performance Ranking System](/docs/avatar-performance-ranking-system) page has been updated with limits for PhysBones and Contacts on PC and Quest. It has also been updated to note the hard cap on Quest Avatar Dynamics components
* All VRChat-provided prefabs are now described on the [SDK Prefabs](/docs/sdk-prefabs) page, and the Prefabs category has been removed
* Many unused, unpublished, and deprecated doc pages were removed
* Archived patch notes from 2017, 2018, 2019, and 2020 have been collapsed into single pages
* Improved the clarity of [the note regarding Write Defaults](/docs/avatars-30#write-defaults-on-states) in the Avatars documentation
Updated 17 days ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Features](#features)
		- [Changes, Improvements, and Fixes](#changes-improvements-and-fixes)
		- [Notes for Creators](#notes-for-creators)
	+ [SDK](#sdk)
		- [Features](#features-1)
		- [Fixes & Improvements](#fixes--improvements)
	+ [Legacy SDK2](#legacy-sdk2)
		- [Improvements](#improvements)
	+ [Documentation](#documentation)
		- [Changes](#changes)
