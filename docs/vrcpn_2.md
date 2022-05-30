# Patch Notes - 2018

[Suggest Edits](/edit/patch-notes-2018)The patch notes listed here are from 2018. They are listed in descending order, with the most recent at the top.


# VRChat 2018.4.4p6


Released: January 31, 2019


## Client


### Fixes


* Security fixes


# VRChat 2018.4.4p5


Released: January 18, 2019


## Client


### Fixes


* Updated video download binaries


# VRChat 2018.4.4p4


Released: January 3, 2019


## Client


### Fixes


* Fixed an issue preventing proper use of the "Create Account" button at login


# VRChat 2018.4.4p3


Released: December 21, 2018


## Client


### Changes


* Changed maximum Favorite Avatars from 3 to 16


### Fixes


* Fixed an issue causing some StandardAsset scripts to be removed when they shouldn't have
* Fixed the "World Unavailable" thumbnail in Playlists for worlds that are no longer public
* Some additional network optimizations regarding redundant/unneeded data sync


# VRChat 2018.4.4p2


Released: December 21, 2018


## Client


### Changes


* Reverted changes that calculated IK locally and transmitted results. IK is now calculated locally on the viewer's machine for all users in the room, as it was in the previous release (2018.4.3)
	+ Unfortunately, this change resulted in additional server load that we cannot handle at this time. We are going to put a high priority on reducing the load and making this method viable, as it is a very large performance gain
* Fixed issue that caused significant network issues when a new user joined a world with many Stations present


# VRChat 2018.4.4p1


Released: December 21, 2018


## Client


### Changes


* Fixed an issue preventing proper authentication when logging on with a Steam or Oculus account


# VRChat 2018.4.4


Released: Dec 20 2018


## Client


### Features


