# VRChat 2021.2.4

Release - 16 June 2021 - Build 1106

[Suggest Edits](/edit/vrchat-202124)This is the **Regions Update**! This update's big feature is the introduction of Regions, which permits players who live in certain areas of the world to have lower ping and a better experience when interacting with other players in their same region! 





**In addition to our current default US region, we're enabling these two new regions:**


* **EU** - European Union
* **JP** - Japan


**When creating an instance, you can choose between the "US", "EU", and "JP" regions.** When you make a choice, VRChat will remember that choice for next time.


![](https://files.readme.io/e14a05a-VRChat_2021-06-10_16-26-31.png "VRChat_2021-06-10_16-26-31.png")![](https://files.readme.io/e14a05a-VRChat_2021-06-10_16-26-31.png "Click to close...")
**When selecting a pre-existing instance via the Worlds menu or via a friend's current world, you'll see an icon on the world thumbnail** with the matching icon for the region that instance is hosted in.


![](https://files.readme.io/2ff799f-vlc_2021-06-16_15-43-07.png "vlc_2021-06-16_15-43-07.png")![](https://files.readme.io/2ff799f-vlc_2021-06-16_15-43-07.png "Click to close...")
Choosing a region that's close to you and your friends will minimize the amount of latency involved with anything involving fast updates, like voice and movement!


Keep in mind that if you and your friend are separated by long distances, there will always be someone with a less-than-optimal ping. Try as we might, we couldn't defeat the speed of light. Maybe next time!


# Client


## Features


* Added **regions**! Players can now choose to create an instance in a specific region
	+ Choosing a region close to you will reduce latency and improve your experience
	+ VRChat currently has regions set up in these geographic locations: US (United States), EU (European Union), JP (Japan)
	+ When creating a new instance, you can choose between the three regions
	+ This choice will be remembered when creating instances in the future
	+ Viewing an instance (via Worlds menu or "Current World" in a user's profile) will show the region as a small flag icon on the thumbnail


## Changes, Fixes, and Improvements


* Significant improvements to memory usage regarding avatar caching
	+ Avatars that are no longer in use in the instance will be periodically unloaded from memory
	+ Changing instances also will completely clear this avatar in-memory caching (as it did before, but just a reminder!)
	+ You may notice a small framerate hitch when content is unloaded
* Fixed an issue where users in FBT would have chest/spine bones incorrectly twist during extreme poses like handstands
* Performance optimizations to viseme processing
* The VRChat camera and screenshots will now always use at least 4X MSAA to improve image quality regardless of the user's performance settings
* Additional fixes to improve user status update reliability and speed
* Fixed issues with avatars and worlds getting stuck at 100% when loading
* Fixed issues causing physics material settings on pickups to be lost in certain situations


## Known Issues


* If you attempt to join a friend who is in an instance that is over capacity by clicking on the user in your Social menu, clicking on their current instance, and then click "Go", you will be unable to join. Use "Join" on the User Profile page instead
Updated 12 months ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Features](#features)
		- [Changes, Fixes, and Improvements](#changes-fixes-and-improvements)
		- [Known Issues](#known-issues)
