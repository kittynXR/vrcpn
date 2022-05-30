# VRChat 2021.1.5

Release - 23 March 2021 - Build 1067

[Suggest Edits](/edit/vrchat-202115)We posted a blog post along with this release! Please check it out [here](https://medium.com/vrchat/vrchat-on-quest-avatar-performance-woes-1a3cc228a442). It goes into detail regarding the Quest Performance Rank changes as well as the Avatar Fallback system.


# Client


## Features


![](https://files.readme.io/6991239-Fallback_v4.1f2p5.png "Fallback_v4.1f2p5.png")![](https://files.readme.io/6991239-Fallback_v4.1f2p5.png "Click to close...")
* Introducing **Fallback Avatars!** If you're on PC hanging out with a Quest player, you can now choose a Fallback avatar.
	+ This Fallback avatar will be displayed instead of the standard "gray robot" that you usually see when looking at a PC-only avatar on the Quest.
	+ You can either choose from a selection of the Featured Public avatars as your fallback, or upload your own Quest-compatible Fallback (as long as it meets the requirements)
	+ If the avatar you're wearing already has a Quest version, there are no changes
	+ Everyone's been assigned a random Fallback avatar to start, but you can change it freely
	+ Read more in our [Avatar Fallback System](/docs/avatar-fallback-system) docs! There's a FAQ in there, so if you have questions, they'll probably be answered there
* Added **Streamer Mode** as an option in the Settings menu! Streamer Mode is intended to keep you safe while streaming or recording and prevent unwanted content from appearing in multiple places in the UI.
	+ Enable Streamer Mode in your Settings menu!
	+ New friend requests and friend requests received in the 5 minutes before activating Streamer Mode are automatically declined. You can still send friend requests to others. ***Don't forget to turn Streamer Mode off once you're done since it blocks friend requests!***
	+ The Quick Menu's display of your current instance and display name is hidden, and the bottom banner indicates the mode's activation
	+ Your display name is hidden in social and player details, the Quick Menu, on your own nameplate, on portals, and during login
	+ Instance information is hidden in the Worlds menu and on portals
	+ Custom status messages on all users are hidden
	+ Notification photos are hidden
	+ Avatar thumbnails on other users are hidden in the Social menu
	+ *Streamer Mode does not indicate to anyone else that you are streaming*, it only hides information in your own view for your own safety.
	+ *Streamer Mode does not hide your name from Udon*, so it might still be visible in worlds that use your name to display on game boards, occupant displays, etc. Just be aware!


## Changes


* The polygon counts for the Quest [Avatar Performance Ranks](/docs/avatar-performance-ranking-system#quest-limits) have been adjusted as part of the effort to reduce the number of "gray robots" on Quest.
	+ **The maximum polygon count for Quest avatars before they are marked as Very Poor is now 20,000 polygons.** Avatars that are ranked as Very Poor still must be shown by clicking "Show Avatar".
	+ The polygon count for other ranks have been adjusted accordingly:
		- Excellent: Polygon count less than or equal to 7500 (increased by 2,500)
		- Good: Polygon count less than or equal to 10,000 (increased by 5,000)
		- Medium: Polygon count less than or equal to 15,000 (increased by 7,500)
		- Poor: Polygon count less than or equal to 20,000 (increased by 10,000)
	+ These changes were made after benchmarking new hardware, and to make creating avatars for Quest more accessible. Check out our blog post linked at the top of these release notes for more info.
	+ ... For those who have been around for a bit, creating an avatar under 20,000 polygons might sound pretty familiar!


![](https://files.readme.io/6efa76d-Polygon_Perf_Ranks_thinking.png "Polygon Perf Ranks_thinking.png")![](https://files.readme.io/6efa76d-Polygon_Perf_Ranks_thinking.png "Click to close...")
* FinalIK has been removed from the Quest avatar whitelist
* Moved the Full Body Tracking calibration indicators ("tracker balls") to the Player layer, so that mirrors that only show players still show them
* Updated font used at the bottom of the QM


## Fixes


* Safety and security changes and fixes
* Changed the behavior on Steam overlay opening-- your resolution is no longer halved. This is an attempt at a work-around for the long-standing Steam overlay "11 FPS" issue
* Fixed issue where users could get stuck in stations remotely
* Potential fix for display issues with favorite friends lists
* Fixed issue where social menu would stop updating properly after having the client open for a while
* Fixed some cases where checking for VRChat Plus status would fail
* Fixed a few issues where avatar favorite count would display improperly for users in various subscription states
* Various fixes to make user online/offline detection more reliable in social menus


# Udon


## Additions


* Added `SendCustomEventDelayedSeconds` and `SendCustomEventDelayedFrames`. These allow you to schedule a custom event to be run X seconds or frames in the future (Note: The minimum delay is the next frame)


## Changes and Fixes


* Made `SendCustomNetworkEvent` work in editor
* Node Graph: Tweaked the search UI to be a bit wider
* Fixed a NullReferenceException that occurred when leaving worlds containing UdonBehaviours that did not have a program


# SDK


* Fixed an issue when using the VRCSDK Platform Switcher to swap to Android. The Single Pass Stereo setting would not be toggled on properly and would cause new uploads to display improperly
Updated about 1 year ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Features](#features)
		- [Changes](#changes)
		- [Fixes](#fixes)
	+ [Udon](#udon)
		- [Additions](#additions)
		- [Changes and Fixes](#changes-and-fixes)
	+ [SDK](#sdk)
