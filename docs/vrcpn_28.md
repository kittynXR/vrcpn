# VRChat 2021.3.2

Release - 4 August 2021 - Build 1121

[Suggest Edits](/edit/vrchat-202132)This is the VRChat Unity 2019 upgrade release! **We're moving to Unity 2019.4.29f1!**


We have been testing this version internally for months, and our Open Beta lasted for weeks! It has been very stable throughout our testing, and existing content has transitioned well with the upgrade. However (*and we cannot stress this enough*), **this doesn't mean that all content will transition smoothly!** 


That being said, in most cases where you see odd issues with content, upgrading your project to 2019 and re-uploading the content should solve most issues.


Check out our [Migrating from 2018 LTS to 2019 LTS](/docs/migrating-from-2018-lts-to-2019-lts) guide to see how to upgrade your projects. It's pretty painless this time around!


As such, aside from the upgrade to Unity 2019, there aren't many new features. We're keeping things minimal so we can find issues without having to worry about it being a bug with a new system instead of the upgrade.



> ### ❗️Hey, Content Creators!
> 
> It is **VITAL** that you read the [Migrating from 2018 LTS to 2019 LTS](/docs/migrating-from-2018-lts-to-2019-lts) documentation. DO NOT SKIP IT. Read it entirely and completely before upgrading your projects.
> 
> Failing to do so may result in damage to your projects. Back up everything.
> 
> 


# Client


## Changes, Improvements, and Fixes


* **Updated VRChat to Unity 2019.4.29f1!**
	+ Check out our [Migrating from 2018 LTS to 2019 LTS](/docs/migrating-from-2018-lts-to-2019-lts) guide to see how to upgrade your projects. **BACK UP YOUR PROJECT BEFORE UPGRADING.**
	+ See the page for [Currently Supported Unity Version](/docs/current-unity-version) to get the links for downloading Unity 2019.4.29f1
* Upgraded Cinemachine (2.8.0), PostProcessing (3.1.1), and TextMeshPro (2.1.6)
* Made changes to keyboard input that make intended keypresses use keys in the same location, regardless of locale or input system. You no longer need to switch to QWERTY to use VRChat
* The keybinds for debug menus should now be usable on foreign keyboard layouts
* Updated some loading screen graphics and added a few new ones
* Added in-app setting to change between graphics quality presets, available under the Advanced Performance Settings
* Fixed Right Shift activating safe mode
* Added logic to keep avatars from loading twice within 3 seconds


# SDK


* ***[Please consult with the "Migrating from 2018 LTS to 2019 LTS documentation](/docs/migrating-from-2018-lts-to-2019-lts)*** to learn how to upgrade your projects
* SDK2, SDK3-Avatars, and SDK3-Worlds now works with Unity 2019.4.29f1
* New "[Build & Reload](/docs/using-build-test#build--reload)" option in the SDK Control Panel for easily reloading open clients into new builds
* Added SDK check and auto-fix for cases where Mesh Read/Write is disabled
* Adjusted quality settings to match the VRChat application
* Made adjustments to increase SDK upload speeds


## Udon


* New `TrackingData.Origin` type in `VRCPlayerApi.GetTrackingData` to get a player's tracking space origin
* Udon can now sync `String` arrays and `VRCUrl` arrays
* Const nodes with multiple fields will now render correctly (`Vector3`, `Quaternion`, etc.)
* Constructor nodes will now list their type along with the label "Constructor" instead of "ctor"
* Calls to `SetVariable` with `sendChange` turned on will now actually become `SetProgramVariable` calls under the hood so that both methods of triggering `OnVariableChange` events work the same now. Fixes an issue where the 'old' variable value was incorrect on first access, and an issue where value types were never copied over
* Comments are editable again
* Fixes display of nodes where you could no longer see outputs (`GetTrackingData`, `SendCustomEvent`, others)
* Fixes issue where `VRCUrl` always reported it was different when serialized (would always fire `OnVariableChanged` for a synced `VRCUrl` even when it wasn't changed)
* Variables will no longer always have `_1` appended to them
* Includes new UdonSyncPlayer graph using `OnVariableChanged` instead of `OnDeserialization`, and drastically simplifying the logic. Should use less bandwidth as well
Updated 10 months ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Changes, Improvements, and Fixes](#changes-improvements-and-fixes)
	+ [SDK](#sdk)
		- [Udon](#udon)
