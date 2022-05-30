# VRChat 2021.3.1

Release - 8 July 2021 - Build 1113

[Suggest Edits](/edit/vrchat-202131)# Client


## Changes, Fixes, and Improvements


* **Significant improvements to networking behavior.** In particular, **this should fix issues where people experience "choppy IK"** after remaining in an instance for some time
* Fixed: Video players in SDK3 worlds would experience audio / video desyncing after experiencing hitches
* Fixed: "Allow Avatar Cloning" setting may be out-of-sync between users
* Fixed: Holoport cursor would appear on launch until any other input was received
* Fixed: Users can be unintentionally kicked from worlds with specific world configurations
* Fixed a bug with unfavoriting worlds (we're aware of the avatar favorites problems!)
* Fixed some crashes related to unloading content
* Fixed jump not working with Holoport
* Upgraded AVPro to 2.1.5
* Improvements to reduce hitching
* Improvements to avatar unloading


# Udon


* The new video player sync is **disabled by default**! The SDK will prompt you and let you know you should enable it. This is done because the new sync method will have issues if you resync too much (as in, multiple times per second). You really shouldn't be syncing very often. A check every few seconds should be sufficient.
* Added dropdown menus to `SetProgramVariable`, `SendCustomEvent`, `GetProgramVariable` and their variations. You can now see a list of target variables and events if the node references a valid UdonBehavior


![](https://files.readme.io/7b9f34d-image_5.png "image (5).png")![](https://files.readme.io/7b9f34d-image_5.png "Click to close...")
* The "Set Variable" node now has a `sendChange` checkbox, which will trigger an `OnVariableChanged` event for that variable if it's been checked.
* [Added `OnVariableChanged` Event Node](/docs/special-nodes#on-variable-changed) which provides the new and old values of the variable when it is changed via `SetProgramVariable` or `SetVariable` with `sendChange` turned on. This change also works for synced variables! **Access this event in the Node Graph by holding down the Alt key and dragging a variable onto the graph.**
* Changed behavior to reload graph after renaming or deleting a variable
* Added `PostLateUpdate`, an event that will happen near the end of the frame after IK has been calculated. Getting bone positions at this time will give you the most up to date positions so that they are not a frame behind
* Updated `UdonExampleScene` to use `OnVariableChange` events instead of `OnDeserialization` wherever possible.
* Fixed Udon crashing with a NullReferenceException when checking destroyed instances of classes that inherit from `UnityEngine.Object` for `null`. Thank you to Merlin for the help!
* Moved expensive UdonBehaviour events to components: `OnAnimatorMove`, `OnCollisionStay`, `OnTriggerStay`, `OnRenderObject` and `OnWillRenderObject` will only be called if your program uses them. Thanks to Merlin for the initial work on this!
Updated 11 months ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Changes, Fixes, and Improvements](#changes-fixes-and-improvements)
	+ [Udon](#udon)
