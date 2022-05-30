# VRChat 2021.4.1

Release - 8 November 2021 - Build 1149

[Suggest Edits](/edit/vrchat-202141)**This is the first half of the VRChat UI update-- UI 1.5!** We've redesigned and rebuilt the Quick Menu from the ground up to be functional, accessible, quick, and sleek all while feeling familiar to VRChat veterans! 


In addition to all the familiar functions, you've got access to the brand-new Quick Menu **Wings**, which are **customizable side panels on your Quick Menu**. Keep your favorite avatars in a Wing to quickly access and wear them, or put your friends on a Wing to see at a glance who's online and which instance to join!


**Want to keep up with the goings-on of VRChat?** Check out the new **Info Banner** across the top of the Launch Pad! These clickable banners will be updated with all kinds of info, including notifications of new versions, blog posts, events, and more. Clicking on them can open up UI panels, open websites, and more.


**Desktop users rejoice!** The cursor now behaves properly and no longer locks your mouse to the VRChat window. When opening the Quick Menu, the cursor in Desktop mode moves into "screen space" mode, permitting easy movement and usage. Hold down Shift to temporarily hide the Quick Menu and enable a "reticle" to easily select a user near you for interaction.


We've added a few new features to the Quick Menu here and there, like the always-useful **"Rejoin World" button**, the super-popular **"sort by location" friends list** from the VRChat Home website, and more. However, we've got **more plans**!


In the future, we're going to open up access to custom Quick Menu Wings and tabs for world authors to add functionality via Udon! Want a menu of locations to teleport to in your world? A list of mirror toggles? A button to spawn a new jet to replace the one you just wrecked? All right there, one click away, in a custom, world-author-defined Quick Menu section. **Coming soon!**


Of course, the Quick Menu's just one half of the new VRChat UI. **Main Menu, you're up next!** Expect to see a rebuilt and redesigned Main Menu in an upcoming VRChat release, likely in early 2022.


Dang, that's a lot! How about we **show** instead of **tell**? Here's a look at the new Quick Menu!



Oh, that last bit? While we were at it, we *also* redesigned and rebuilt the VRChat Camera. nbd.


One last surprise: the new Camera is coming to the Quest version of VRChat in our next major update! 🎉🎉🎉


# Client


## Features


* **The Quick Menu has been completely redesigned and rebuilt!**
	+ **The Launch Pad gives you quick access** to several common menu sections and actions
	+ **The Info banner across the top of the Launch Pad shows you the latest information** on VRChat happenings, like new releases, blog posts, and more
	+ **The "cursor" has been redesigned both in the menus and in world space** to be easily visible, but not large and in the way
	+ **The Wings on the side of the Quick Menu give you a place to show and quickly access** your own Profile, your Friends (and their locations, like the website!), your Avatars (including favorites, and the ability to sort them!), Emoji, and your available Expressions!
	+ **The tabs across the bottom give you quick access** to your notifications, the "Here" menu, your Camera options, your volume sliders, and some common settings
		- **The "Here" menu lists info and provides actions contextually relevant for your current location**, like the brand new "Rejoin World" button
		- **The Camera tab gives you access to camera-related functions**... like the brand new Camera!
		- **The Audio tab gives you access to volume sliders** for Master, Voices, and World, as well as a way to quickly select your mic from a list of devices, and adjust your own mic volume
		- **The Settings tab gives you access to common toggleable settings**, like nameplate display,
	+ In Desktop mode, click "Select User" on the Launchpad tab to put yourself into a selection mode to easily select a user near you... or just hold down Shift to quickly mouse over and click your target user
	+ In Desktop mode, your view is now locked in place when your Quick Menu is open, and your mouse moves in screen-space rather than turning your head
	+ Quickly swap into and out of Safe Mode without wiping your custom Safety settings (*finally!*) using the Safe Mode button in the bottom right
* **The Camera has been completely redesigned and rebuilt!** Tons of new Camera features:
	+ **A brand new model for the camera and camera lens!**
	+ **A brand new UI for the camera**, which lets you select options with the laser instead of clicking buttons! 🙏🙏🙏
	+ **Depth of Field!** Choose between several lens modes to give your photos a stylistic touch by blurring objects out of focus
		- Go with Auto Focus for auto-magic! Click the screen with your selection laser to move the focus circle. Click the circle again to re-center it.
		- Use Semi-Auto to permit some Aperture and Focal Length adjustment
		- Go full Manual to adjust the Focal Distance yourself!
		- Of course, you could just turn it off completely too.
	+ **You can now grab the lens** when its detached to adjust its position. The lens has a small pin light to show which way is up when it is disconnected
	+ **Click the selfie button** to quickly flip the lens around to face you
	+ **Use the Lock button** to lock the camera in place
	+ We're looking into getting the **Camera on Quest**! Keep an eye out in future releases


