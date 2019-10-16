---
title: "Unity Tutorials"
language: "en"
previous: "minitalks.html"
---

# Unity Tutorials

Below are some of resources to help build your games in Unity.

## Unity Workshop 2018

Mindsports had a Unity Workshop that covers a step-by-step tutorial on basic mechanis for a 2D Shooter game (except for Week 2 which quickly covers Unity3D).

It's available in Google Drive in https://drive.google.com/drive/folders/1uTiyEkhv9kkRYSSrA92GQp86sT6FpDko.

## Unity FAQ

A list of FAQ compiled by your mentors.

Live version available in [Google Docs](https://docs.google.com/document/d/1IGY36hnK-_QpNHj6nkQM8WFvR3IMH_tRRrAAK2Zu1Lg/).

* [_Debugging_](#debugging) 
* [_Need access to some other game objects?_](#need-access-to-some-other-game-objects) 
* [_I saw `[SerializeField]`, what is it?_](#i-saw-serializefield-what-is-it)
* [_Player Movement_](#player-movement)
* [_Looping Background_](#looping-background)
* [_Oh no, what is prefab?_](#oh-no-what-is-prefab)
* [_2D Movement (Enemy)_](#2d-movement-enemy)
* [_Rotation?_](#rotation)
* [_Layer Based Collision_](#layer-based-collision)
* [_Why Code When You Can Copy_](#why-code-when-you-can-copy)


### _Debugging_

I present your _**best friend**_:


```c#
Debug.Log("I am alive!");
```
_Note_: do this only when you need to, like something not behaving correctly, use this to print out your variables' values, or use this to know whether your function is called or not

### _Need access to some other game objects?_

Finding a game object by **tag** or **name** might be useful.

https://docs.unity3d.com/2019.3/Documentation/Manual/ControllingGameObjectsComponents.html

### _I saw `[SerializeField]`, what is it?_

It is to make private variables visible in the inspector (the column on the right).

![Inspector Location](https://docs.unity3d.com/uploads/Main/InspectorWindowCallout.jpg)

To make a variable in a Component visible, you can either make it public:
```c#
public int health = 100;
```
or use `[SerializeField]`
```c#
[SerializeField]
private int health = 100;
```

Source: https://forum.unity.com/threads/when-to-use-serializefield-and-why.184687/#targetText=Serialization%20is%20the%20process%20of,it's%20state%20to%2Ffrom%20disk

About Inspector: https://docs.unity3d.com/Manual/UsingTheInspector.html

### _Player Movement_

Source: https://docs.unity3d.com/ScriptReference/Input.html

#### Keyboard Controls

|Code|Explanation|
|-|-|
|`Input.GetKey` |Returns true while the user **holds down** the key identified by name. |
|`Input.GetKeyDown`|Returns true during the frame the user **starts pressing down** the key identified by name.|
|`Input.GetKeyDown`|Returns true during the frame the user **releases** the key identified by name.|


#### Mouse Controls

|Code|Explanation|
|-|-|
|`Input.GetMouseButton`|Returns whether the given mouse button is **held down.**|
|`Input.GetMouseButtonDown`|Returns true during the frame the user **pressed** the given mouse button.|
|`Input.GetMouseButtonUp`|Returns true during the frame the user **releases** the given mouse button.|

### _Looping Background_

Good for top-down shooter / infinite run kind of game
https://learn.unity.com/tutorial/live-session-making-a-flappy-bird-style-game#5c7f8528edbc2a002053b69e


### _Oh no, what is prefab?_

https://docs.unity3d.com/Manual/Prefabs.html

Tl;dr, prefab = original copy of the game object, can be duplicated, if its component/properties are changed, every duplicate of it will change according to it.

**How to make prefab?** Drag the game object to your resources (the section below)

### _2D Movement (Enemy)_

https://www.youtube.com/watch?v=dwcT-Dch0bA

https://docs.unity3d.com/ScriptReference/Transform.html


### _Rotation?_

Good luck differentiating and learning [Quaternion](https://en.wikipedia.org/wiki/Quaternion) and [Euler](https://en.wikipedia.org/wiki/Euler_angles) in unity.

https://docs.unity3d.com/Manual/QuaternionAndEulerRotationsInUnity.html

https://docs.unity3d.com/ScriptReference/Transform.Rotate.html

https://docs.unity3d.com/ScriptReference/Transform-rotation.html

### _Layer Based Collision_

So that your enemies’ projectiles don’t hit the enemies (no friendly fire)

https://docs.unity3d.com/Manual/LayerBasedCollision.html

### _Why Code When You Can Copy_

**First-Person Controller**: https://docs.unity3d.com/Manual/class-CharacterController.html

**Navigation AI** (NavMesh): https://docs.unity3d.com/Manual/nav-Overview.html

![navmesh](https://docs.unity3d.com/uploads/Main/NavMeshAgentSetup.svg)
