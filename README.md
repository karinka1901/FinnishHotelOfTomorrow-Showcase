![Internship Project](https://img.shields.io/badge/Internship-E6007A?style=for-the-badge&logoColor=white)
![Showcase](https://img.shields.io/badge/Showcase_Video_Only-E6007A?style=for-the-badge&logoColor=white)

![Built with Unity](https://img.shields.io/badge/Unity-000000?logo=unity&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?logo=csharp&logoColor=white)
![Built for VR](https://img.shields.io/badge/VR-0055FF?logo=steamvr&logoColor=white)
![Built for VR](https://img.shields.io/badge/MetaQuest3-0055FF?logo=meta&logoColor=white)
![Built for VR](https://img.shields.io/badge/Convai-226039?logo=convai&logoColor=white)

# Finnish Hotel Of Tomorrow 2.0

> **⚠️ Showcase only, source code is not publicly available.**


***Finnish Hotel of Tomorrow*** is a virtual reality hotel simulation I developed for **Meta Quest 3** during my internship at the ***[Helsinki XR Center](https://helsinkixrcenter.com/)***. 

FHOT 2.0 is a continuation of my first project, [FHOT 1.0](https://www.youtube.com/watch?v=HzUbI3jcV24), with an expanded environment, new and improved interactions, and AI-driven NPCs. While it builds on the original concept, the project was rebuilt from the ground up from a code perspective during migration to the Meta XR SDK.

[Demo Video](https://github.com/user-attachments/assets/7e26f8d1-ac0b-47f4-90e2-99451f942117)

*Note: Demo footage shortened to fit a 2-minute showcase limit.*

## Overview
**Role:** Unity Developer  
**Duration:** May – July 2025  
**Team:** 4 people (1 developer, 1 artist, code lead, art lead)  
**Engine:** Unity  
**Platform:** Meta Quest 3

## My Role
In this project I was responsible for implementing the core gameplay and interaction systems of the VR application in Unity.

While the visual assets were created by artists on the team, I developed the gameplay systems and interaction logic and integrated them into the final experience.

## Key Features

- **Interactive Tutorial:** A multi-step tutorial system guiding the player through phone usage, locomotion, and robot interaction.
- **Interactive Robots:** Tutorial, Waiter (delivery and pickup), and Info robots with Convai-powered dialogue.
- **NPC Conversations:** Player-to-NPC interactions powered by the Convai SDK.

- **Phone UI:** A central interaction system that allows players to:
  - Control room settings (room modes, lights, blinds, audio, scenery)
  - Interact with robots and track them on the minimap
  - Order food and pay for services
  - Book sauna sessions
 
- **Room Modes:** Preset configurations such as Work, Relax, and Sleep, with support for custom configurations that persist across sessions.

- **Navigation System:** Phone-based navigation that displays an AR-style guidance path on the in-game phone to direct players to selected destinations.

- **Configurable Locomotion:** Player movement options including teleport, smooth locomotion, snap turn, and smooth turn with saved user preferences.

- **Scene and Game State Management:** Systems controlling scene transitions, player spawning, tutorial progression, and feature availability across lobby, hotel room, and sauna scenes.

## Project Structure
```text
Scripts
├── Audio
│   ├── AudioController.cs
│   ├── HotelRoomAudioController.cs
│   ├── LobbyAudioController.cs
│   ├── PhoneSFXController.cs
│   └── RobotSFXController.cs
│
├── General
│   └── HotelRoom
│       ├── RoomModeSettings
│       │   ├── BlindsController.cs
│       │   ├── LightController.cs
│       │   ├── LightToggle.cs
│       │   ├── RoomModeController.cs
│       │   ├── RoomModeSaveData.cs
│       │   ├── SceneryController.cs
│       │   └── SofaController.cs
│       │
│       ├── DisableCamera.cs
│       ├── DoorController.cs
│       ├── DoorLockController.cs
│       ├── GameObjectHolder.cs
│       ├── HallwayEntrySensor.cs
│       ├── ItemInteractions.cs
│       ├── RoomEntrySensor.cs
│       └── RoomExitTriggers.cs
│
├── Lobby
│   ├── BarTableInteractions.cs
│   ├── CheckinController.cs
│   └── LobbySceneInitialiser.cs
│
├── Player
│   ├── LobbySpawnPointSetter.cs
│   ├── LocomotionSaveData.cs
│   ├── LocomotionSettings.cs
│   ├── PhoneSpawner.cs
│   ├── PlayerSpawnLocation.cs
│   └── SpawnRecenter.cs
│
├── Robot
│   ├── InfoJob.cs
│   ├── IRobotJob.cs
│   ├── LobbyWaiterJob.cs
│   ├── RobotController.cs
│   ├── RobotFaceController.cs
│   ├── RobotTalkState.cs
│   ├── RoomWaiterJob.cs
│   └── TutorialJob.cs
│
├── Scenes
│   ├── SceneLoader.cs
│   └── SceneTypeManager.cs
│
├── Tutorial
│   ├── PhoneTutorialState.cs
│   ├── TutorialAreaTrigger.cs
│   └── TutorialController.cs
│
├── UI
│   ├── CameraNavigator.cs
│   ├── CustomPopup.cs
│   ├── MinimapController.cs
│   ├── PhoneUIElements.cs
│   ├── PhoneUIManager.cs
│   └── RobotDisplayController.cs
│
├── Utilities
│   ├── CameraWallDetection.cs
│   ├── CharacterIdSwitcher.cs
│   ├── DebugColor.cs
│   ├── HapticFeedback.cs
│   ├── OnGrabDisableTeleportation.cs
│   ├── StartupPermissionManager.cs
│   └── TalkController.cs
│
├── MenuController.cs
└── SaunaBookingController.cs
```
## System Architecture

The project is built around several core systems:

- **SceneTypeManager** – controls global game state and scene-specific behaviour.
- **RobotController** – manages robot spawning, navigation, and job logic.
- **PhoneUIManager** – central hub for player interactions.
- **MenuController** – handles food and drink ordering and robot service logic.
- **RoomModeController** – manages room presets and environment configuration.

  
## Technologies
- Unity 2022.3.42f1 LTS
- Meta XR SDK v76 (for Quest 3 VR functionality)
- Convai SDK v3.2.4 (for AI-powered NPC dialogue)
