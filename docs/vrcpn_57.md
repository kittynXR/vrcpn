# VRChat 2022.2.1p2

Release - 26 May 2022 - Build 1203

[Suggest Edits](/edit/vrchat-202221p2)# Client


## Changes, Fixes, and Improvements


* Fixed an issue where attempting to join a world past soft-cap via the QM wings would result in an incorrect "this world is full to capacity" message
* Fixed further issues related to Favorites
* Fixed an issue where users could clone someone else even if cloning was off by performing a sequence of UI interactions


# Udon


## Changes, Fixes, and Improvements


* Fixed an issue where sync would break when an object had both continuous and object sync UdonBehaviours on the object


# SDK


## Changes, Fixes, and Improvements


* **Important change:** We fixed a bug preventing you from animating the position of a PhysBone's root or multi-child parent. Please note that to animate those bones, it is now required to have `isAnimated` enabled
* Avatar Dynamics gizmos should now move along with animations in play mode (assuming `isAnimated` is enabled)
* Fixed an issue where PhysBones "resisted" animation even when `isAnimated` was enabled
* Burst and Math packages are now imported for World projects


## Known Issues


* Animated PhysBones are jittery, it is a known bug and will be fixed in a patch in the coming week
Updated 2 days ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Changes, Fixes, and Improvements](#changes-fixes-and-improvements)
	+ [Udon](#udon)
		- [Changes, Fixes, and Improvements](#changes-fixes-and-improvements-1)
	+ [SDK](#sdk)
		- [Changes, Fixes, and Improvements](#changes-fixes-and-improvements-2)
		- [Known Issues](#known-issues)
