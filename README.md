# Key-and-Door-System

# Prerequisites
Before approaching this tutorial, you will need a current version of Unity and a code editor (such as Microsoft Visual Studio Community) installed and ready to use.

This tutorial was created with Unity 2022.3 LTS and Microsoft Visual Studio Community 2022 versions. It should work with earlier or later versions. But you should check the release notes for other versions as the Editor controls or Scripting API functions may have changed. This is as the changes in the updates can cause errors to occur that may have been fixed or changed within different versions of the Unity and Visual Studio softwares.

If you need help installing Unity you can find many online tutorials such as: https://learn.unity.com/tutorial/install-the-unity-hub-and-editor

You will also need to know how to create an empty project, add primitive objects to your scene, create blank scripts, and run projects from within the editor. If you need help with this, there is a short video demonstrating how to do all of these things here:

https://www.youtube.com/watch?v=eQpWPfP1T6g

In this tutorial we will be importing TextMeshProEssentials Unity Package which will be shown in the tutorial.

# Primary Objectives
This tutorial aims to create a simple interactable key and door system, which means that if a key is picked up by the player the door will open with that key. 

# Preview



# Getting Started
To start this tutorial, we will need to create a new Unity Project.

![image](https://github.com/user-attachments/assets/2b494d4b-da21-495e-8f42-6b9be4f2bc62)

We will first add a TextMeshPro item by right clicking onto the hieracrhy. It whould be under the UI selection as seen in the image above, Once we add this into our project, Unity will then ask if we want to add addition packages for the TextmeshPro to function properly and help prevent any errors in the future, which is why we should import them as early on in the project as possible. Once we add them the TextmezshPro will then be underneath the Canvas item that was just added when we added and ceated the TextMeshPro onto the scene. We then rename the TextMeshPro as Timer so that it is easier to find later in the line. 

![image](https://github.com/user-attachments/assets/2d1012dd-3bb7-4694-b132-9cac0eec3fed)

We the go into the Canvas in the Hierarchy and add a script which we will name as Timer. Double click on the script and it should open up the visual Studio Program on your device.

![image](https://github.com/user-attachments/assets/28b475ab-b057-4cce-b506-77a19d8212b5)

Once opened we will the add the line is using TMPro; line which will allow us to use the parts within the TMPro package when doing the timer for the scene.

This script just means that the on the TextmeshPro (TMPro) object we renamed as timer, it will use the TMPro to display the text which we have stated in the script to be the time that has elapsed when we play the scene.

Once we get this working to show the basic functionality of a timer, we then go back into teh script and change the elapsedTime into remainingTime throughout the script. We then also change the += into a -+ which just means that instead of going up the timer will count down which is what we want.




