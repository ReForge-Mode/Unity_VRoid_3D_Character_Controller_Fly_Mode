# Unity VRoid 3D Character Controller + Fly Mode
This project will show you how to use VRoid Studio model with the "3rd Person Controller + Fly Mode" asset by Vinicius Marques in Unity Asset Store. This project uses Unity version 2021.2.3f1, earlier versions of Unity might not work. Keep in mind that this controller uses the Old Input System. Information on how to change input system is in Step 1 below.

I made this project to help with those who want to make Anime-looking game and learning to use the free character controller made by Vinicius Marques.

Huge credit to these guys who made this possible!
- UniVRM plugin: https://github.com/vrm-c/UniVRM
- Unity Starter Assets - Third Person Character Controller: https://assetstore.unity.com/packages/essentials/starter-assets-third-person-character-controller-196526
- 3rd Person Controller + Fly Mode: https://assetstore.unity.com/packages/templates/systems/3rd-person-controller-fly-mode-28647

# Instructions
This 3D controller is a lot easier to implement with VRoid models than the Unity Starter Assets.

If you want to start fresh, you can just create a basic 3D project from Unity Hub, import the Character Controller Starter Assets and 3rd Person Controller asset from Unity Asset Store, then import UniVRM plugin and your character. If you don't know how to import your VRoid character to Unity, I have a tutorial about it in here: https://www.youtube.com/watch?v=IrIn9wRYqUI

Now, to use this character controller to your VRoid project:
1. After you import all plugins to your project, make sure that you're using the Old Input System. For the sake of comparison, we're using both Unity Starter Assets and the Fly Mode one. They are using a different input system. If you want to change it, Go to Edit > Project Settings > Player. In "Configuration", select Active Input Handling and change "Input Manager (Old)" to "Both". If you can't find it, you can search for it with the search box on the project settings window.
<p align="center"><img src="https://github.com/FFaUniHan/Unity_VRoid_3D_Character_Controller_Fly_Mode/blob/main/1.png" width=100% height=100%></p>

2. Drag the "shadow" player prefab to the scene window from the project window in 3rdPerson+Fly > Prefabs. Now also drag Vita prefab (VRoid model) to the scene 
<p align="center"><img src="https://github.com/FFaUniHan/Unity_VRoid_3D_Character_Controller_Fly_Mode/blob/main/2.png" width=80% height=80%></p>

3. Unpack all Prefab for both Vita and shadow
<p align="center"><img src="https://github.com/FFaUniHan/Unity_VRoid_3D_Character_Controller_Fly_Mode/blob/main/3.png" width=100% height=100%></p>

4. Duplicate shadow and hide the original. We're going to move child object and components from shadow to Vita.
<p align="center"><img src="https://github.com/FFaUniHan/Unity_VRoid_3D_Character_Controller_Fly_Mode/blob/main/4.png" width=50% height=50%></p>

5. Move "Main Camera" object from "shadow" to Vita as a child object. 
<p align="center"><img src="https://github.com/FFaUniHan/Unity_VRoid_3D_Character_Controller_Fly_Mode/blob/main/5.png" width=50% height=50%></p>

6. Then, in the "Main Camera" object, in the component "Third Person Orbit Cam Basic (Script)", change the "Player" field to Vita. You can also drag and drop Vita object from the Hierarchy Window to this field
<p align="center"><img src="https://github.com/FFaUniHan/Unity_VRoid_3D_Character_Controller_Fly_Mode/blob/main/6.png" width=50% height=50%></p>

7. Move every component from "shadow" to Vita, except for the Animator. For the Animator, just change the Controller field used in Vita to the one that is used by "shadow". The animation will work with the VRM object. You can copy component that you can't move (Rigidbody and Collider) and paste it on Vita.

And that will be it! You can now delete the duplicate of "shadow". Let me know if you guys want a video tutorial instead of a written tutorial. If there's enough request, I'll make the short tutorial for it.
