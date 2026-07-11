# Unity Triggering Events

This project is a Unity 6 demo/prototype for trigger-driven gameplay events.  
It provides a small scene (`SampleScene`) where colliders fire UnityEvents on trigger enter, with optional filtering so only objects with allowed `ObjectID` values activate the trigger.

## What the project provides

The core scripts in `DM-Production-Week2/Assets/Scripts` implement:

1. `ActivateTriggerOnEnter`  
   Raises a `UnityEvent<GameObject>` when an object enters a trigger.  
   Supports:
   - optional filtering by `ObjectID`
   - selecting whether the collider object or trigger object is passed to event listeners

2. `MoveObjectToPosition`  
   Caches and restores a target object's position and rotation (useful for respawn/teleport behavior).

3. `TriggerReceiver`  
   Example event receiver methods that log received trigger events/objects.

4. `ObjectID`  
   A lightweight integer ID component used by trigger filtering.

The sample scene is set up with first-person controller assets so you can move through the level and interact with trigger volumes to drive these events.

## Unity version

- `6000.0.58f2`

## Project structure

- Unity project root: `DM-Production-Week2/`
- Scene: `DM-Production-Week2/Assets/Scenes/SampleScene.unity`
- Scripts: `DM-Production-Week2/Assets/Scripts/`
