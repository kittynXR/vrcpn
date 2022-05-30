# VRChat 2021.1.4

Release - 10 March 2021 - Build 1061

[Suggest Edits](/edit/vrchat-202114)# Client


## Changes, Improvements, and Fixes


* Made changes that should reduce the number of logins required when using 2FA in both the client and the SDK
* Made changes that should reduce voice issues that occur specifically in very high population instances of worlds that use large amounts of sync bandwidth
* Various improvements to internal UI systems
* Adjustment to the "Grounded" layer calculation
* Reduced pano capture noise volume
* Pickups with `pickupable` disabled will no longer block the interact laser
* Misc improvements to the way favorites are loaded
* Safety and security fixes


# Udon


## Features


* **Udon Midi Support**! Read more here: [Midi in Udon](/docs/midi)
* **New Event-Based Input System**! Read more here: [Udon Input Events](/docs/input-events). Here's how much simpler handling input is now:


![All the noodles on the left handle getting input for a jump. Then again, so does the economical bowl on the right!](https://files.readme.io/78750e3-i_view64_2021-03-10_12-14-18.png "i_view64_2021-03-10_12-14-18.png")![All the noodles on the left handle getting input for a jump. Then again, so does the economical bowl on the right!](https://files.readme.io/78750e3-i_view64_2021-03-10_12-14-18.png "Click to close...")All the noodles on the left handle getting input for a jump. Then again, so does the economical bowl on the right!


## Changes, Improvements, and Fixes


* Udon Support for AnimationCurves and Gradients
* Udon OnRespawn Event
* Udon Graph: performance improvement for Groups
* Udon Graph Search: new subcategories for less-used items
* Udon now has static Array methods: Copy, Clear, Reverse, BinarySearch and more


# SDK / Library Updates


* The client's version of Post Processing has been updated to 3.0.3.
* The client's version of AVProVideo has been updated to 2.0.7 Enterprise.\*
* The client's version of ONSP has been updated to the latest version.


\*Note: Existing worlds that use AVPro *directly* (as in, AVPro was imported into the world project to add components) will break with this update. These worlds will need to be reuploaded with the updated version of AVPro.

Updated about 1 year ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Changes, Improvements, and Fixes](#changes-improvements-and-fixes)
	+ [Udon](#udon)
		- [Features](#features)
		- [Changes, Improvements, and Fixes](#changes-improvements-and-fixes-1)
	+ [SDK / Library Updates](#sdk--library-updates)
