# CountDown Timer Reset Scene
Description
This tutorial will show how to make a basic countdown timer, as well as show how to change the code so that it has the ability to reset the scene once the timer ends.

# Prerequisites
Before approaching this tutorial, you will need a current version of Unity and a code editor (such as Microsoft Visual Studio Community) installed and ready to use.

This tutorial was created with Unity 2022.3 LTS and Microsoft Visual Studio Community 2022 versions. It should work with earlier or later versions. But you should check the release notes for other versions as the Editor controls or Scripting API functions may have changed. This is as the changes in the updates can cause errors to occur that may have been fixed or changed within different versions of the Unity and Visual Studio softwares.

Code was taken from:
[Timer](https://www.youtube.com/watch?v=POq1i8FyRyQ), [restart scene](https://discussions.unity.com/t/how-to-restart-scene-properly/118396/3)

If you need help installing Unity you can find many online tutorials such as: https://learn.unity.com/tutorial/install-the-unity-hub-and-editor

You will also need to know how to create an empty project, add primitive objects to your scene, create blank scripts, and run projects from within the editor. If you need help with this, there is a short video demonstrating how to do all of these things here:

https://www.youtube.com/watch?v=eQpWPfP1T6g

In this tutorial we will be importing TextMeshProEssentials Unity Package which will be shown in the tutorial.

# Primary Objectives
This tutorial aims to create a simple timer that when it reaches 0:00 the scene will reset.

# Preview

https://github.com/user-attachments/assets/d14152d9-4063-4afa-932a-fd940ce7eb51

# Getting Started
To start this tutorial, we will need to create a new Unity Project.

![image](https://github.com/user-attachments/assets/2b494d4b-da21-495e-8f42-6b9be4f2bc62)

We will first add a TextMeshPro item by right clicking onto the hieracrhy. It whould be under the UI selection as seen in the image above, Once we add this into our project, Unity will then ask if we want to add addition packages for the TextmeshPro to function properly and help prevent any errors in the future, which is why we should import them as early on in the project as possible. Once we add them the TextmezshPro will then be underneath the Canvas item that was just added when we added and ceated the TextMeshPro onto the scene. We then rename the TextMeshPro as Timer so that it is easier to find later in the line. 

![image](https://github.com/user-attachments/assets/2d1012dd-3bb7-4694-b132-9cac0eec3fed)

We the go into the Canvas in the Hierarchy and add a script which we will name as Timer. Double click on the script and it should open up the visual Studio Program on your device.

![image](https://github.com/user-attachments/assets/28b475ab-b057-4cce-b506-77a19d8212b5)

Once opened we will the add the line is using TMPro; line which will allow us to use the parts within the TMPro package when doing the timer for the scene.

![image](https://github.com/user-attachments/assets/886aa93f-0c6f-4929-be44-1ac001484840)



https://github.com/user-attachments/assets/39c1dd36-c09a-48e5-b74d-e19e98ac1921

Video just shows how the script will look like when added onto the canvas.

This script just means that the on the TextmeshPro (TMPro) object we renamed as timer, it will use the TMPro to display the text which we have stated in the script to be the time that has elapsed when we play the scene.
![image](https://github.com/user-attachments/assets/90d67810-2dd9-4418-9a41-d27248cfbd4c)
-  using [insert system] means that it can refer to that specific system and its properties when coding using references made to a specific system
-  : means this class inherits functions and variables from another class
-  [Monobehaviour](https://docs.unity3d.com/ScriptReference/MonoBehaviour.html) refers Unity supplied class that attaches directly to [GameObjects](https://docs.unity3d.com/ScriptReference/GameObject.html), which we base a new class onto.
-  [Serialize Field](https://docs.unity3d.com/ScriptReference/SerializeField.html) helps to make the private variables accessible within the Unity editor without making them public, as well as helps to make serialize any private variable.
-  [TextMeshProUI]() just refers to the TextMeshPro attachment we added which will be used for the UI text which in the code will be called timerText;
-  float refers to a numerical value that can be assigned (whole or decimal).
-  [void](https://discussions.unity.com/t/what-does-void-mean-when-in-front-of/23128) refers to a function can return normally without the need of a value.
-  [update](https://docs.unity3d.com/ScriptReference/PlayerLoop.Update.html) means a function that gets called every frame if the MonoBehaviour is enabled.
-  int just refers variable that stores whole numbers (integers shortened to int) without decimals.
-  [Mathf](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Mathf.html)
-  [Mathf.FloorToInt](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Mathf.FloorToInt.html)
-  timerText.text just means that the text will change using the timerText which is the TextMeshPro. timerText is a reference to TextMeshPro and the .text just means that it will change the text itself.
-  [string](https://docs.unity3d.com/560/Documentation/ScriptReference/String.html) this refers ta sequence of characters.
-  Format ("{0:00};{1:00}") this just means that the timer's text will show up in this format for the timer.


Once we get this working to show the basic functionality of a timer, we then go back into the script and change the elapsedTime into remainingTime throughout the script. We then also change the += into a -+ which just means that instead of going up the timer will count down which is what we want as seen above.

https://github.com/user-attachments/assets/5a74081b-36fa-4ba9-b640-60ccd242169f

When we play the scene this should occur (video above).

https://github.com/user-attachments/assets/15471615-12e9-4b34-8232-0bd2ba1f00bd

the problem is that when the countdown reachers past 0:00 this will occur seen in the video above. To solve this we will adjust the script.

![image](https://github.com/user-attachments/assets/f098f676-be40-42a1-bf08-b214d9c19adb)
- if() is an if statement which is used to help show if a block of code can be exectuted if specified conditions is true.
- [Time.deltaTime](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Time-deltaTime.html) is the completion time in seconds since the last frame. This is used in games to help make the game run nicely on different compters with different specs.
The changes in the script just means that if the time is less than 0 then that the time should not go past 0:00.


https://github.com/user-attachments/assets/e07a5af7-efe7-4fbc-ace6-8ea30d0a9c2f

This just shows that the Time will just stay at 0 instead of counting down further.

![image](https://github.com/user-attachments/assets/aeb08fc8-b67d-4d60-ba51-fda3cd05a9cf)

These are the changes that I added onto the if statement which just allows the scene to reset which are on lines 5, and 22. This just means that it will use the Unity's Scene management to reset the scene.
- using UnityEngine.SceneManagement; just means that the code will utilise Unity's SceneManagement system in the script.
- [SceneManager](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/SceneManagement.SceneManager.html) this just allows you toorganise and move from scene to scene in Unity when you play.
- [LoadScene("")](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/SceneManagement.SceneManager.LoadScene.html) this means that unity will load "this scene", which in thois case is the SampleScene.

https://github.com/user-attachments/assets/d14152d9-4063-4afa-932a-fd940ce7eb51
We then add the current scene we have onto the build settngas and change the name in LoadScene("") to the name of your scene mine in SampleScene if yours is level1 it would lok like this LoadScene("level1"). You can then see how the scene resets wghen I move the green capsule.
