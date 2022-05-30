# VRChat 2022.1.1

Release - 24 February 2022 - Build 1169

[Suggest Edits](/edit/vrchat-202211)# Client


## Features


* **OSC API for Avatars!**
	+ You can now set up Open Sound Control to change parameters on your avatar and read parameters from your avatar-- both input and output!
	+ You can use this to implement your own eye tracking, face tracking, make changes to your avatars based on external inputs, and more!
	+ This is a pretty technical subject! Check out our [blog post](https://hello.vrchat.com/blog/vrchat-osc-for-avatars) to read more and see some examples.
	+ You can also check out our documentation here for more details on how to use this system: [OSC Avatar Parameters](/docs/osc-avatar-parameters)
	+ We've also added a [debug menu for OSC](/docs/osc-debugging) to help with development!
	+ OSC API for Avatars is is available for VRChat on both PC and Quest! You'll just need to point your OSC application at your Quest's IP using the default ports.
* **OSC API for Input!**
	+ You can also use the same system to provide input into VRChat! Many of our controls are mapped to OSC channels
	+ You can use this to map your own controllers, peripherals, and more!
	+ More details are provided in the [OSC as Input Controller](/docs/osc-as-input-controller) docs and [blog](https://hello.vrchat.com/blog/vrchat-osc-for-avatars)
	+ OSC API for Input is also available for VRChat on both PC and Quest!
* Added a **"tunneling" VR movement comfort feature** that optionally adds a vignette effect during movement
	+ Has "Light" and "Strong" settings, adjustable in the Quick Menu


## Changes, Improvements, and Fixes


* **Added the `Voice` parameter for usage on avatars!** This parameter is the avatar wearer's microphone amplitude in a float value from 0.0 to 1.0
* Added a "View Profile" button to friend request notifications
* Fixed an issue where the Upper Chest bone was not being networked properly, which could cause desynced poses when it was mapped (especially for full body users)
* Fixed an issue where some friends would be stuck "Online" after they'd logged off
* Greatly reduced spurious logging to the output log to improve performance. Re-enable these logs (and some new ones) by using the new `--enable-verbose-logging` launch option
* EXPERIMENTAL: Added the `--enable-avpro-in-proton` launch option, which will allow Proton users to re-enable AVPro for video playback. This may cause crashes!
* Fixed an issue where closing the Stream camera would open the Photo camera
* Fixed an issue where the VRChat UI could react when the mouse cursor was not over the window
* A variety of fixes to address application crashes in certain circumstances
* Various internal networking adjustments and updates


## Notes for Creators


Here's some useful links to participate in the OSC development community! Since this is a pretty developer-centric feature (at least, at first), we're going to handle these slightly differently.  

Discussions: <https://github.com/vrchat-community/osc/discussions>  

Bugs & Feature Requests: <https://github.com/vrchat-community/osc/issues>  

Milestones: <https://github.com/vrchat-community/osc/milestones>


# Udon


## Features


* Added `VRCPlayerAPI.Respawn` node with optional spawn index


## Changes, Improvements, and Fixes


* Udon synced objects are now less likely to rubber-band when transferring ownership


# SDK


## Features


* Allow other tools to define methods for `SendCustomNetworkEvent`, `SetKinematic`, and `SetGravity` for use in the Editor
Updated 3 months ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Features](#features)
		- [Changes, Improvements, and Fixes](#changes-improvements-and-fixes)
		- [Notes for Creators](#notes-for-creators)
	+ [Udon](#udon)
		- [Features](#features-1)
		- [Changes, Improvements, and Fixes](#changes-improvements-and-fixes-1)
	+ [SDK](#sdk)
		- [Features](#features-2)