* **It is again possible to place chairs on avatars!** Use this to create things like car avatars, carry around people in your hands or on your shoulders-- anything you can think up! Please note: This feature is prone to weirdness and may act strange. For best results, try to mount the chair on your avatar such that the "head" location (as in, where a standard-sized occupant's head will be when sitting) is as close as possible to the Bone/GameObject the VRC\_Station is a child of
	+ The easiest way to add a station to your avatar is to create an empty GameObject as a child of whatever you want it to "stick" to, then add the `VRC_Station` script to that new empty GameObject. Don't use the VRCChair prefab, you'll get some SDK errors
* **The SDK's limit on polygon (triangle) count is now 70,000, and will now warn you if your avatar is unoptimized in the Build Control panel.** Check out the SDK section below for details on the changes to the SDK
* **Favorite Worlds have become Playlists, and you can view other users' Playlists!**
	+ **You have up to three Playlists** that you can save worlds into
	+ **Each Playlist has a maximum of 32 worlds**
	+ **You can name each Playlist** as you see fit
	+ **You can set the Privacy level of a Playlist** to Public, Friends-Only, or Private
	+ **You can view the Playlists of other users on their Social page** by clicking on the Playlists button.
* **You can now see avatar performance statistics of someone's avatar performance while in VRChat.** This system is not meant to be an end-all-be-all authority on performance, but it can help guide users improve their avatar's performance impact. It is purely informational and does not limit anything at this time. Check out our [**Avatar Performance Ranking System**](/docs/avatar-performance-ranking-system) page for more details. You can access it in two ways:
	+ When your Quick Menu is open, you'll see an icon on the left side of the nameplate that indicates the general "performance ranking" of the avatar that user is wearing
		- Performance ranks are (in descending order of performance): "Excellent", "Good", "Medium", "Poor", "Very Poor"
	+ When you select someone with your Quick Menu open, you can click the "View Avatar Stats" button to view details on their avatar's performance
		- These numbers are highlighted depending on where they fall on the Ranking scale
		- You can also view the stats of your own avatars in the Avatar tab of the menu
		- The numbers used in this system are **not final** and we will be tweaking it based on feedback and further review
* **You can view your own avatar's performance ranking by clicking "View Avatar Stats" on your Avatar page**
* **[You can now Clone any Public Avatar](/docs/public-avatar-cloning) that another user is wearing as long as they have "Allow Avatar Cloning" enabled in the Settings menu!** See an avatar that someone's wearing? Want to try it on yourself? As long as it is a Public avatar and the user in question has "Allow Avatar Cloning" checked in their Settings menu (enabled by default), then you can just click them, click the button on the right in your Quick Menu, and you're good to go!
	+ **Important Note:** If you have avatars that you don't want to be Cloneable, make sure they're set to Private in the "Manage Uploaded Content" section of the SDK
* **You can also view the Social page of the Author of an Avatar any user is wearing!** Find this button right below "Clone Public Avatar" on the right side of the Social Quick Menu once you click on someone
* **We slipped in some festive Holiday emoji.** Please use mistletoe responsibly.


### Changes


* **We have implemented heavy optimizations to the IK system!** You now only calculate the IK of your own local avatar, and you transmit the results of those calculations to others. This should greatly reduce the cost of IK, which was previously one of the most intensive parts of the app
* **We have added a World Script Whitelist** to improve security in worlds and prevent users from accessing scripts they should not have in worlds. [See the full list of whitelisted world scripts here](/docs/whitelisted-world-components)


### Fixes


* Safety and Security fixes
* Fixed an issue causing VRChat to recognize game controllers as trackers
* Fixed an issue where certain animators would cause worlds to crash
* Fixed an issue where moving the mouse slowly horizontally would cause the movement to "catch"
* The user point of view when sitting on a moving station is MUCH smoother (affects avatar and world stations)
* Users without AVX instructions on their CPU should be able to launch VRChat once again. Thanks to Oculus for providing a patch!


### Known Issues


* Playlists currently have several issues with viewing/editing/sharing them. We're working on fixing this ASAP.
* Announcement in pop-up during load informing users about Cloning is missing a URL. We're working on fixing this ASAP.
* Moving stations, particularly on avatars, may result in some strange behavior. For best results, try to mount the chair on your avatar such that the "head" location (as in, where a standard-sized occupant's head will be when sitting) is as close as possible to the Bone/GameObject the VRC\_Station is a child of
* Doing any emote such as backflip, sitting in a station, and then getting back out will freeze you for about two minutes. Workaround: Don't do this
* If you sit on a station that is on the avatar of someone sitting on you, you get flung into space. This is your punishment for breaking physics. Workaround: Don't do this-- or do, and accept the wrath of Newton
* You can only have one copy of a world in any playlist (as in, you can't have the same world in multiple playlists)


## SDK


### Features


* **The SDK will now warn you when you are exceeding counts of various component types on avatars.** This includes material counts, Dynamic Bone Affected Transforms, Dynamic Bone colliders, Skinned Meshes, and etc. We also provide links to our [Avatar Optimizing Tips](/docs/avatar-optimizing-tips) documentation to help users optimize their avatars. These warnings are non-blocking **for now**-- in the future, this will change
* **The SDK will tell you what Performance Rank your avatar is** so you can see before you upload.


### Changes


* **The SDK now permits avatars to have up to 70,000 polygons/triangles.** Going above 70,000 polygons/triangles will prevent you from uploading your avatar


### Fixes


* The SDK has been informed that we've upgraded to 2017.4.15f1 and will no longer whine that it wants to go back to 5.6


# VRChat 2018.4.3p1


Released: December 12, 2018


## Client


### Changes


* Slight change to client reconnection behavior to mitigate issues when having problems with real-time networking services


# VRChat 2018.4.3


Released: December 11, 2018


## Client


### Unity 2017 Upgrade


* **VRChat has upgraded to Unity 2017.4.15f1**. Please read our [Blog Post](https://medium.com/@vrchat/vrchat-upgrade-to-unity-2017-4-90727844522a) on the subject to learn more.
* **Check out our documentation on [Migrating from 5.6 to 2017.4](/docs/migrating-from-56-to-20174)** for a full guide on installing 2017.4.15f1 and migrating your projects.
* You must re-upload your **worlds** if:
	+ **You have baked lighting in the world and left the lights enabled**, otherwise the lights will revert to "Mixed" lighting, hurting performance
	+ **You have a mirror in the world**, otherwise the mirror will behave strangely
	+ **You use Realtime GI (Global Illumination) in your world**, otherwise it will not work
	+ **You have animations in the world that affect GameObject rotation**, otherwise the rotations will behave incorrectly
	+ **You have used Crunch Compression on textures in your world**, otherwise the textures will not decompress/display properly
* You must re-upload your **avatars** if:
	+ **You have animations on your avatar that affect GameObject rotation**, otherwise the rotations will behave incorrectly
	+ **You have used Crunch Compression on textures on your avatar**, otherwise the textures will not decompress/display properly


### Features


* **Support for Unity Store assets that require Unity 2017.4** (as a reminder, we do not support assets that require C# scripting)
* There are many new features in Unity 2017-- far more than we can list here. The [Blog Post](https://medium.com/@vrchat/vrchat-upgrade-to-unity-2017-4-90727844522a) has a link to a [doc we've created that lists many of the new features available](https://docs.google.com/document/d/1ob0G6IYJdUZuLGkV6SUherQJmiLkNICqMdc7LXtis5A/edit?usp=sharing). Not *everything* new in Unity 2017 is available in VRChat just yet, but *a lot of it is*-- experiment, play around, and let us know how things work on our [Canny](https://vrchat.canny.io)


### Changes


* ***IMPORTANT:*** If your CPU is lower than our minimum requirements (Intel i5-4590/AMD FX 8350 or equivalent), you may experience crashes. This is because your CPU does not support the AVX instruction extensions, which are required for usage in VRChat.
* **"New" World Row is now sorted by Creation date** rather than Modified date
* **"Recently Updated" World Row added**, which is sorted by Last Modified (same as 2018.4.2)
* **Updated SteamVR SDK**
* **Updated Oculus SDKs** (LipSync, Spatializer)
* **We now support the Post Processing v2 stack.** You must download the version [here](https://github.com/Unity-Technologies/PostProcessing/releases/tag/2.1.1)
* **Disabled the microphone switcher** in-app until mic switching has been fixed


### Fixes


* **VRC\_SyncVideoPlayer and VRC\_SyncVideoStream no longer have audio/video desync over time** tied to CPU load
* **Users will no longer crash when viewing an avatar with a disabled Cloth object**
* **Turning your view is no longer tied to framerate** and should feel consistent no matter your current performance level
* **Users will now spawn directly on World Spawns** rather than offset based on their position in their playspace
* **You can now un-Favorite Worlds that have been removed** and show up as "???"
* **Improved app behavior on disconnect/reconnect cycle**
* **Fixed user info not displaying properly when they are in an Invite+ instance**
* **Fixed bug in physics update time**, which was causing unnecessary jitter on objects


### Known Issues


Upgrading from 5.6 to 2017.4 carried a few bugs forward for us. Our primary focus was getting Unity 2017 live and working for users. We're working on all of these issues for soon-to-come releases.


* **You cannot change your microphone device from within VRChat.** Workaround: Set your Default Recording and Communication Device in Windows before launching VRChat. If you wish to change your microphone while VRChat is still running, you have to disable the "old" microphone device that you're swapping from. This will be addressed in a future patch (this is a Unity bug)
* Toggling sitting or standing mode will rotate you based on your controller's orientation, not your head
* Haptics are stronger than they should be
* Putting hands in mirrors results in your hand coming back out
* Rarely, voice gets louder then quiets back down for the next clip spoken
* Hand gestures locked in open palm in desktop mode
* VRC\_Stations with inclined/angled transforms do not adjust camera as expected
* If you have 50 or more avatars, your Personal avatar row may sometimes disappear (fix by closing/reopening menu)
* VRChat sometimes freezes upon closing
* SteamVR detects game pads as a FBT trackers and puts you into calibration mode. Work around this by checking your SteamVR before launching VRChat, and if you see an additional controller, unplug it
* Horizontal mouse movement can hitch occasionally when moving very slowly


## Website and Account


### Features


* **You can now edit many of your world's properties from the website!** You can change things like your world's name, your description, or your tags. We will be moving most of the world management away from the SDK and toward the website over time.
* **You can now add a YouTube trailer for your world!** This trailer will be displayed in our new World Link format that we'll be updating soon.


## SDK


### Changes


* Updated for Unity 2017.4.15f1


### Known Issues


* **The SDK will complain about being on the incorrect version.** You can safely ignore this.


# VRChat 2018.4.2p1


Released: November 28, 2018


## Client


### Changes


* Modified disconnection error dialogs to auto-dismiss after a short period


# VRChat 2018.4.2


Released: November 20, 2018


## Client


### Features


* We've added **User Reporting**. You can find the "Report User" button under the "Favorite User" button in the Social menu. This allows you to report users for issues with behavior, the user's avatar, text (such as their name or status), or the thumbnail image for their avatar. This works very similarly to World Reporting. If you have urgent issues or something that doesn't match any of the report reasons, please continue to contact *[[email protected]](/cdn-cgi/l/email-protection)* with reports


### Changes


* Updated bundled content for faster load times of popular worlds
* When looking at someone's Social panel, Public worlds that they've authored are now visible even if you aren't friends with them
* Added background to friend request popup


### Fixes


* Safety and Security fixes


## Website and Account


### Features


* You can now change your own name on the VRChat Home site! Check out our [Knowledgebase article](http://help.vrchat.com/knowledge_base/topics/id-like-to-change-my-username) for more details.


## SDK


### Fixes


* SDK camera adheres properly to FoV set on SDK camera


# VRChat 2018.4.1p3


Released: 8 November 2018


## Client


### Fixes


* Fix an issue causing most audio on avatars to be set to zero volume
* Fix an issue that was disabling GPU skinning optimizations
* Fix an issue causing sessions to expire when sitting in a room for too long


# VRChat 2018.4.1p2


Released: 7 November 2018


## Client


### Fixes


* Updated Video Player backend components to fix YouTube playback. No new features or additions


# VRChat 2018.4.1p1


Released: 6 November 2018


## Client


### Changes


* Temporarily disable "Upgrade Account" button until Steam Account upgrade issue is resolved


# VRChat 2018.4.1


Released: 6 November 2018


## Client


### Features


* **You can now upgrade a Steam account into a VRChat account, or merge a Steam account into a pre-existing VRChat account!** You can find the button to Upgrade Account in your Settings menu, in the bottom right. ***You will only see this button if you are logged into a Steam account.*** Follow the steps as you're prompted
	+ **If you already have a VRChat account**, you will be prompted to "merge" your Steam account into your VRChat account
	+ **If you do *not* already have a VRChat account**, you will be prompted to make a new VRChat account, and then merge your Steam account into the new VRChat account
	+ The merge process can take up to an hour, so keep that in mind
	+ Merging or upgrading a Steam account into a VRChat account will carry over all your friends, your favorites, and your groups into your new or pre-existing VRChat account
	+ You will retain the name of your VRChat account when you merge
	+ Merging or upgrading an account is irreversible, so ensure you're merging or upgrading into the correct VRChat account. **Once an account is merged or upgraded, it cannot be undone.**
* **The UI has received a visual overhaul!** Although functionality remains the same, the UI has been changed in numerous places for visual consistency.
* **Worlds can now have up to five "tags".** Tags make it easier for users to find a world. Example tags might include "game", "avatars", or "hangout"
	+ You can search for Tags in the Worlds search interface by searching for a term, then changing the "Search In" button to "Tags" instead of "Title".
* **Users can now Report worlds** for various issues. Find the Report button on the World Details tab.


### Fixes


* Safety and Security fixes
* Performance fixes, including a more performant Voice Chat


## Website and Account


### Features


* When your email address on your VRChat account has been changed, you will receive an email notification to your old email address


## SDK


### Features


* You can now add up to five "tags" when uploading a world


# VRChat 2018.3.3


Released: October 16, 2018


## Client


### Features


* All of the emoji in the Quick Menu have been redone! In addition to changing the graphics, we've added two more pages worth of emoji, and added effects to some of them. We also threw in some Halloween emoji for good measure!
* **You can now view more details about a world in the world page**, including:
	+ The world's author. You can click on the author's name to access their social page
	+ The world's file size
	+ The number of people in public and private instances
	+ The description of the world (as set when uploading the world)
* You can now click on the "You are in *this world*" top of the Worlds tab to view details of the world you're in
* Added two new world rows
	+ **Games** - These worlds are interactive games you can play with other people!
	+ **Halloween** - These are Halloween worlds that might be a tad bit spooky. They may also remind you that you have a skeleton inside you *right now*


### Changes


* You can now view a user's Trust Rank in their social page
* Tuned desktop mode crouching a bit
* Moved the "Exit VRChat" button in the settings menu so you don't accidentally click it while adjusting nearby settings
* Changed the image used when loading thumbnails so that overlaid text is more readable
* Removed in client account registration in favor of website registration
* Loading screen elements are now mirrored both in front and behind you
* Updated messages received when Warned or Kicked to be more concise and less severe-sounding
* Updated video player components
* Added a small sound effect when you select items in the menu/quick menu


### Fixes


* Safety and security fixes
* Fixed some strange behavior when sitting before your avatar has loaded, and sitting while changing Safety settings
* Normal maps are now preserved when Standard falls back to Standard during shader blocking
* Quick Menu laser is no longer blocked by the notification row if there are no notifications
* Idle animation for other users now plays at the proper speed


### Known Issues


* Private instance count in world description is sometimes wrong


## SDK


### Changes


* The SDK now forces you to setup layers instead of simply asking you to do so when uploading a world


# VRChat 2018.3.2p1


Released: October 3, 2018


## Client


### Fixes


* Fixed an issue which caused full-body tracking not to initialize properly, preventing it from working locally or remotely
* Fixed an issue causing strange stretching/bending when crouching in desktop and looking up/down
* Fixed an issue causing other users' camera indicators not to appear when they have been spawned
* Fixed an issue causing stations (seats), portals, onTimer triggers, and various other components not to work properly in some cases


### Known Issues


* Desktop crouch issues may still occur on occasion, but can be fixed by swapping avatars


# VRChat 2018.3.2


Released: October 2, 2018


## Client


### Features


* **Introducing the VRChat Trust and Safety System!** This system is a new extension of the currently-implemented VRChat Trust system, and is designed to keep users safe from nuisance users negatively impacting your experience in VRChat. [Read more about it here!](/docs/vrchat-safety-and-trust-system)
* **You can now Favorite up to 3 avatars!** In your Avatar menu, while you're wearing the avatar, click "Favorite" under the preview on the left. You can only favorite avatars from pedestals. We plan on addressing organizing your own uploaded avatars in a future update
* **Quick Menu has been revamped** with a better layout, a new style of toggle, and a new section on the top of the menu that is context-sensitive. See the Safety System document for more details
* **Social Quick Menu has been revamped**. See the Safety System document for more details


### Changes


* **Legacy animations on avatars newer than September 1st, 2018 will be removed.** See this [blog post](https://medium.com/@vrchat/legacy-animations-update-5906df811183) for more info. **This does not affect non-legacy animations**
* **The VRChat Home has been updated** with some new videos instructing users on how to use the Trust and Safety System
* "System" menu has been renamed "Settings"
* **There is now a "Go!" button on the loading screen** that lets you idle at the loading screen before you load into a world. **If you don't want this, you can disable it** in your Settings menu: "Skip Go Button in Load"
* **Toggle Nameplates and HUD has been moved** to the "UI Elements" quick menu
* **Offline Friends is now hidden** until you click to expand
* **World rows in Avatar/Social menus are now hidden** once you are a New User Trust Rank or higher
* **Mic volume slider has been moved** to the Settings menu
* **Loading screen background** has been darkened significantly
* **Initial "VRChat" loading screen has been changed** to match the new loading screen background
* **Changed up some loading screen tips**, added more related to the Safety System
* **"Mute Users by Default" and "Block Avatars by Default" have been removed**, as they are now managed by the Safety Mode you're using
* **Safe Mode** (triggered by Shift+Esc on Desktop, both Menu Buttons+both Triggers in VR) no longer mutes and blocks all users, but instead reverts you to the "Safe Mode" Safety Mode.
* **Muting a user no longer mutes the audio on the avatar**, as the Safety System now handles this
* **When you unfriend a user, you now have to click a confirmation box** so you don't accidentally unfriend someone
* **Online friends in friend groups are now listed first** before the offline users
* **The login screen now has a button to temporarily show your password** so you can ensure you're typing it right


### Fixes


* Safety and Security fixes
* World filesize is now calculated correctly wherever it is displayed. Apparently, 1000 != 1024 ¯\\_(ツ)\_/¯
* Optimization to the menu to lessen the frequency and severity of frameloss while browsing friends, worlds, etc
* Rotating your wrist should no longer result in strange local-only twisting behavior while in VR
* Updated components of SyncVideoPlayer to fix YouTube functionality


### Known Issues


* If you enter a station that is disabled when the world starts and is enabled by a trigger later, you cannot exit it and must respawn


## SDK


### Fixes


* Fixed an issue where the SDK spammed errors in the Unity console when it didn't recognize some data sent by the API


# VRChat 2018.3.1


Released: September 4, 2018


## Client


### Features


* Added some new loading screens with new music, a more descriptive loading bar, and some helpful tips for your time in VRChat
* Desktop users now have a reticle in the middle of the screen to help show what they're pointing at. This reticle can be toggled off in the System menu, and will hide when you press Ctrl-H to hide the other UI elements
* Desktop users can now toggle crouching with the "C" key and go prone with the "Z" key


### Changes


* Active Worlds now also shows at the bottom of your Social menu
* Avatar Worlds now also shows in the bottom of your Avatars menu
* Active Worlds now show at the top of the World tab, instead of the Featured Worlds


### Fixes


* When nameplates are off, users who are muted retain their muted status
* Fixed an issue that would result in users getting a black screen on world load
* Fixed an issue where if you had both the old `vrchat;config.json` and the new `config.json`, VRChat would hang indefinitely
* Fixed an issue where the damage graphic might persist between worlds
* Fixed several issues that resulted in users getting disconnected


## SDK


### Fixes


* Mirror Default Maximum Anti-aliasing now *actually* set to 1 instead of 8


# VRChat 2018.2.3p1


Released: August 23, 2018


## Client


### Fixes


* Potential fix for an issue that resulted in various problems such as red nameplates at spawn, repeating mic voice, black screens upon joining a full world, and other related issues


# VRChat 2018.2.3


Released: August 23, 2018


## Client


### Features


* You might have noticed that we've released a **new Hub!** Our art team has put a lot of hard work into it, and it was been designed as a meeting place for groups before you go out adventuring through the metaverse. Take some time to explore, put on a monocle and moustache, and relax in the park.
* You can now **bookmark friends into groups** in your Social panel! These bookmark groups store friends that you assign, so you can access them quickly. Assign friends to bookmark groups to keep track of your social circles.
	+ To add a friend to a bookmark group, click the "Favorite" button on their social details screen and choose which group to add them to.
	+ Select the button next to the bookmark group's row to rename that bookmark group
	+ To remove a friend from a bookmark group, go to their social details screen and click "Unfavorite"
	+ You can have up to 32 friends in each bookmark group
	+ You can have up to 3 bookmark groups (for a total of 96 friends across all bookmarks)
* You can now set your **Status**! Your Status is a message which allows you to inform users with a short custom message of what you're up to, as well as a status icon that allows you to customize how you receive invite requests. In a private world, but you're accepting invites? You can choose to **auto-accept invite requests**. Don't want any invite requests? You can set yourself to "**Busy**". Find the Status UI in top left of the Social tab.
	+ Click inside the field to type your custom Status message. You can also set a Status type:
		- Join Me (blue) - Auto-accepts any invite requests
		- Active (green) - Any invite requests will have to be manually accepted (this is the previous behavior)
		- Busy (dark red) - Hides all notifications


### Changes


* The "Request Invite" notification when you're not the owner of an instance now has a "Decline" button
* VRChat's output log is now located in `%AppData%\..\LocalLow\VRChat\vrchat` and is named `output_log.txt`
* VRChat's configuration file (at the moment only used for the [Avatar Particle System Limits](/docs/avatar-particle-system-limits) system) is now located in `%AppData%\..\LocalLow\VRChat\vrchat` and is named `config.json`
* VRChat's output log format has been greatly improved and is much more readable


### Fixes


* **Performance fixes** related to how we handle networking for events, objects, and users
* Eye tracking should now work properly again when using full-body IK. Thanks for the [Canny report](https://vrchat.canny.io/bug-reports/p/eye-tracking-broken-when-using-full-body-tracking), Gallium!
* Mutes and blocks have been fixed so they aren't "sticky" and won't persist after you've unmuted/unblocked the user and swapped worlds
* Your currently online Friends list will now paginate properly and show all of your online friends
* Significantly reduced the occurrence of the level-wide "hitch" when your client loads an avatar
* Fixed a small graphical issue with the World Loading screen
* **Safety and Security** fixes and improvements. For security purposes specifics of these changes are not provided


### Known Issues


* Avatars may appear to take a bit longer to load (but will cause less frame drops as a result)


## Website


**Find all these new features at the VRChat Home website:** <https://vrchat.com/home>


### Features


* You can now view a list of friends and see if they're online, offline, or in a private world!
* You can click to join a friend directly in the world they're currently in
* You can search for worlds, find them, and join instances right from the website.
* You can now view the list of your worlds, featured worlds, popular worlds, avatar worlds, and spotlight worlds


### Changes


* Documentation at [docs.vrchat.com](http://docs.vrchat.com) have been revamped and updated across most articles


## SDK


### Changes


* The default "Max Anti Aliasing" value on the Mirror prefab has been changed from 8 to 1. Thanks for the [Canny report](https://vrchat.canny.io/bug-reports/p/set-mirror-anti-alias-in-sdk-to-1-instead-of-8), Mimi!


### Fixes


* Fixed the example URLs included in the [VRC\_SyncVideoPlayer](/docs/vrc_syncvideoplayer) prefab example to include URLs it could actually play. Thanks for the [Canny report](https://vrchat.canny.io/open-beta/p/201822-feedbackbug-example-videoplayersync-has-incorrect-urlscomponents), PhaxeNor!


# VRChat 2018.2.2p1


Released: August 17, 2018


## Client


**CHANGES**


* Web Panels have been disabled due to a security issue. Read more at our blog post [here](https://medium.com/@vrchat/security-update-web-panels-4699fa0be103).
* Other security fixes


# VRChat 2018.2.2


Released: June 26, 2018


## Client


**FEATURES**


* We now support the use of the [VRC\_SyncVideoStream](/docs/vrc_syncvideostream) component for playing Twitch and YouTube Live streams! See the documentation on this feature [here](/docs/vrc_syncvideostream).
* There is now a mouse sensitivity slider for Desktop users! Find it in the System menu
* The particle limiter has been re-implemented, but it is now an optional, beta system that a user must enable. Settings for this system are tweakable per-user. You can enable the system and change these settings for yourself in a file saved in the same directory that the output logs are saved. See a guide on the recommended limits and how to set your own limits [here](avatar-particle-system-limits). To reiterate, this system is **not enabled by default** and must be enabled by creating the configuration file.


**CHANGES**


* VRChat will now display the file size of worlds on the World's icon in the top left
* If VRChat detects that you are using an AMD card with drivers installed known to have issues with some community-created shaders, it will inform you that you need to update


**FIXES**


* Many bugs fixed related to performance/error reporting
* Even more Safety and Security fixes


**KNOWN BUGS**


* SyncVideoStream audio may sometimes play to the wrong Windows Mixer channel. If this occurs, VRChat will mute the audio to avoid overly loud volume. If you have no audio, check your Windows Audio Mixer for an extra channel. You may have to restart VRChat to fix this issue.
* SyncVideoStream has some issues playing videos in Normal mode (as in, non-live static videos). This feature is still being worked on, so we strongly suggest that you check out [VRC\_SyncVideoPlayer](/docs/vrc_syncvideoplayer) for use with static videos.


## SDK


**FEATURES**


* You now have access to the VRChat Home Kit! This kit includes the Home world, which will allow you to create your own version of the Home! Check out our video and view more documentation about the Home Kit [here](vrchat-home-kit).
* Added the [VRC\_SyncVideoStream](/docs/vrc_syncvideostream) component
* Added the [VRC\_VideoScreen](/docs/vrc_videoscreen) component for use with [VRC\_SyncVideoStream](/docs/vrc_syncvideostream) component
* Added the [VRC\_VideoSpeaker](/docs/vrc_videospeaker) component for use with [VRC\_SyncVideoStream](/docs/vrc_syncvideostream) component


**CHANGES**


* New triggers added to `Example-Triggers.unity` included with the SDK
* New actions added to `Example-Actions.unity` included with the SDK


**FIXES**


* VRCWorld prefab had the UpdateTimeInMS set to 10ms even though the slider value in inspector is capped to 33ms as minimum value. The default is now set to 33ms.


# VRChat 2018.2.1p1


Released: June 12, 2018


## Client


**FIXES**


* Fixed a regression that broke AddDamage and AddHealth action on players.


# VRChat 2018.2.1


Released: June 12, 2018


## Client


**CHANGES**


* Many safety and security fixes have been implemented
* **Favorite Worlds**: There's now a limit of 32 worlds for Favorite Worlds, up from 20


## SDK


**FEATURES**


* The SDK now has a Splash Screen that details the latest changes, added features, and notes that opens when you open a Unity Project with the SDK imported (this can be disabled)
* Improved Drag and Drop support in Trigger Reference fields
* New Triggers and Actions added
	+ **TRIGGERS**
	+ OnOwnershipTransfer - Used to detect when the ownership of an ObjectSync object ha changed
	+ OnDisable (like OnEnable) - Fires when a game object is disabled
	+ **ACTIONS**
	+ PlayHaptics - Used to play haptics in a Touch or Vive controller. Must be used with VRC\_Pickup
	+ SetUIText - Used to set the text of a UIText component
	+ SetAngularVelocity - Used with a rigidbody to set it's angular velocity
	+ AddVelocity - Used with a rigidbody to add to its velocity
	+ SetVelocity - Used with a rigidbody to set its velocity
	+ AddForce - Used with a rigidbody to add force
* New Midi Device Triggers
	+ VRC\_MidiNoteIn - Play a virtual piano with a real piano keyboard! Fires when a Note message is received on a MIDI device. You can select NoteOn or NoteOff and which Channel.
	+ VRC\_OscButtonIn - Control your world with a phone or tablet! Fires when an OSC message is received at a specific address. You can specify whether to trigger on Button On (1) or Off (0)


VRChat attempts to connect to all available MIDI devices.  

VRChat attempts to receive OSC messages on port 9000.


**CHANGES**


* All trigger actions' target object field now defaults to the local gameobject


**FIXES**


* BufferOne support added to several actions: SetLayer, SetWebpanelVolume, AddHealth, AddDamage, SetComponentActive, SetMaterial, ActivateCustomTrigger
* Fixed SetKinematic, SetGravity trigger actions


# VRChat 2018.1.3


Released: May 29, 2018


## Client


**FEATURES**


* **Recent Worlds**: You'll find a new row in your Worlds tab called Recent Worlds. It lists the worlds you've been in recently! The history goes back a month, and will not list private worlds.
	+ You can also use the most recent world in your Recent Worlds list to easily access your current world. From there, you can see the author, favorite the world, or make it your new Home!
* **Favorite Worlds**: You can now Favorite up to 20 Worlds, which will show up as a new row in your Worlds tab. Find the Favorite button next to the "Make Home" button for a World.
* **Invert Mouse option**: For all those flightsim enthusiasts
* Various security fixes


**FIXES**


* Fixed VRC\_SyncVideoPlayer freeze when loading in with too many video urls being parsed at once
* Fixed an issue with VRC\_SyncVideoPlayer pausing if you're alone in a room
* Fix to Clear RPC for VRC\_SyncVideoPlayer
* Fix to AddURL RPC for VRC\_SyncVideoPlayer


## SDK


**FEATURES**


* Added OnVideoStart, OnVideoEnd, OnVideoPlay and OnVideoPause triggers for use with VRC\_SyncVideoPlayer


# VRChat 2018.1.2


Released: May 10 2018  

**CLIENT**


**FEATURES**


* Cameras v2



```
    - The camera and lens now have new models! The lens is much more camera-like now, and it is easier to recognize when you are in the spotlight. The buttons now have icons, and also let you see if the camera is oriented correctly. There’s been a lot of changes, so let’s cover the whole feature set once again
    - Filters - There are now a ton of filters available for both the Photo and Stream Camera
        - Old Timey - Doesn’t look like anything to me
        - Pixelate - VRChat now for the PS1
        - Glitch - Glitch, download!
        - Code - You get used to it, I don’t even see the code
        - Sparkles - Mahou shoujo Unity-chan
        - Hypno - When I snap my fingers, you’ll atlas your textures
        - Trippy - You ever seen the back of a 20 dollar bill… on VRChat?
        - Green Screen - Since you can’t buy a big green bed sheet for VR. Useful for videos and streaming!
        - Alpha Transparent - For photoshopping yourself into the group photos. Also good for streaming!
        - Blueprint - This is just a draft
        - Drawing - VRChat Coloring Book
    - Lens Movement Space - You can now set the lens to operate in one of three “movement spaces”
        - Normal - The lens is attached to the camera
        - Player Space - The lens moves with relation to the player. Useful for a secondary view in your stream
        - World Space - The lens locks to a position in the world
    - Lens Movement Behavior - You can change how the lens behaves regarding movement and rotation
        - Normal - The lens is stationary and remains where you place it
        - Steady Cam - The lens attempts to smooth out movement
        - Look at Me - The lens is always oriented toward your head
    - Pins - You can save up to three configurations for either the Photo or Stream Camera using Pins. These configurations save Filter, Lens Movement Space, and Lens Movement Behavior. These settings save until you restart VRChat
    - Timer - Sets a five-second timer with sound feedback, then takes an image (works with either camera)
    - Extender Stick - Extends the grab range of the camera from 1 meter to 2 meters. Don’t try to grab it directly, point toward the camera!
    - Photo Camera - Pulling the trigger on your controller while holding the camera takes a picture and saves it to your Pictures directory in Windows, under a folder called VRChat
    - Stream Camera - Mirrors what is in your camera’s view to your Desktop monitor for easy stream/recording capture. Using the Green Screen or Alpha Transparency filters with recording software allows for easy “facecam” or “Picture in Picture” on your video. Pulling the trigger on your controller while holding the camera toggles between the Pin you are on, and the last Pin you were using. 

```
* Menu-on-top - Your menus now render on top of everything else, and the menu has priority for selection when obstructed by objects or players in the world
* Mute Avatar Sounds - If you mute a user, the sounds on their avatar will also be muted


**FIXES**


* 2018.1.1 enabled a feature to convert shaders on non-friends to Standard with Ctrl-F. This feature is not complete or ready for release, so it has been removed
* Fixes to avatar clones so that mirrors and cameras display your avatar properly
* Nameplates over cameras are now disabled if you have player nameplates disabled
* Blocking and muting now work as expected
* Voice System has had a few bugs worked out, still in progress
* Teleporting or loading into a world will no longer preserve your previous rotation vector and will instead match the spawn location transform rotation as intended
* Stations on avatars have been disabled. This was a planned feature released mistakenly. It will return, but the feature requires some more work and design to avoid abuse and improve user control. See Developer Update for more info
* Buttonless Gaze option removed from System Menu
* Performance issues related to cameras fixed
* General performance improvements
* General security improvements


**KNOWN ISSUES**


* If you leave your Lens in World Space mode and change worlds, your Lens will still be at the same world coordinates, which may not make sense in the new world
* If a user blocks and/or mutes a user in a room and then unblocks/unmutes them in that same room, upon moving to another room with that user they are still blocked/muted and need to be unblocked/unmuted again. In other words, don’t mute or block someone unless you actually want to block or mute them
* Camera Extender Stick is still pretty hard to grab (point your hand towards the camera to grab more easily)
* Buttons on the camera can be difficult to select. Hold the camera with one hand, and choose buttons with the other


# VRChat 2018.1.1


Released: April 24 2018


***CLIENT***


**FEATURES**


* Cameras  

- Photo Camera (VR Only) - Access in the “Camera” menu. Take pictures with a handheld camera! Detach the lens for easy group shots, use a timer for easy setup, and use an arm extension for easy selfies! Images are saved in UserProfile/Pictures/VRChat.  

- Timer - Sets a five second timer to count down before taking an image.  

- Detach Lens - Lets the lens float in space, which allows you to move around while the camera remains stationary  

- Extender - Extends the grab/hold range of the camera to two meters  

- Stream Camera (VR Only) - Access in the “Camera” menu. While using a VR headset, use the Stream Camera to mirror the camera’s view to your desktop. Ideal for recording or streaming in third person!  

- See Active Cameras - You can see all active cameras around you by opening your Quick Menu. All cameras by any user will be highlighted with a bright red column of light, and their viewpoint will be indicated by a red triangle.
* Home  

- VRChat Home - You will now spawn in the new VRChat Home when you launch. Explore the Help videos, some nice music, the latest Developer Update, and a few other fun toys. You can invite your friends to your Home!  

- Set Home - You can set a custom Home world by accessing the World entry for a world, and selecting “Make Home”. Reset it back to the VRChat Home by selecting “Reset Home”  

- Go Home - You now have a “Go Home” button on your quick menu which transports you to your set home world (default is VRChat Home)
* Vive Movement Toggle - You can now swap between the Advanced and Classic Vive movement system by choosing “Advanced Vive Movement” in the System menu. You will default to the Classic system on first login.
* High-Resolution Screenshot - Press Ctrl-F12 in Desktop mode to take a 4K screenshot. It will be saved to UserProfile/Pictures/VRChat. This may cause a little bit of lag, so be careful!
* You can now toggle the HUD and nameplates in your quick menu
* New audio slider in settings for audio sources on avatars
* General security improvements
* General server stability improvements


**FIXES**


* Fixed issue where logging out and then in again in-app resulted in infinite loop
* “Fist” gesture now releases in an analogue-like manner
* Particle systems are limited to reasonable levels


**CHANGES**


* Personal avatars are now shown above default avatars


**KNOWN ISSUES**


* Buttons on the camera can be difficult to select (hold the camera while you select buttons)
* Camera extender is difficult to grab (point your hand towards the camera to grab more easily)
* Nameplates above cameras are not toggleable
* If you have a camera held in your hand and disable the camera, it will prevent you from grabbing things with that hand. Disable the camera while it is not being held.
* If you have your "Mic Defaults On" setting unchecked, your microphone will be muted when you enter a new world.


***SDK***  

The new SDK is available on our site!  

<https://vrchat.com/home>


**FEATURES**


* Enable VRC\_Pickup.Drop() to the SendRPC event type
* New VRC\_IKFollower component for use with world space particles on avatars
* WorldID is removed from VRC\_PipelineManager when the world is deleted from ContentManager
* Added Actions to the VRC\_Trigger for making easier logic with Animators  

AnimationIntAdd - Add a value to an Animator int parameter,  

AnimationIntDivide - Divide an Animator int parameter by value,  

AnimationIntMultiply - Multiply an Animator int parameter by value,  

AnimationIntSubtract - Subtract a value from an Animator int parameter


**FIXES**


* Removed pre-attached world ids from example scenes
* AddDamage and AddHealth event types now work with players when VRC\_CombatManager component is present in a world


**CHANGES**


* Removed popup when toggling privacy status on avatars in SDK
Updated 3 months ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [VRChat 2018.4.4p6](#vrchat-201844p6)
		- [Client](#client)
	+ [VRChat 2018.4.4p5](#vrchat-201844p5)
		- [Client](#client-1)
	+ [VRChat 2018.4.4p4](#vrchat-201844p4)
		- [Client](#client-2)
	+ [VRChat 2018.4.4p3](#vrchat-201844p3)
		- [Client](#client-3)
	+ [VRChat 2018.4.4p2](#vrchat-201844p2)
		- [Client](#client-4)
	+ [VRChat 2018.4.4p1](#vrchat-201844p1)
		- [Client](#client-5)
	+ [VRChat 2018.4.4](#vrchat-201844)
		- [Client](#client-6)
		- [SDK](#sdk)
	+ [VRChat 2018.4.3p1](#vrchat-201843p1)
		- [Client](#client-7)
	+ [VRChat 2018.4.3](#vrchat-201843)
		- [Client](#client-8)
		- [Website and Account](#website-and-account)
		- [SDK](#sdk-1)
	+ [VRChat 2018.4.2p1](#vrchat-201842p1)
		- [Client](#client-9)
	+ [VRChat 2018.4.2](#vrchat-201842)
		- [Client](#client-10)
		- [Website and Account](#website-and-account-1)
		- [SDK](#sdk-2)
	+ [VRChat 2018.4.1p3](#vrchat-201841p3)
		- [Client](#client-11)
	+ [VRChat 2018.4.1p2](#vrchat-201841p2)
		- [Client](#client-12)
	+ [VRChat 2018.4.1p1](#vrchat-201841p1)
		- [Client](#client-13)
	+ [VRChat 2018.4.1](#vrchat-201841)
		- [Client](#client-14)
		- [Website and Account](#website-and-account-2)
		- [SDK](#sdk-3)
	+ [VRChat 2018.3.3](#vrchat-201833)
		- [Client](#client-15)
		- [SDK](#sdk-4)
	+ [VRChat 2018.3.2p1](#vrchat-201832p1)
		- [Client](#client-16)
	+ [VRChat 2018.3.2](#vrchat-201832)
		- [Client](#client-17)
		- [SDK](#sdk-5)
	+ [VRChat 2018.3.1](#vrchat-201831)
		- [Client](#client-18)
		- [SDK](#sdk-6)
	+ [VRChat 2018.2.3p1](#vrchat-201823p1)
		- [Client](#client-19)
	+ [VRChat 2018.2.3](#vrchat-201823)
		- [Client](#client-20)
		- [Website](#website)
		- [SDK](#sdk-7)
	+ [VRChat 2018.2.2p1](#vrchat-201822p1)
		- [Client](#client-21)
	+ [VRChat 2018.2.2](#vrchat-201822)
		- [Client](#client-22)
		- [SDK](#sdk-8)
	+ [VRChat 2018.2.1p1](#vrchat-201821p1)
		- [Client](#client-23)
	+ [VRChat 2018.2.1](#vrchat-201821)
		- [Client](#client-24)
		- [SDK](#sdk-9)
	+ [VRChat 2018.1.3](#vrchat-201813)
		- [Client](#client-25)
		- [SDK](#sdk-10)
	+ [VRChat 2018.1.2](#vrchat-201812)
	+ [VRChat 2018.1.1](#vrchat-201811)
