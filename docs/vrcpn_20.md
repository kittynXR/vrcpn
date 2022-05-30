# VRChat 2021.2.3

Release - 3 June 2021 - Build 1101

[Suggest Edits](/edit/vrchat-202123)![](https://files.readme.io/54bc69b-HeaderImage_IdentityUpdate_v2_1.png "HeaderImage_IdentityUpdate_v2 (1).png")![](https://files.readme.io/54bc69b-HeaderImage_IdentityUpdate_v2_1.png "Click to close...")
This is the **Identity Update**! The focus of this update is to provide you with a bunch of new ways to identify yourself in VRChat! Everyone can fill out their profile, write up a custom status, and see status on people's nameplates for a quick at-a-glance look at who's who around you! You can also enjoy some nice new quality-of-life features like status history, increased favorite friend/world playlist sizes, and more.


We've also got some bug fixes, performance improvements, and a handful of new Udon additions!


**If you're a VRChat Plus supporter**, enjoy the new Gallery feature and the ability to set a custom image as your Profile picture! This profile picture will replace your avatar thumbnail in social menus! Create a custom image using image editing software and upload it on the site, or just take a picture in VRChat and use that instead! You can also use Gallery images for image invites-- so make some fancy invite cards for your next event, or just to show off a bit.


# Client


## Features


![The new user profile!](https://files.readme.io/05ff68d-IdentityUpdate_ProfilePage.png "IdentityUpdate_ProfilePage.png")![The new user profile!](https://files.readme.io/05ff68d-IdentityUpdate_ProfilePage.png "Click to close...")The new user profile!


* The "User Profile" page in the Main Menu has been reworked, rearranged, and had some new features added!
	+ You can access your own User Profile page via the "In Room" row of the Social panel. Clicking yourself will lead you to your own profile
	+ The User Profile displays your profile picture, your status, your trust rank, any badges you have, your bio, your Playlists, and your public worlds
	+ The profile picture is either your custom profile picture (if you use that feature) or your current avatar's thumbnail
	+ The bio is a text field that you can write some details about yourself in. It has a limit of 512 characters, and can be edited either in the VRChat application or on the website
	+ There's also a button that allows you to view a user's profile on the VRChat website. Clicking "View on VRChat.com" will open a browser to the profile page for that user on the VRChat Home site
	+ The world that the user is currently in will display in the bottom left, under "Current World". If it is joinable, you can click on it to bring up the world page!
		- This means that if your friend is in a public instance, you can drop a portal to your friend's instance!
* Your nameplate now includes your custom status message! By default, this is only visible when your Quick Menu is open. Open your Action Menu to configure it to always show if the nameplate is visible, or to be always hidden.


![Status on nameplate!](https://files.readme.io/6e8d6e5-Id_update_NameplateStatus.png "Id_update_NameplateStatus.png")![Status on nameplate!](https://files.readme.io/6e8d6e5-Id_update_NameplateStatus.png "Click to close...")Status on nameplate!


* Your last 10 statuses are saved server-side, and you can reset to them at any time! Use the big "history" button on the side of the Edit Status window to see the last 10. We didn't keep track before now, so you'll get some placeholders at first. They'll drop off the list as you fill out your own history.
* The size of favorite friend lists has been increased to 64 (from 32)
* The size of world playlists has been increased to 64 (from 32)
* You can now search Community Labs! Simply search for Worlds like normal, then click the checkbox at the top of the results to "Show Community Labs"
* **VRChat Plus Benefit**: You can now choose an image from your Gallery as a **Profile Image**!
	+ This image will appear in the place of your current avatar's thumbnail, like in the User Profile page or the social menu
	+ You can choose any image from your Gallery (including ones that you upload from the VRChat Home website¹) as your profile image
	+ To use your avatar image again, go to your own User Profile page and click "Use Avatar Image"


![The VRChat Plus image Gallery](https://files.readme.io/362cf9c-IdentityUpdate_Gallery.png "IdentityUpdate_Gallery.png")![The VRChat Plus image Gallery](https://files.readme.io/362cf9c-IdentityUpdate_Gallery.png "Click to close...")The VRChat Plus image Gallery


* **VRChat Plus Benefit**: You can now upload images to the **Gallery**, which is a repository of images currently used for profile images and custom invite images
	+ These images can be taken using a camera in VRChat, or uploaded from the VRChat Home website¹
	+ These images can currently be used for the Profile Image feature, or as the photo in a Photo Invite
	+ This means that you can easily create a fancy profile image or whip up a nice-looking invite card, upload it, and use it in VRChat!


¹ Uploading images to the VRChat Gallery via the Home website will not be available during the initial Open Beta testing period, and will become available later or at release time.


![Use Gallery Images with your VRC+ invites!](https://files.readme.io/36afb92-IdentityUpdate_InviteGallery.png "IdentityUpdate_InviteGallery.png")![Use Gallery Images with your VRC+ invites!](https://files.readme.io/36afb92-IdentityUpdate_InviteGallery.png "Click to close...")Use Gallery Images with your VRC+ invites!


## Changes, Fixes, and Improvements


* **Your user Status text is now visible to the public**, instead of just friends and users in your current instance.
* Adjusted the default MSAA multiplier for PCVR to 4x instead of 8x for performance savings. An option has been added to the Performance menu for users that prefer 8x
* Adjusted locomotion exiting stations so that bumping your control stick won't accidently jump you out of the station (requires analog value of 0.7 to exit)
* Fixed a long-standing issue preventing users from interacting with the Quick Menu while falling or moving quickly
* Fixed an issue where some WMR headsets and some canted display headsets had NearClip and FarClip improperly applied, resulting in undesired culling behavior
* Several changes were made to reduce the negative impact of avatar initialization timing changes made in [2021.2.1](/docs/vrchat-202121), which caused issues such as arm twisting and strange leg movement during locomotion
* Fixed an issue where the audio source for voice wouldn't move properly in some culling situations
* Fixed an issue where the AV3 utility poses (IKPose, TPose) weren't being used in some situations


# SDK & Udon


* Object and Int arrays can now be shuffled using Utilities.ShuffleArray
* VRCObjectPool can now shuffle its spawn order using VRCObjectPool.Shuffle
* UdonBehaviours now have a 'DisableInteractive' property you can get and set to control whether an object with an Interact event should accept pointer raycasts and show an interactable outline and tooltips
Updated 12 months ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Features](#features)
		- [Changes, Fixes, and Improvements](#changes-fixes-and-improvements)
	+ [SDK & Udon](#sdk--udon)
