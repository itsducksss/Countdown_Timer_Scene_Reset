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
To start this tutorial, we will need to create a new Unity Project. To the Unity scene we will add a Plane to represent the floor, and 2 3 cubes scaled to size to represent the wall and the door, as well as a movable capsule to represent the player.
![image](https://github.com/user-attachments/assets/fab3d17b-80bd-486e-9e0d-1f3829155878)![image](https://github.com/user-attachments/assets/cc63c2d9-5de6-46e2-9fa6-e17418c33c84)

in the scene we have a plane in the scene to represent the floor, with a mesh collider so that it is able to act as a floor, and so that the player can move on the plane.
![image](https://github.com/user-attachments/assets/13ad3d45-4af0-4831-86f7-86e558ce25bc)

We then add in cube and scale that to look like a wall using the "r" key on the keyboard and adjust as wanted. This can then add a box collider onto it then duplicate twice to create the door and the walls for the scene.
![image](https://github.com/user-attachments/assets/a6c39aab-d6ef-4e9d-a61c-3e182283d8f8)

The door for this tutorial will be coded with the colour blue so that it is easy to identify and correspond with the colour of the key for this tutorial.
![image](https://github.com/user-attachments/assets/1b8a0104-9c66-41bb-ab9d-f9c991995153)![image](https://github.com/user-attachments/assets/23cf39f4-108e-4eb0-8a34-3dfc299ae6e5)

We will then create an empty and move it so that it is located between edge of the wall and the door.
![image](https://github.com/user-attachments/assets/94825b9a-033c-469a-9ea5-ba8ac8be60b0)

We will then rename the objects in the heirarchy. The cubes not coloured in blue will be called the walls. The blue cube will be called the door in the heirarchy. The empty we just made will be calle the hinge, as it will have the functionality of a hinge.
![image](https://github.com/user-attachments/assets/37854cd0-e4ad-43ae-b1fd-d81eb14c989c)

We then make the door the child of the Hinge empty.
