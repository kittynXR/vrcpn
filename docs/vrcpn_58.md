# VRChat 2022.2.1p1

Release - 25 May 2022 - Build 1202

[Suggest Edits](/edit/vrchat-202221p1)# Client


## Changes, Fixes, and Improvements


* Fixed an issue causing URLs in some video player implementations to not properly sync, resulting in broken players
* Fixed an issue where the message lists shown for invite responses could be incorrect


# Udon


## Changes, Fixes, and Improvements


* Objects instantiated via Udon's instantiate function will now inherit the original's `localRotation` and `localPosition`
	+ In [build 1201](/docs/vrchat-202221) clones were set to inherit the original's `rotation` and `position`, but this was both undocumented and inconsistent with Unity's instantiation behavior
	+ This new behavior imitates Unity instantiation behavior for consistency, [refer to their documentation for details](https://docs.unity3d.com/2019.4/Documentation/ScriptReference/Object.Instantiate.html)
	+ This is a change from previous behavior so we expect some rare cases where creators were relying on undocumented behavior to break
Updated 3 days ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Changes, Fixes, and Improvements](#changes-fixes-and-improvements)
	+ [Udon](#udon)
		- [Changes, Fixes, and Improvements](#changes-fixes-and-improvements-1)
