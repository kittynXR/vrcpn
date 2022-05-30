# VRChat 2021.1.1

Release - 19 Jan 2021 - Build 1039

[Suggest Edits](/edit/vrchat-202111)# Avatars 3.0


Lots of new features for Avatars 3.0!





* **Avatar parameters are now persistent!** This means that your Avatars 3.0 parameters will be saved and restored any time you load the avatar later-- including switching between avatars, loading a new world, or closing and re-opening VRChat.
	+ **By default, all parameters are saved on all "legacy" Avatars 3.0 avatars. That means that all AV3 avatars will have this ability from launch!**
	+ By default all parameters are saved when creating a new parameter object. *This can be manually disabled on a per-parameter basis in the parameter definition object when creating the avatar.*
	+ These parameters are saved locally.
	+ Parameters are saved per avatar ID
	+ A button to clear all locally saved parameters was added to the Settings menu
* You can now specify a custom default value for your parameters in the Expression Parameters object!
* Added the `bool` parameter type! This parameter can be either true or false. Fancy!
* **You can now have more than 16 avatar parameters!** You have a total of 128 bits for parameters.
	+ Using an `int` or `float` parameter will use up 8 bits of space. This means you can use up to 16 parameters if you only use these types.
	+ Using a `bool` parameter will only use up 1 bit of space. This mean you can use up to 128 parameters if you only use this type.
* The `VRCParameterDriver` [State Behavior](/docs/state-behaviors) now has the ability to add to or subtract from a parameter. You can also pick a random value between a minimum and maximum value you set.


#### AV3 Changes Note:


A change made to AV3 systems for the continued development of features has resulted in the loss of some unsupported functionality. In particular, the ability of a second sub-animator using a `VRCParameterDriver` state behavior to trigger the change of a parameter on the main avatar animator will no longer function.


This behavior was not intended and out of scope of the functionality of the state behavior. This change will not be reverted. It did not appear to be in heavy use, but some advanced AV3 creators were using it for their avatar's functionality.


*That being said,* we very much realize that this behavior is desired and makes some **REALLY COOL** stuff possible. We'll keep it in mind going forward with the implementation of future systems, and will use this desire to measure what we should be working on next. No promises, but we know that you want this kind of stuff.


Thank you to our AV3 creators for exploring the boundaries of the system. We have to keep moving forward, but knowing that you used this functionality for some very advanced AV3 behavior will help us drive our path forward with AV3 development.


# Udon Graph


* You can now set the Interaction Text and Proximity on UdonBehaviors without switching to Debug mode
* Fix for multiple Set Variable nodes. You can now use the fields in the nodes themselves to set values without overwriting other copies of that Set Variable node.
* Fix for `VRCUrl` variables not being editable
* Udon Graph Variables will ensure that their names are unique when you create or rename them in the variables window, or when you paste them into the graph
* Added "VideoError" nodes so you can figure out which error you got from a video player and handle it properly.


# Udon


* Update order can now be set for each program. The option to set it can be found in the settings menu in the graph window, or the program source's inspector. Lower values run before higher values.
* Missing classes have been exposed to Udon. Not all methods are available yet:
	+ `ReflectionProbe`
	+ `OcclusionPortal`
	+ `Gradient`
	+ `AnimationCurve`
	+ `CultureInfo`
	+ `StopWatch`
	+ `GeometryUtility`
* Reduced the cost of `UdonBehavior.RunProgram(string eventName)` when the program has many exported events.
* Optimized how `UdonBehavior.Update/LateUpdate/FixedUpdate` events are run to eliminate the overhead of processing these calls for UdonBehaviors whose program does not export these events


# SDK 2/3


* These VRChat Control Panel Settings are now saved properly so they stay even after closing Unity:
	+ Force Non-Vr
	+ Number of Clients
	+ Show Extra Options


# Midi System


* The MIDI driver only loads if you visit an SDK2 world with MIDI features, and unloads when you leave that world.
* New launch flag `--midi=deviceName` will search for a connected MIDI device which contains the name you supply, including partial matches. Case-insensitive.
* Midi system only connects to one device-- either the first one that Windows lists, or the one specified by the launch flag given above


# Client Changes and Fixes


* Fixed an issue where players were unable to make instances for worlds with a user cap of 1
* Fixed an issue where jawflap visemes would get stuck open locally
* Graphics backend optimizations that may help improve performance. Testing showed an improvement in frame times of 20-30%, depending on your system's setup. If you are CPU-bound (and have GPU room to spare), you are likely to see the most benefits. If you are not CPU-bound but are instead GPU-bound, it is unlikely you'll see much improvement.
* Safety and security changes and fixes
Updated over 1 year ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Avatars 3.0](#avatars-30)
	+ [Udon Graph](#udon-graph)
	+ [Udon](#udon)
	+ [SDK 2/3](#sdk-23)
	+ [Midi System](#midi-system)
	+ [Client Changes and Fixes](#client-changes-and-fixes)
