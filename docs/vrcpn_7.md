# VRChat 2021.1.2

Release - 2 Feb 2021 - Build 1046

[Suggest Edits](/edit/vrchat-202112)# Client


## New Features


### Sending Messages with your Invitations


When sending an invite, or requesting an invite, **you can now send along an Invite Message!** 


In addition, you can now also **respond to invitations or invitation requests with an Invite Message!**



There are several types of Invite Messages:


* **Invite** messages, for when you're inviting someone to your instance,
* **Request Invite** messages, for when you're asking for an invite,
* **Invite Response** messages, for when you're responding to an invite, and
* **Request Invite Response** messages, for when you're responding to a request for an invite.


You can **customize and save** up to 12 messages per message type for a total of **48 messages** saved! We've given you some defaults, but feel free to change them up.


A new UI will appear when sending an invitation or requesting an invite allowing you to select a message to send. This UI will also appear when selecting the "reply" function in the notification panel.


![](https://files.readme.io/8db9558-Sending_Invites_with_Messages_transparent_v2.png "Sending Invites with Messages_transparent_v2.png")![](https://files.readme.io/8db9558-Sending_Invites_with_Messages_transparent_v2.png "Click to close...")
You can type up to 64 characters of text to send along and let your friends know you're on the way, that you'll be a little delayed, or they should join on you instead!


We also added several **new notification envelope icons** to indicate what kind of notification you have waiting for you!


![](https://files.readme.io/de6d1ce-New_Invite_Icons_ColorCoded_v3_3.png "New Invite Icons_ColorCoded_v3 (3).png")![](https://files.readme.io/de6d1ce-New_Invite_Icons_ColorCoded_v3_3.png "Click to close...")
### VRChat Plus: Photo Invites!


We're adding a new benefit to your active **VRChat Plus** supporter subscription: **take a picture and send it along with your new Invite Messages!**



Is someone asking for an invite? **Snap a quick picture to send along with your invitation** to show your friends what they're hopping into!


When you get a photo invite from someone, **click the image to view it at a larger size**!


This feature uses the same camera as the user icon feature so you can quickly snap an image!


### The Notification Page


When you receive a notification (including the new invite request/response messages), they now appear in the **new Notification page** in addition to their old position on top of the Quick Menu!


![](https://files.readme.io/9b1da05-QuickMenu_Notifications_Big_v4.png "QuickMenu Notifications_Big_v4.png")![](https://files.readme.io/9b1da05-QuickMenu_Notifications_Big_v4.png "Click to close...")
When you click on a notification on the top of the Quick Menu or click on the notification bell at the bottom of the Quick Menu, you'll be taken to the new Notification page.


A red "NEW" badge will appear on the notification bell icon when you have unread notifications.


On the Notification page, you can see a list of your pending notifications.


You can accept the notification (as in, accept the invite) with the check icon, decline to respond or act on the notification with the X icon, or reply with the reply icon!


If you get a photo with the invite you just got, you can **click on the thumbnail to view it at a larger size!**


In the bottom right of the notifications page, you can disable the display of photos in case you don't want them to show in a recording or on a stream.


Replying will open up a response window that lets you send back a message letting your friend know you're busy, you'll drop by later, or whatever message you like!


## Changes and Fixes


* [Removed an extraneous confirmation prompt for sending an invite](https://feedback.vrchat.com/open-beta/p/1043-remove-invitation-required-pop-up-for-invite-requests)
* [Fixed an issue preventing the Safety system from properly muting avatar audio set to play on avatar spawn](https://feedback.vrchat.com/bug-reports/p/safety-settings-wont-sometimes-block-avatar-audio)
* Fixed an issue where UI sliders would sometimes get "stuck" on the VRChat laser pointer
* Fixed an issue where the user's UI and HUD would show in panoramic photos
* Safety and Security fixes


# Udon / SDK


* [Udon: Added support for TextMeshProUGUI](https://feedback.vrchat.com/vrchat-udon-closed-alpha-feedback/p/add-textmeshprougui-to-the-whitelist)
* Node Graph: Fixed array editor behavior
* [Fixed an issue where instantiated UdonBehaviors would be delayed before activating](https://feedback.vrchat.com/vrchat-udon-closed-alpha-bugs/p/1039udonbehaviours-on-instantiated-objects-activate-after-a-15s-second-delay)
* Added instancing support to the mobile matcap shader included in SDK


# Known Issues


* Invite Response camera may not properly capture all post-processing effects present in the world. This will be fixed in an upcoming patch or release.
* Output logs contain unintentionally garbled strings. This will be fixed in an upcoming patch or release.
* Edits made to the invite message prompts may take a few minutes to propagate through the system or it might be instantaneous. This may have been fixed by a recent API change-- we're keeping an eye on things!
Updated over 1 year ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [New Features](#new-features)
		- [Changes and Fixes](#changes-and-fixes)
	+ [Udon / SDK](#udon--sdk)
	+ [Known Issues](#known-issues)
