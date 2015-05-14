# spacepuppy-unity-framework
A framework of reusable objects with the Unity game engine version 4.x.

This project is intended to be compiled in Visual Studio and then place the compiled dll's into the project. When compiling you will need to ensure you reference the UnityEngine and UnityEditor dll's for your version of unity. I include a version list in the Resources folder for the version of unity I'm currently using.

I usually create a folder Assets/3rdParty/SpaceuppyUnityFramework. The SpacepuppyUnityFramework dll and .mdb go in there (a .pdb will also be generated by unity, this will allow for code stepping when debugging). I then create a folder Assets/3rdParty/SpaceuppyUnityFramework/Editor and place the SpacepuppyUnityFrameworkEditor dll and .mdb there.

You will also want to go to the PlayerSettings and set the Api compatability level to .Net 2.0, and not 2.0 subset.

Lastly you'll want to set the execution order of 3 classes in the framework. Of course, if you have meta files turned on, you could just include the supplied SpacepuppyUnityFramework.dll.meta file instead (found in the Resources folder). Those 3 classes are:

com.spacepuppy.GameLoopEntry : -32000

com.spacepuppy.Hooks.EarlyExecutionUpdateEventHooks : -31999

com.spacepuppy.Hooks.TardyExecutionUpdateEventHooks : 32000
