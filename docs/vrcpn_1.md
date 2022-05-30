# Patch Notes - Pre-2018

[Suggest Edits](/edit/patch-notes-pre-2018)The patch notes listed here are from before we used the year-based [semver-like](https://semver.org/) system we use now. Most are from 2017. 


They are listed in descending order, with the most recent at the top.


# VRChat 0.12.0p15


Released: February 28, 2018  

***CLIENT***


**CHANGES**


* Vive Movement Tweaks
* Pressing the trackpad down a second (or subsequent times) will no longer stop your movement. Lift your thumb from the pad to stop movement.
* Center deadzone is slightly larger to help with fist gesture
* New World Row
* When a world is graduated up to either the Avatar or Community Spotlight row it should no longer appear in the new world row.


**FIXES**


* Issues with failing to login with a “SendHMDAnalytics” or “TooManyRequests” message have been fixed
* Fixed Panic Mode hotkey on Xbox controllers, keyboard
* Avatars should no longer “squish” down into their seats over time when seated
* Various security and stability fixes


If you are having issues as if your account is missing, please contact [[email protected]](/cdn-cgi/l/email-protection) with your VRChat username from the email address you registered your account under.


# VRChat 0.12.0p14


Released: February 24th, 2018


Hi! Welcome to VRChat 0.12.0p14. This is a quick, small patch to fix some outstanding bugs.


Restart Steam to force the download of the latest client. The current build number is Build 523. 


***CLIENT***


**FIXES**


* Desktop override buttons will no longer trigger all other avatar's overrides locally.
* Fixed login issues


# VRChat 0.12.0p13


Released: February 23, 2018  

***CLIENT***


**Changes**


* Avatar Pedestal saves between sessions — any avatar selected from a pedestal will stay as your avatar so long as that avatar remains public.
* Panic Button - in the event that unwanted audio or visual spam occurs, or your frame-rate tanks, you can engage in Panic Mode to audio-and-visual mute anybody who isn't your friend.  

- Desktop: Shift+Esc  

- Rift: both triggers OR both grips and both menu buttons  

- Vive: both triggers OR both grips and both menu buttons  

- Windows Mixed Reality / Other VR: take your plank or pancake or whatever crazy input type you're using and press both triggers OR grips and menu buttons if they exist  

XBox Controller: both triggers and back and menu buttons  

Once you enable Panic mode, you must disable it by unchecking the "Mute Users By Default" and "Block Avatars by Default" options in the System menu
* Avatar Public/Private flag
	+ In the SDK, you can now set an avatar as public or private
	+ Public is meant for use with pedestal avatars and avatars that you want to share.
	+ Private is meant for use with avatars that you do not want to share.
	+ We have not completed securing private avatars yet — this feature just concerns whether or not the avatar should be secured.
* New Rows in the World Menu
	+ Community Spotlight - Worlds of high quality, interesting content, or fun games
	+ Avatar - Avatar worlds with lots of pedestals
	+ Avatar sound effects are now affected by the "SFX" slider in the System menu.
* Keyboard Gesture Overrides
	+ You can now trigger gestures with the keyboard!
	+ Hold down Left Shift and F1-F8 for left-hand gestures.
	+ Hold down Right Shift and F1-F8 for right-hand gestures.
	+ Your arms still aren't animated, so these are mainly useful for animation overrides.


**Fixes**


* Issues with audio spatialization failing when users with audio clips on their avatar load/play audio have been resolved
* Hip tracking using a single Vive Tracker has been fixed.
* Tragically Hip tracking still broken.
* Offline Friends are back! We lost them for a bit.
* VRChat Cache downgraded from gargantuan to simply enormous, now capping at 10GB
* Local Avatar Override was changed to Ctrl-\


***SDK***


**Changes**


* Manage Uploaded Content window now:
	+ Shows the progress of how many items it has loaded
	+ Caches avatar/world images


**Fixes**


* No longer causes performance issues when Build Control Panel is open with avatars in scene


# VRChat 0.12.0p12


Released: February 2, 2018  

***CLIENT***


**Changes**


* New Instance Type: Invite
	+ Very private. Owner can accept invite requests and send invites. Occupants get notifications that others want into the instance.
* New Instance Type: Invite+
	+ Somewhat private. Owner and any occupants can accept invite requests.
* Friends list is now sorted alphabetically
* User lists on the social page are now expandable
* The small Red Arrows that allow expanding of rows in menus have been replaced with Expand and - Collapse buttons
* You can now join friends in Friend instances if the owner is also your friend


**Fixes**


* Object owner disagreement between clients has been fixed. This was causing pickups to fly around worlds
* Fixed notifications showing up blank in some cases
* The forced audio source falloff curve in the SDK has been fixed


# VRChat 0.12.0p11


Released: January 30, 2018  

***CLIENT***


**Changes**


* Due to security updates, users can no longer request invites from players in private instances. We are aware that this may be confusing or frustrating, and we will be addressing this feature again shortly.


**Fixes**


* Eye simulation works again!
* Audio bug progress. Should be less frequent but if you encounter it please send us video or steps to reproduce.
* Fixed issue where certain pickups only could be picked up by master.
* Fixed issue where static portals didn't take users to the same instance.
* Local testing has been fixed (requires new SDK).
* Fixed issue where objects deleted caused performance drop.
* In the world details we now show 20 automatically selected instances of a world that are sorted to be more meaningful to users, instead of all instances of that world.
* Fixed bugs and updated the automatic instance selection where users were loading into an empty hub or other worlds.


# VRChat 0.12.0p10


Released: January 22, 2018  

***CLIENT***


* Fixes
* Server and security updates
* Known Issues
* Eye simulation (tracking) is not working, will be fixed in next patch


# VRChat 0.12.0p6


Released: January 11, 2018  

***CLIENT***


**Changes**


* Manages server load better
* Fixes
* Fixed 9 degree rotation on avatar pedestals


# VRChat 0.12.0p4


Released: January 6, 2018  

***CLIENT***


**Changes**


* Non-Steam account email addresses must be verified to login to client. You can resend your verification or update your email address from www.vrchat.com/home/profile
* Adjusted falloff distance for Avatar Audio Sources, it should now match voice falloff distance more closely
* Avatar pedestals now show avatar image instead of avatar model (turns out downloading all avatars in avatar worlds are inflating our server bills. Hope everyone understands. May make it an optional setting in the future)
* Many VRChat worlds (HUB, Bowling, etc) now come bundled with client and load without a download (won’t go live until a few days after patch)


**Fixes**


* Fixed issue that caused videopanel to play error video when videopanel loaded without video playing
* Fixed issue where portals to private worlds split up people into their own instances
* Fixed an error that could cause destroying of objects to reduce framerate significantly in games such as CTF
* Fixed issue where doing an emote with a non-humanoid avatar caused you to no longer be able to move
* Fixed issue where voice chat audio was heard from incorrect locations for remote players (if you are experiencing this, it’s because your avatar is doing something weird with audio source)


**Known Issues**


* Unblocking users can result in them not being unblocked correctly, restarting client fixes it and lets you and unblocker see each other again


***SDK v2018.01.03.12.06***


**Fixes**


* Fixed issues where some users were unable to upload content


# VRChat 0.12.0p3


Released: December 14, 2017  

***CLIENT***


**Features**


* General performance improvements
* Added Friends Only instance type, where only friends of the instance owners can join
* Votekicks are now sticky for the world instance
* Instance owners can kick, warn and turn off other users’ mics
* World authors can kick, warn and turn off other users’ mics
* Moderator actions for instance owners and authors are available from the quick menu
* Added some checks to ensure users can’t accidentally back into a portal
* Added different icons for different notification types
* Added error world to send users when they get stuck in infinite loop
* Ban messages now display reason and length of ban
* Public Ban Type where banned users are banned from public worlds instead of the entire app
* Added Desktop tutorial
* Improved IK <-> animation blending


**Changes**


* Client changes avatar audio sources to spatial


**Fixes**


* Fixed issue where blending IK and locomotion results in avatars being dragged behind player
* Fixed bug that disconnected users when changing worlds after spending more than an hour in a world
* Fixed default alien avatar so it doesn’t have a bright glow in worlds with bloom
* Fixed Search UI in client is all white if you've visited a world with a web panel
* Fixed bug where pickups aren’t destroyed for new users even though the pickup was actually destroyed
* Fixed bug where desktop users see wrists vibrating on avatars
* Fixed bug where VRC\_Trigger executes buffered event, is destroyed, then new users get bad FPS
* Fixed issue where some users couldn’t load into large worlds
* Video player playlists no longer show white screen when users join mid video
* Multiple video players in scene no longer cause performance hitches


**Known Issues**


* Unblocking users can result in them not being unblocked correctly, restarting client fixes it and lets you and unblocker see each other again


***SDK v2017.12.12***


**Features**


* Added SetAnimatorInt event
* Added ability to specify spawnPoint in ObjectSpawn event


**Changes**


* Whitelist LineRenderer on avatars
* Upgraded Sdk pano prefab


**Fixes**


* Fixed issue where random avatars and worlds are overwritten when a different avatar or world is uploaded
* You can have prefabs that are not in the scene instantiate other prefabs that are not in the scene
* Fixed issue with ObjectSync/TeleportTo rpc where chaging targetLocatoin param on one object changed it on others
* Removed broken warning incorrectly stating client and SDK are incompatable


***WEBSITE***


**Features**


* Users can change email and password from their homepage
* Users can create invite-only links to instances from the website
* Users can search for other users from website


# VRChat 0.12.0p2


Released: October 27, 2017  

***CLIENT***


**Features**


* Author of an world is now able to sticky kick a user from the world or an instance for 1 hour
* Author of an world is now able to warn a user from the world or an instance
* Mod spawned polaroid camera can be used by users
* Performance improvements


**Changes**


* Changed “Request Host” button to ”Report Abuse”
* Change "host" on nametag to "mod"
* Only display user kicked message to initiator of vote-kick [Community Request]
* Added black outline to nameplate text for easier reading


**Fixes**


* Hand gesture should reset to default when user removes finger from vive pad [Community Request]
* Fixed error spam with AvatarPedestal
* World metadata initialized immediately upon world load
* Fixed VRCHIVE 360 photos
* Fixed infinite reload when launching from a bad VRC url
* Worlds open for a long period no longer take extra time to load for new players
* Fixed memory leak in worlds open for long periods of time
* Fixed particle effects on portals
* Fixed VoteKick not working if player to be kicked is master client
* Players vote-kicked from world no longer get stuck in infinite loop
* Reference camera post effects no longer carry over from world to world
* Fixed mod spawnable polaroid cameras


***SDK v2017.12.12***


**Features**


* Added OnStationEntered Trigger [Community Request]
* Added OnStationExited Trigger [Community Request]
* Add LeaveStation Trigger Action, which evicts whoever is in the target station from the station [Community Request]
* Add a SetOwner Trigger Action, that can set the owner of a target GameObject to Instigator [Community Request]
* Add a "Trigger Custom Actions at Random" Trigger Action, allowing only one of a given set of custom triggers to be triggered at random. [Community Request]


**Changes**


* Convert VRC\_Chair to use Triggers


**Fixes**


* PipelineSaver is no longer flagged during avatar upload
* Fixed PlayerMods editor script


# VRChat 0.12.0p1


Released: October 5, 2017  

***CLIENT***


**Features**


* Optimized some avatar animation components
* Optimized performance for dynamic bone on avatars


**Changes**


* Mic status now persists across worlds
* Changed default VRChat image in menu


**Fixes**


* Fixed changing avatars while seated leaves seated idle
* Fixed third person locomotion animation
* Fixed loading scene double space tunnel
* Fixed issue where there was a quick blast of sound when leaving worlds
* Fixed issue where video player lags everyone except master in a world
* Fixed bug where two vrchat installation helpers popup when closing VRChat
* Fixed loading avatar stuck in place
* Fixed changing avatar in a chair breaking viewpoint position
* Fixed text overlap in main menu
* Fixed dynamic portal countdown timer and counter not working
* Fixed issue where nametags in ground upon first joining a world
* Fixed issue where tooltip UI on equipped objects is not attached to the object
* Fixed issue where players randomly become invisible
* Fixed issue where some animations are not smooth (Heliride)
* Blocked users are no longer able to send friend requests to the blocker
* Fixed issues with blocking and unblocking users
* Potential fix for Video Player lags everyone except master in room after a while
* Ensure non whitelisted components don’t work on local or remote avatars
* Fixed hands being rotate incorrectly
* Fixed static portals
* Fixed strobe lights in bowling
* Fixed issues with vive trackers and calibrating
* Fixed Hub reload issue where there was a bad master
* Fixed issues surrounding object childed to the VRC\_SceneDescriptor
* Fixed guns acting like non equip objects
* Changing avatar while calibrating avatar for full body tracking no longer breaks locomotion
* Fixed issue where avatars are dragged across map when teleporting


**Known Issues**


* Mic status now persists across worlds


***SDK***


**Features**


* Added VRC\_CustomRendererBehaviour (includes RealtimeGIUpdated)


**Changes**


* Restrict certain components that can be uploaded on an avatar to save performance
* Replaced Ethan with tutorial avatar
* Removed VRCYoutube prefab
* More SDK example changes
* Updated SDK examples
* VRC\_Trigger proximity defaults to 1 instead of 100
* VRC\_SyncVideoPlayer works with lists of urls
* VRC\_SyncVideoPlayer supports Youtube, Vimeo and DailyMotion links


**Fixes**


* Avatar pedestals update when blueprint id is changed


# VRChat 0.12.0


Released: August 30, 2017  

***CLIENT***


**Features**


* Upgraded to Unity version 5.6.3p1
* New keyboard supports International layouts
* Desktop users have full IK
* Improved Framerate
* Improved experience for severely degraded connections
* Supports Vive trackers for full body tracking


**Changes**


* To change avatars, users must now select the avatar, and then select the “Change” button
* Removed dynamic light from portal prefebs


**Fixes**


* Improved voice chat reliability
* Fixed issue where Unity incompatible microphones resulted in infinite VRChat loop
* Menu properly scales to avatar’s size
* Eye and mouth movements now work in mirror (with a delay on the mouth movement)
* Avatar menu can handle more avatars
* Desktop users heads are properly rotated when loading
* Menu opens at proper height when opened when avatar is sitting or crouched
* Menu does not open underground
* Smoother arm and hand movement
* Seats work with moving platforms/vehicles
* Fixed a bug where you would just feel sad, sometimes, and not know why
* Better text over portals
* Many bugs in ownership and event replication
* Better motion for desktop avatars


**Known Issues**


* Mirrors degrade framerate
* Web panels are disabled


***SDK***


**Features**


* Upgraded to Unity version 5.6.3p1 - allowing for 3d movies, 3d pictures, 3d panorama,, better particle effects, and more
* Build process is quicker
* Buffer One option for events
* Avatar animations, gestures and emotes can be customized
* Avatar upload warns about rigs that break FinalIK
* Integrated Unity post processing stack
* Added VRC\_SyncVideoPlayer


**Changes**


* Turned on Future Proofing by default when uploading worlds and avatars


**Fixes** 


* Many bugs in authorization and login flow
* VRCCam in SDK should default to a better preview position and settings
* Future Proofing is much quicker when iterating on worlds and avatars


# VRChat 0.11.7p5


Released: August 30, 2017  

***CLIENT***


**Features**


* Terms of Service added


# VRChat 0.11.7p2


Released: May 2, 2017  

***CLIENT***


**Fixes**


* Improved Performance


# VRChat 0.11.7p1


Released: April 25, 2017  

***CLIENT***


**Fixes**


* Fixed issue where players could not hand an object to another player
* Fixed spelling mistake in About menu text
* Fixed issue where remote desktop avatar heads did not rotate up and down
* Fixed issue where portals to private worlds take users to different instances
* Fixed issue where avatar pedestals change users remotely but red error avatar appears locally
* Haptics and dotted lines appear again when hands are close to a pick-up object
* Notifications now properly clear when accepted or declined once
* Users should no longer be able to stand on top of each other
* Presentation room should no longer crash when there are many drawings and someone enters or reloads (unfortunately, this means we don’t always pass older drawings to users when they enter)
* Avatars load quicker, resulting in less hitching when users enter a world or change avatars


# VRChat 0.11.7


Released: April 14, 2017  

***CLIENT***


**Features**


* Private Worlds - Users can create private copies of public worlds. When creating a new instance, there will be the option to create a friends-only or invite-only private world
* Request Invite - Users can request an invitation from a friend in an invite-only world
* Private World Moderation - Authors of any world, and owners of private worlds can kick unwanted users out
* Microphone Switching - Users can now change their microphones in System Menu
* Improved Voice - Speech should be more consistent, with less dropout. Users with high latency or low bandwidth should also experience improved voice chat
* See Friends - Friends are no longer blocked by personal space
* Seated and Standing Play - Oculus users with an Xbox controller are set for Seated Play, while those with Touch controllers are set to Standing Play. Shortcut menu buttons have been renamed and have icons added.
* Better video - gamma correction and linear filtering added to YouTube panels


**Fixes**


* Users who are sitting should appear to be so even when others leave and reenter the world
* Youtube panels should not sync across worlds
* Gamma fixed on Youtube Panels
* VRChat now works with the Steam VR Beta
* Other users’ mouths move if they are talking even if you have them muted
* Other users' mouths move if you are talking if you are a ventriloquist


# VRChat 0.11.6p1


Released: March 9, 2017  

***CLIENT***


**Features**


* Users can choose to have new people be unmuted or muted for them. This setting is also available in the System menu.


**Fixes**


* Improvements to interaction tutorial in the hub
* Users should not be able to climb on each other
* Fixed touch support on non-Steam Oculus build


# VRChat 0.11.6


Released: March 6, 2017  

***CLIENT***


**Features**


* Users can now select each other directly to interact
* Users must unmute others to hear them
* Nameplates now show who can hear you, who you can hear, and also show your friends
* Added safe search youtube wall
* Users can adjust their microphone volume in the shortcut menu
* Gain adjustment automatically quiets users with loud microphones
* Users have personal space, which prevents other avatars from being drawn when they are too close. This can be turned off in system
* Voice chat uses less bandwidth
* Nearby users no longer shown in the shortcut menu. This space is now reserved for notifications
* Menu for desktop users has been reduced in size and moved out of the way to make it less intrusive
* Web VRChat links now work with steam build


**Fixes**


* Users cannot block themselves!
* Objects do not float if a user disconnects while holding them
* More fixes for situations where users could not hear each other
* Players can no longer set their height to zero and break their avatars


# VRChat 0.11.5p10


Released: February 13, 2017  

***CLIENT***


**Changes**


* VRChat accounts must be verified via email in order to login


**Fixes**


* Fixed more issues where players sometimes couldn’t hear each other


# VRChat 0.11.5p7


Released: February 10, 2017  

***CLIENT***


**Fixes**


* Fixed issue where players sometimes couldn’t hear each other
* Fixed bug where mods couldn’t turn off players’ mics
* Fixed bug where mods would wake up, in Tijuana, in a bathtub full of ice, with a fresh scar


# VRChat 0.11.5p6


Released: February 10, 2017  

***CLIENT***


**Changes**


* Avatar events and triggers can only be played locally


**Fixes**


* Tons of network fixes and cleanup


# VRChat 0.11.5p4


Released: February 9, 2017  

***CLIENT***


**Changes**


* Features to reduce hot-mics from new users
* Desktop users have a new icon to help them determine how to operate their mics


**Fixes**


* More fixes for users unable to get into the HUB occasionally


# VRChat 0.11.5p3


Released: February 8, 2017  

***CLIENT***


**Changes**


* Tweaked audio drop-off so separate conversations can be had more easily in all worlds


**Fixes**


* More fixes for users unable to get into the HUB occasionally
* If the HUB fails to load, VRChat will automatically try to load a new HUB instance and it works this time. Probably.


# VRChat 0.11.5p2


Released: February 7, 2017  

***CLIENT***


**Features**


* Mods can reload world for all users in the world
* Mods can move all users from one world to the HUB
* Mods can dance if they want to - they can leave their friends behind


**Fixes**


* Potential fix for users not being able to get into the HUB
* If the HUB fails to load, VRChat will automatically try to load a new HUB instance


# VRChat 0.11.5p1


Released: February 4, 2017  

***CLIENT***


**Features**


* Added PvP muting because sometimes blocking is too much
* Mods can now turn off players’ mics if the mic is accidentally left on
* Mods can now turn off players’ mics if the player is singing 80’s pop hits


**Fixes**


* Fixed occasional hub reload when the master client gets in a bad state
* Fixed social search


# VRChat 0.11.5


Released: February 1, 2017  

***CLIENT***


**Features**


* Ability to login via Steam account
* Ability to call a moderator for help
* New Content - Steel ‘n’ Gold


**Fixes**


* Fixed bug where the voice chat plugin could not be found
* Fixed occasional infinite reload on app start
* Fixed issue where friend requests could not be accepted thru main menu
* Fixed issue where pickups could be offset from hand if picked up when tracking is lost
* Fixed issue where tracking could be confused by three children using VR from within a trenchcoat


**Changes**


* Vote to kick results in a 60 min ban from world instance
Updated 3 months ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [VRChat 0.12.0p15](#vrchat-0120p15)
	+ [VRChat 0.12.0p14](#vrchat-0120p14)
	+ [VRChat 0.12.0p13](#vrchat-0120p13)
	+ [VRChat 0.12.0p12](#vrchat-0120p12)
	+ [VRChat 0.12.0p11](#vrchat-0120p11)
	+ [VRChat 0.12.0p10](#vrchat-0120p10)
	+ [VRChat 0.12.0p6](#vrchat-0120p6)
	+ [VRChat 0.12.0p4](#vrchat-0120p4)
	+ [VRChat 0.12.0p3](#vrchat-0120p3)
	+ [VRChat 0.12.0p2](#vrchat-0120p2)
	+ [VRChat 0.12.0p1](#vrchat-0120p1)
	+ [VRChat 0.12.0](#vrchat-0120)
	+ [VRChat 0.11.7p5](#vrchat-0117p5)
	+ [VRChat 0.11.7p2](#vrchat-0117p2)
	+ [VRChat 0.11.7p1](#vrchat-0117p1)
	+ [VRChat 0.11.7](#vrchat-0117)
	+ [VRChat 0.11.6p1](#vrchat-0116p1)
	+ [VRChat 0.11.6](#vrchat-0116)
	+ [VRChat 0.11.5p10](#vrchat-0115p10)
	+ [VRChat 0.11.5p7](#vrchat-0115p7)
	+ [VRChat 0.11.5p6](#vrchat-0115p6)
	+ [VRChat 0.11.5p4](#vrchat-0115p4)
	+ [VRChat 0.11.5p3](#vrchat-0115p3)
	+ [VRChat 0.11.5p2](#vrchat-0115p2)
	+ [VRChat 0.11.5p1](#vrchat-0115p1)
	+ [VRChat 0.11.5](#vrchat-0115)