## Improvements


* **The Main Menu has new theming** with sharper, more crisp graphics
	+ **A full Main Menu redesign and rebuild is already in-progress**, keep an eye out for it in future updates
* **The Fallback "Feather" icon is now always visible** on nameplates of users wearing a fallback even when the Quick Menu is closed, letting you quickly see if someone's in a Fallback avatar. This can be turned off in the Quick Menu (in the settings tab) or by turning off nameplates entirely
* **The camera now saves pictures in folders in the format `YYYY-MM` to aid with organization** (and to prevent Windows from crying out in pain any time it opens a Pictures folder with more than a few hundred images in it)
	+ Old photos won't be organized in this manner, only new ones taken going forward
* Blocking users now comes with a confirmation dialog
* Updated multiple loading screen graphics to reflect new UI
* "Users Blocking You" and "Blocked Users" are now visible at the bottom of the Here tab. This list starts collapsed but can be expanded and made visible
	+ All users will see "Blocked Users", but only world authors and instance owners will see "Users Blocking You"
* "Vote to Kick" notifications now have a unique icon
* The maximum world size for Quest worlds has been raised from 50MB to 100MB
* AVPro upgraded to 2.2.1


## Fixes


* Fixed: First Person View steady-cam wouldn't reload the camera settings properly upon loading a world
* Fixed: The player collider was not able to pass under colliders less than 2m tall, despite being 1.65m tall. The player collider is now 1.65m tall
* Fixed: Seeking behavior with AVPro was buggy
* Workaround: The "Auto Resync" option on video players was causing crashes, so we've temporarily disabled it


# Udon


## Improvements


* None sync can now be used on the same GameObject as Manual or Continuous
* Exposed many requested Udon types!
	+ **New Types**
		- `ParticleSystemRenderer`
		- `CombineInstance`
		- `GradientColorKey`
		- `GradientAlphaKey`
		- `CharacterController`
		- `Vector2Int`
		- `Vector3Int`
		- `System.Math`
	+ **Whitelisted Methods**
		- `AudioSettings.get_dspTime`
		- `AudioSettings.get_outputSampleRate`
		- `Math.Min`
		- `Math.Pow`
		- `CustomRenderTexture.antiAliasing`
		- `CustomRenderTexture.Update`
		- `Animator.Update`
		- `Animator.GetBoneTransform`
		- `TextMeshPro.` / `TextMeshProUGUI.`
			* `ForceMeshUpdate`
			* `UpdateGeometry`
			* `maxDisplayedChars`
			* `textInfo`
			* `meshInfo`
			* `enabled`


## Fixes


* Fixed: Sync type "None" wasn't functional. Oops
* Fixed: `IsUserInVR` would return false for some VR players when called on `Start`
* Fixed: Trigger and Collision events will no longer fire for protected objects like Stations on Avatars and the User's Camera


# SDK


## Improvements


* Added `OnPostprocessAvatar` hook, fires after avatar processing is complete to allow for cleanup operations
* Ensured that `OnPreprocessAvatar` hook stops the build on failure


## Fixes


* Fixed: Build hooks were registered twice, causing unnecessary extra time spent during builds
* Fixed: SDK world builds failed in specific cases


# Documentation


* Improved organization of the Release Notes section, it isn't 10 miles long anymore. Wow, we've had a lot of releases
* Documentation updated with notices that SDK2 is deprecated and should not be used for new projects
* Some very-out-of-date documentation has been removed after sitting in archival status for a long while


# Website


* The VRChat Home Download page has been updated with notices that SDK2 is deprecated and should not be used for new projects. The SDK2 download has been moved to a collapsed "Other" section
* The VRChat Home Worlds page now reflects how the Worlds tab looks in-app! [Check it out!](https://vrchat.com/home/worlds)
Updated 6 months ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Features](#features)
		- [Improvements](#improvements)
		- [Fixes](#fixes)
	+ [Udon](#udon)
		- [Improvements](#improvements-1)
		- [Fixes](#fixes-1)
	+ [SDK](#sdk)
		- [Improvements](#improvements-2)
		- [Fixes](#fixes-2)
	+ [Documentation](#documentation)
	+ [Website](#website)
