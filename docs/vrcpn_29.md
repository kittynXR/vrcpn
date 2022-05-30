# VRChat 2021.3.2p1

Release - 12 August 2021 - Build 1123

[Suggest Edits](/edit/vrchat-202132p1)# Client


* Fixed an issue with PostProcessLayers which would affect Post Processing settings not appearing on user cameras
* Fixes to constraints in the SDK to make their behavior match in-app
* Made adjustments that will catch and skip bad draw calls that can result in crashes during certain situations
* Fixed MSAA being disabled on Quest 1
* Fixed issues with TextMeshPro shaders on outdated Quest content by automatically replacing them
* Added TMPro shaders to the always include shaders list
* Added legacy particle shaders to the always include shaders list which should help fix cases where the shaders turned opaque


# Udon & SDK


* Changes to recompile all Program Sources when opening project to resolve issue where programs would appear to be empty in the inspector, especially on Prefabs.
* Disabled function that Clears the log after Udon import - this was also clearing on entering PlayMode, hiding logs that happened during Start.
* Fixed issue where SerializedAssets would be removed from UdonBehaviours in the Editor
* Fixed issue where UdonBehaviours on Instantiated objects would not be registered for events
* Reduced VRC Control Panel Draw calls for better performance when visible
* Fixed AnimatorControllers which were being hidden in the Inspector
* Added ColorBlock.defaultColorBlack back to Whitelist
Updated 10 months ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
	+ [Udon & SDK](#udon--sdk)
