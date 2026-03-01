![Internship Project](https://img.shields.io/badge/Internship-E6007A?style=for-the-badge&logoColor=white)
![Showcase](https://img.shields.io/badge/Showcase_Video_Only-E6007A?style=for-the-badge&logoColor=white)

![Built with Unity](https://img.shields.io/badge/Unity-000000?logo=unity&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?logo=csharp&logoColor=white)
![Built for VR](https://img.shields.io/badge/VR-0055FF?logo=steamvr&logoColor=white)
![Built for VR](https://img.shields.io/badge/MetaQuest3-0055FF?logo=meta&logoColor=white)
![Built for VR](https://img.shields.io/badge/Convai-226039?logo=convai&logoColor=white)

# Finnish Hotel Of Tomorrow 2.0
# $${\color{red}Showcase \space only, \space source \space code \space is \space not \space publicly \space available!}$$

***FHOT 2.0*** is a virtual reality hotel simulation I developed for **Meta Quest 3** during my internship at the ***[Helsinki XR Center](https://helsinkixrcenter.com/)***. It is a continuation of my first project, [FHOT 1.0](https://www.youtube.com/watch?v=HzUbI3jcV24), with an expanded environment, interactions, and AI-driven interactive NPCs.

[Demo Video](https://github.com/user-attachments/assets/7e26f8d1-ac0b-47f4-90e2-99451f942117)

## Key Features
- **Interactive Robots:** Tutorial, Waiter (Delivery/Pickup), and Info robots with Convai dialogue.
- **Phone UI:** Central interaction system that lets players:
  - Control room settings (room modes, lights, blinds, audio, scenery)
  - Interact with robots and track them on the mini map
  - Order food and pay for services
  - Book sauna sessions
- **Room Modes:** Work, Relax, Sleep, or custom configurations that persist across sessions.
- **NPC Conversations:** Player-to-NPC interactions powered by Convai SDK.

## Technologies
- Unity 2022.3.42f1 LTS
- Meta XR SDK v76 (for Quest 3 VR functionality)
- Convai SDK v3.2.4 (for AI-powered NPC dialogue)

## Script structure
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
