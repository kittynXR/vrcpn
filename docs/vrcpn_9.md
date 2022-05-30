# VRChat 2021.1.3

Release - 23 Feb 2021 - Build 1054

[Suggest Edits](/edit/vrchat-202113)# Client


## Changes, Improvements, and Fixes


* Improvements made that should help reduce hitching in various cases, mostly involving the UI
* Some optimizations to asset loading systems. Note: results are dependent on the content in question (asset type, size, optimization, etc)
* Fixed an issue where all avatars would reload when closing the Performance Settings window without changing any settings
* Fixed some refresh/display issues with the notification page
* Fixed an issue causing notifications and the message composition menu refreshing when a user joins
* Added new options to local config to allow advanced users to adjust the cache maximum size and expiry delay: `cache_size` and `cache_expiry_delay`. They cannot be lower than 20GB/30 days respectively. See our documentation on the [Configuration File](/docs/configuration-file#cache-settings) to learn more
* Fixed an issue that caused Occlusion Culling to be unreliable if Post Processing was enabled in the world
* Made changes that *may* help prevent rare consistent hitching for certain players in long-running rooms
* World authors can now join instances of worlds they've created even if the instance is at maximum capacity. The client UI will not reflect this yet
* Instance owners can now join instances that they've created even if the instance is at maximum capacity. The client UI will not reflect this yet


# Udon


* New Udon `Utilities.IsValid()` method for detecting destroyed GameObjects and VRCPlayers who have left the instance
* Node Graph: Fixed error with converting strings
Updated over 1 year ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Changes, Improvements, and Fixes](#changes-improvements-and-fixes)
	+ [Udon](#udon)
