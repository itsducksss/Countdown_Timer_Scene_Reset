# CountDown Timer Reset Scene

# Prerequisites
Before approaching this tutorial, you will need a current version of Unity and a code editor (such as Microsoft Visual Studio Community) installed and ready to use.

This tutorial was created with Unity 2022.3 LTS and Microsoft Visual Studio Community 2022 versions. It should work with earlier or later versions. But you should check the release notes for other versions as the Editor controls or Scripting API functions may have changed. This is as the changes in the updates can cause errors to occur that may have been fixed or changed within different versions of the Unity and Visual Studio softwares.

Code was taken from:
[Timer](https://www.youtube.com/watch?v=POq1i8FyRyQ)
[restart scene](https://discussions.unity.com/t/how-to-restart-scene-properly/118396/3)

If you need help installing Unity you can find many online tutorials such as: https://learn.unity.com/tutorial/install-the-unity-hub-and-editor

You will also need to know how to create an empty project, add primitive objects to your scene, create blank scripts, and run projects from within the editor. If you need help with this, there is a short video demonstrating how to do all of these things here:

https://www.youtube.com/watch?v=eQpWPfP1T6g

In this tutorial we will be importing TextMeshProEssentials Unity Package which will be shown in the tutorial.

# Primary Objectives
This tutorial aims to create a simple timer that when it reaches 0;00 the scene will reset.

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

This script just means that the on the TextmeshPro (TMPro) object we renamed as timer, it will use the TMPro to display the text which we have stated in the script to be the time that has elapsed when we play the scene.
![image](https://github.com/user-attachments/assets/90d67810-2dd9-4418-9a41-d27248cfbd4c)

Once we get this working to show the basic functionality of a timer, we then go back into teh script and change the elapsedTime into remainingTime throughout the script. We then also change the += into a -+ which just means that instead of going up the timer will count down which is what we want as seen above.

https://github.com/user-attachments/assets/5a74081b-36fa-4ba9-b640-60ccd242169f

When we play the scene this should occur (video above).

https://github.com/user-attachments/assets/15471615-12e9-4b34-8232-0bd2ba1f00bd

the problem is that when the countdown reachers past 0:00 this will occur seen in the video above. To solve this we will adjust the script.

![image](https://github.com/user-attachments/assets/f098f676-be40-42a1-bf08-b214d9c19adb)

The changes in the script just means that if the time is less than 0 then that the time should not go past 0:00.


https://github.com/user-attachments/assets/e07a5af7-efe7-4fbc-ace6-8ea30d0a9c2f

This just shows that the Time will just stay at 0 instead of counting down further.

![image](https://github.com/user-attachments/assets/aeb08fc8-b67d-4d60-ba51-fda3cd05a9cf)

These are the changes that I added onto the if statement which just allows the scene to reset which are on lines 5, and 22. This just means that it will use the Unity's Scene management to reset the scene.


