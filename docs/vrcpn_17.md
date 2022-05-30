# VRChat 2021.2.1

Release - 3 May 2021 - Build 1088

[Suggest Edits](/edit/vrchat-202121)# Client


## Changes and Improvements


* Various performance improvements to internal systems
	+ In particular, changes made to improve to avatar loading speeds and reduce hitching
* Adjusted FPS display font to be monospaced so it is easier to read
* The "VRChat Launcher Installer" helper program that launches when VRChat closes has been improved!
	+ You'll be re-prompted once with this update. Accepting the changes will be necessary to fix a previous launch protocol bug
	+ Now includes more accurate messaging depending on the current state of the helper
	+ No longer pops up when not needed
	+ After accepting the helper program's install, the Launch button on world links will work once more


## Fixes


* Less/no more players appearing at 0,0,0 for others during spawn
* Fixed several issues with the "fade to black" used during world changes
* Lots of various fixes to avatar initialization
* Locomotion settings are now properly saved and restored upon changing input controllers
* General improvements and adjustments to the management of voice decode tasks
* Fixed some cases of "popping" voice (not the current "pop-and-restore" bug)


## Known Issues


* While in Full Body Tracking, pressing Calibrate and then immediately opening up the SteamVR menu (or similar system overlay menu) will cause problems.
	+ If you're not using legacy calibration, you'll have visible tracking points/controllers until you complete a valid Calibration.
	+ If you're using legacy calibration, you'll be stuck in place and have visible tracking points/controllers until you complete a valid Calibration.
* When loading into an AV3 avatar, the `TrackingType` [parameter](/docs/animator-parameters) is unexpectedly set to `2` for 1-2 frames. This will cause any avatar controllers that are built with "dead-ends" to have issues. "Dead-ends" are branches of the animator that don't have a way to exit based on `TrackingType` changing after the initial avatar load.
	+ You can also avoid this by not making transitions based off `TrackingType` being `2`, but you really should also avoid building in dead-ends!


## Major Documentation Changes


Documentation has been added to [Animator Parameters](/docs/animator-parameters) to indicate that avatar authors should **never** "dead-end" animator branches based off parameters, otherwise undocumented or unintentional behavior may result. Animators should be designed with the expectation that any parameter value may change.


The section on the [`TrackingType`](/docs/animator-parameters#trackingtype-parameter) animator parameter has been expanded with a better explanation of how to design animators to account for value changes.


# Udon


* Exposed the rest of the AVPro audio channels
* Exposed `IsInstanceOwner` for `Network` and `VRCPlayerAPI`


## Udon Node Graph


* Major speed increases, especially with groups and large graphs
* Compiles much less often
* Fixed issue where you couldn't use all the ports after switching overloads (like a Quaternion with a single input or three inputs)
* Pasted nodes are now also brought to the front of the graph


# SDK2


* Both video players will now log who added a video URL and what that URL was to the output log
Updated about 1 year ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Changes and Improvements](#changes-and-improvements)
		- [Fixes](#fixes)
		- [Known Issues](#known-issues)
		- [Major Documentation Changes](#major-documentation-changes)
	+ [Udon](#udon)
		- [Udon Node Graph](#udon-node-graph)
	+ [SDK2](#sdk2)
