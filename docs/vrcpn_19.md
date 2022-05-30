# VRChat 2021.2.2

Release - 17 May 2021 - Build 1095

[Suggest Edits](/edit/vrchat-202122)This is the *Udon Networking Update*! Don't let the name fool you, this long-awaited release isn't just about improving networking for Udon. As you'll see in the notes below, "UNU" is a massive improvement to many systems in VRChat that rely on networking, and an overhaul to many of our networking systems.


This update contains a huge amount of "under the hood" changes to improve networking behavior and add some long-awaited features to Udon. As such, it might not seem very flashy in terms of new user-facing features, but rest assured that our Udon-savvy creator community will quickly show off what they've been working on during the UNU testing period.


# Client


## Changes, Fixes, and Improvements


* **Generally speaking, networking has been improved in all situations and there will likely be many bugs that are now fixed that we're not listing here!**
* Synced objects (as in, objects that transmit their position over the network) should be smoother in all situations
* Portal entry is now more reliable, especially when moving fast or when your framerate is low. Hopefully, this means a lot less "back up and try again" when you're trying to go through a portal in a busy instance
* The "network voice bug" where all voice and IK for users in VERY busy instances would freeze/degrade badly *should occur much less!* We haven't seen it recur during mass tests during Open Beta, so fingers crossed!


# SDK & Udon


* Array variables can be synced! Check out the new [Networking docs](/docs/udon-networking) for more info on supported array types
* New Manual Sync Mode for UdonBehaviours for precise control of when variables are serialized
	+ Each manually-synced object is rate limited as a factor of the data size. The more it sends, the more its send rate is limited
* Most bugs that caused `OnOwnershipTransferred` to fire too often or at not the right times have been fixed. The event will now happen when it should
* New VRCObjectSync component instead of Sync property on UdonBehaviours if you just need to sync Transform & Rigidbody. Allows you to temporarily disable interpolation on an object, and properly set the Gravity and Kinematic properties on a synced physics object
* "Ownership Transfer On Collision" will behave better and no longer cause excess network traffic
* New `OnOwnershipRequest` event. This event gets sent when someone tries to take ownership, and by setting a return value it allows you to deny the transfer if you want to keep it
* Improved the reliability of syncing who the owner of an object is. Everyone should always agree on who the owner is, even in edge cases like late joiners having the object disabled or multiple people fighting over ownership
* `Networking.SetOwner` now works immediately - you can update variables immediately after changing ownership and the changes will apply properly
* Join-In-Progress issues fixed, you should no longer have issues with variables not being Deserialized for Players who join the world after they are changed
* New VRCObjectPool for managing collections of objects, including automatically managing their active states. Use this instead of Instantiation when you want a lot of networked objects
* New Debugging tools for seeing info about networked objects in your world, including the current owner, the data being used, and state information
* Fixed bugs that caused various variable types to not sync properly. Byte, Short, Uint and more can now be synced. See the [Networking docs](/docs/udon-networking) for more info
* Added `Networking.isClogged` which will tell you if outbound traffic is currently under heavy load
Updated about 1 year ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Changes, Fixes, and Improvements](#changes-fixes-and-improvements)
	+ [SDK & Udon](#sdk--udon)
