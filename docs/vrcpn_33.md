# VRChat 2021.3.4

Release - 15 September 2021 - Build 1132

[Suggest Edits](/edit/vrchat-202134)**This update brings the new and improved [Avatar Fallback System](/docs/avatar-fallback-system)!** Seeing an avatar that exceeds your [Minimum Displayed Performance Rank](/docs/vrchat-configuration-window#minimum-displayed-performance-rank) no longer results in a gray robot, but instead a customizable Fallback avatar. As before, you can choose from many of our default avatars for your Fallback, or you can upload your own custom Fallback avatar.


Check out the details of the improved [Avatar Fallback System here](/docs/avatar-fallback-system)! 


You could also just watch this very good video:



# Client


## Features


* Fallback Avatars now work for both the "Platform Missing" and "Performance Blocked" cases, for all platforms! See more details in the [Avatar Fallback System](/docs/avatar-fallback-system) guide


## Improvements


* **Updated VRChat to Unity 2019.4.30f1.** This upgrade is minor, and is aimed at addressing some known issues; *content uploaded on 2019 does not need to be updated.*
	+ This Unity upgrade fixes some issues, namely a VRAM bug with Realtime GI as well as the "Unity crashes with multiple monitors with different scaling values" issue
	+ **As usual, you can get the correct version on our [Currently Supported Unity Version](/docs/current-unity-version) page.** Install the new Unity version and open your projects using it, the migration doesn't require any further steps
* **Station sync has been rewritten** to fix a myriad of bugs and make them more reliable overall
* **You can now view Fallback Author and Fallback Performance Rank**
* **Fallback state can be seen in user name plates** when in "Full View" (Quick Menu open)
	+ New Blue Feather icons are used to indicate fallback state
	+ This icon will indicate many states, including "Performance Blocked", "File Size Blocked", "Error", "Loading", and "Manually Blocked"
	+ All of the new states are listed in the [Avatar Fallback System](/docs/avatar-fallback-system) section of the documentation
* [New config file option](/docs/configuration-file#first-person-steadycam-fov) that allows you to customize field-of-view of the first-person Steadycam option


## Fixes


* Fixed login issues for people with Oculus subs on non-Oculus versions of VRChat
* Fallback avatars can no longer be cloned
* Fixed an issue where certain WMR headsets would have incorrect camera clipping values due to large changes in clipping ranges between world changes


# Udon


## Improvements


* Added "None" sync to Udon. This can be used for any UdonBehaviors that do not need to sync, reducing overall data use


## Fixes


* Fixed OnAnimatorIK not firing on UdonBehaviours
Updated 9 months ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Features](#features)
		- [Improvements](#improvements)
		- [Fixes](#fixes)
	+ [Udon](#udon)
		- [Improvements](#improvements-1)
		- [Fixes](#fixes-1)
