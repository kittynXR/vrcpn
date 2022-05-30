# VRChat 2022.1.2p4

Release - 4 May 2022 - Build 1194

[Suggest Edits](/edit/vrchat-202212p4)# Client


## Changes, Fixes, and Improvements


* PhysBones that were converted from Dynamic Bones are now treated as having sphere colliders when colliding with converted Dynamic Bone colliders
	+ This fix should help many Dynamic Bone conversions, such as avatars that look like they had hair "sticking out" of their head collider
	+ See the SDK patch notes for more details
* Some further logging reductions
* Improvements to fix more cases where the audio bug would pop up
* Safety and security fixes


# SDK


## Changes, Fixes, and Improvements


* Implemented **Immobile Mode** for `PhysBone` components
	+ This option switches how the "Immobile" factor works
	+ If set to **All Motion**, Immobile reduces any motion as calculated from the root transform's parent
		- This is the **default mode** for new PhysBones and converted Dynamic Bones
		- In this mode all PhysBone movement in either scene-space or playspace will be dampened by the Immobile factor
	+ If set to **World (Experimental)**, Immobile negates only positional movement from the reference of the scene root transform. Motion via animation or IK still affects the bones normally. *This mode may change in the future!*
	+ This means that moving around in your playspace will still affect your PhysBones' movement as normal, but locomoting (pushing on your joystick to move) will have its movement dampened by the Immobile factor
* **Sphere Colliders:** Added the `bonesAsSpheres` option for `PhysBoneCollider` components, which changes how colliders treat interactions with PhysBones
	+ If enabled on a collider, that collider will treat any bones it interacts with as spheres, using the `radius` defined on the PhysBone
	+ This does not affect grabbing and automatically-generated hand colliders. Those still treat bones as capsules, to preserve behavior
Updated 25 days ago 



---

Did this page help you?YesNo* [Table of Contents](#)
* + [Client](#client)
		- [Changes, Fixes, and Improvements](#changes-fixes-and-improvements)
	+ [SDK](#sdk)
		- [Changes, Fixes, and Improvements](#changes-fixes-and-improvements-1)
