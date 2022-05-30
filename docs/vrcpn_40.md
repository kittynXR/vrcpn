# VRChat 2021.4.2

Release - 1 December 2021 - Build 1156

[Suggest Edits](/edit/vrchat-202142)This is VRChat 2021.4.2, the **"UI 1.5.1, VRC+ Gifting, Quest Camera, and US East Regions" update!**


As you might've guessed from the name, there's a bunch in here! This release focuses on a few things.


First off, **we've done a bunch of polishing to the UI 1.5 update.** You'll notice a lot of work to the new Quick Menu, mostly in regards to fixing bugs, adjusting annoyances, and other stuff. We've also slipped in some fixes to the Camera while we were in there. This release was always planned to be the "Hey, our community's had a bit to test stuff out, let's tweak things based on what they said." So, here we are! We're doin' it!


Next, **we've introduced VRChat Plus Gifting!** Available only on Steam for now, you can now send a non-recurring gift of a month or a year of VRChat Plus to your friends! Open your Quick Menu, click your friend, then click "Gift VRC+". 🎅 We plan on getting this working on Oculus as soon as we can, hopefully before the holidays. Fingers crossed! 🤞


Oh, right. We promised to put the Camera on Quest in this update, right? Done! **The VRChat Camera can now be used on the Oculus Quest!** Open it up using the Camera tab 📷 in the Quick Menu. Tip for Real Professional Gamers: Click the Camera tab twice to quick-spawn the camera. 🤯


**We've also introduced the US East region!** We've got new servers running in Virginia, USA, which not only should help people living in that area with a bit of improved voice and IK latency, but also allow NA and EU bridge the Atlantic gap a little bit more reasonably! You can choose to create a new instance in the US East region the same way you'd choose to create an EU or JP region instance.


There's also some new FBT menu options, and some new rich presence with the Meta/Oculus Quest, and camera fixes and... uh... okay, **there's a LOT in this update.** Kitchen-sink style. Fixes, improvements, changes, all that jam. I could go on and on, but really, you should just read our patch notes. Which you were going to do *anyways*, right? 🙃


# Client


## Features


* **Added VRChat Plus gifting!** Click on a user, click "Gift VRC+", and spread the love!
	+ For now, only Steam users can purchase, but **any VRChat user can receive a gift**
	+ Users with an active subscription cannot receive a VRChat Plus gift
	+ Gifts can be a 1 Month VRChat Plus credit, or a 1 Year VRChat Plus credit. They do not recur
	+ Working on bringing gifting to Oculus soon!
* **Added the Camera to VRChat on Quest!**
	+ Unfortunately, due to performance issues, the "depth of field" focusing effect is not available
	+ Images are saved in the Quest's Pictures folder under VRChat, and can be accessed via the Quest's OS. They can also be accessed via connecting your Quest to your PC and looking under the `Pictures/VRChat` folder
* **Added the US East region!**
	+ Added a text indicator on portals to differentiate between US East and US West
* **We've added support for a variety of Oculus/Meta Quest social features!**
	+ There is now an expanded Rich Presence system on Oculus/Meta Quest
	+ Users in VRChat can send invites to Oculus/Meta Quest friends that are online but not in VRChat


## Improvements


* **Added Full Body Tracking settings section to the Quick Menu!**
	+ This menu allows you to adjust your user height, recalibrate quickly, and **disable/re-enable Full Body Tracking** with a button press 🎉🎆🎇🍾
* **The VRChat UI is now rendered such that it will no longer be affected by avatar or world shaders, post processing, or other effects!**
	+ 👩‍💻 Creators: We used one of our reserved layers (`reserved2`, layer 19) as part of this change. The SDK will reflect this in a future release. Just FYI!
* Added a new safety / debug feature: **If you hold down both Quick Menu buttons for the duration of loading a world, your avatar will be reset upon load-in!** Hold down the buttons until your avatar loads and you'll be in a gray error robot. Then you can freely change avatars as you see fit. This also works for Desktop users if you hold down the backslash `\` key
* 👩‍💻 Creators: **Improved the Shader Fallback System!** There's a lot of improvements and it is rather technical, so please check out our newly-augmented [Shader Fallback System](/docs/shader-fallback-system) documentation.
* Holding right-click in Desktop Mode will cause the reticle to temporarily appear
* Added collapsable sections to the Here, Selected User, and Settings tabs in the Quick Menu
* Clicking "Avatar Details" in the QM will now open the details in the Quick Menu rather than in the Main Menu
* Added a button in the Camera tab to open the Picture save directory in Windows
* Added the user's current world info to the User Profile section of the Quick Menu
* Added an info panel to the Camera tab to explain where pictures are saved
* Added an error message to a situation during Oculus VRC+ purchases that would previously error with no message
* Reduced animation motion in the Quick Menu when using arrows to cycle between users in the instance
* Unavailable avatars are now displayed in grayscale in the Avatars wing
* Updated AVPro to version 2.2.4
* We gave VRCat a bunch of pats and now they're doing all the stuff they should've been. patpatpatpatpatpatpatpatpatpatpatpatpatpatpatpat


## Fixes


The following issues were fixed:


* Logging out of an account and logging back into another would cause some information to be incorrectly retained
* In some worlds, a "goggle" overlay effect would appear in the camera
* The camera did not display the skybox color correctly
* Remote lenses would not have their orientation correctly shown
* Some avatars would not appear in the avatar wing of the Quick Menu
* The "Letters" user icon (as in, no icon selected) in the gallery was missing the letters
* Some worlds would cause the Quick Menu audio to loop abruptly
* SDK2 avatar emote names would not appear in the Quick Menu Emotes wing
* Scrolling in the Main Menu had some issues
* "Return to Default Home" button would not work properly in VR
* Some UI could stick after closing the main menu
* The Quick Menu offered incorrect options when a user was blocked
* Only the first 16 images would appear in a Gallery in some cases
* Buttons to Flip and Move image in the icon and image cameras weren't working properly
* The Action menu could mess with the UI mouselook
* Some visuals in the Expression wing had incorrect colors
* The Clone Avatar button wouldn't update properly in some cases
* A variety of safety and security fixes


Various small fixes were applied to:


* VRC+ favorites in the Quick Menu Favorites Wing
* HUD element render order
* Sounds and haptics when selecting user capsules


## Known Issues


* Meta/Oculus social features are available on the Desktop Meta/Oculus app, but do not do anything
* Meta/Oculus social features will tell you incorrect information if you are in Ask Me / orange status
* Hitting the Screenshot button in VR may cause the view to flicker


# Udon


## Improvements


* General performance improvements to Udon
* UdonBehaviour Interact text has been exposed to Udon via `Set InteractionText` and other methods
* `PostProcessVolume` has been exposed to Udon via:
	+ `Get` and `Set blendDistance`
	+ `Get` and `Set priority`
	+ `Get` and `Set isGlobal`
	+ `Get` and `Set weight`


## Fixes


The following issues were fixed:


* Manual sync sometimes would get "stuck" and `OnDeserialization` would not fire for remotes until someone else joined
	+ More precisely, we fixed a bug that caused synced variables to not be properly received on UdonBehaviours that implemented `OnOwnershipTransferRequest`


# Documentation


* The [Shader Fallback System](/docs/shader-fallback-system) has been updated with a full description of the functionality of the new Shader Fallback procedure
Updated 3 months ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Features](#features)
		- [Improvements](#improvements)
		- [Fixes](#fixes)
		- [Known Issues](#known-issues)
	+ [Udon](#udon)
		- [Improvements](#improvements-1)
		- [Fixes](#fixes-1)
	+ [Documentation](#documentation)
