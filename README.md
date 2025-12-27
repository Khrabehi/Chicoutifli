# Chicoutifli

A 3D action-adventure game created during the Winter 2024 Game Jam at Chicoutimi, Canada.

![Unity](https://img.shields.io/badge/Unity-2021.3+-black.svg?style=flat-square&logo=unity)
![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=c-sharp)
![Game Jam](https://img.shields.io/badge/Game%20Jam-48h-orange?style=flat-square)

## 📖 Context

This game was developed in **2 days** during the **Winter 2024 Game Jam** held in Chicoutimi, Quebec, Canada. It was created as part of my bachelor's degree program in Video Game Development.

## 👥 Team

The game was brought to life by a talented team of **6 members**:
- **4 Developers** - Programming, gameplay mechanics, and systems implementation
- **2 Artists** - 3D assets, animations, VFX, and visual design

## 🎮 Game Overview

Chicoutifli is a 3D action game where players navigate through multiple levels fighting mutant enemies. The game features a unique syringe selection mechanic where players must choose different syringes with varying stats from a pharmacist character to progress through increasingly challenging levels.

### Key Features

- **Quest System**: Progressive quest system with 4 distinct levels
- **Dynamic Combat**: Real-time combat with melee attacks and special abilities
- **Syringe Selection Mechanic**: Choose between different syringes with unique stats that affect gameplay
- **AI Enemies**: Multiple enemy types with different behaviors including:
  - Patrolling enemies with detection radius
  - Boss enemy with ranged and melee attacks
- **Dialogue System**: Interactive NPC dialogue system
- **Multiple Levels**: 
  - Hospital (Niveau1-Hopital)
  - School (Niveau2-Ecole)
  - House (Niveau3-Maison)
  - Boss Fight (Niveau4-BOSS)
- **Cinematic Intro**: Timeline-based cinematic introduction
- **Main Menu & Victory/Game Over Screens**: Complete UI flow

## 🛠️ Technical Details

### Built With

- **Engine**: Unity (Universal Render Pipeline)
- **Language**: C#
- **AI Navigation**: Unity NavMesh for enemy pathfinding
- **UI**: UI Toolkit (UIElements)
- **VFX**: Visual Effects Graph for attack effects
- **Audio**: Custom sound effects for player actions, combat, and dialogue
- **Animations**: Multiple character animations with Unity Animator

### Core Systems

#### Player System (`S_Player.cs`)
- Movement and rotation controls
- Combat system with attack cooldown
- Health management
- VFX integration for attacks

#### Quest System (`Quete.cs`)
- Persistent quest tracking across scenes
- Dynamic pharmacist positioning based on quest progress
- Syringe selection integration
- Level unlocking system

#### AI System
- **AIController**: Enemy patrol, chase, and attack behaviors with vision cone detection
- **AIBoss**: Advanced boss AI with shooting and melee attacks, distance management

#### Dialogue System (`DialogueManager.cs`)
- Queue-based dialogue display
- UI integration for character conversations
- NPC interaction triggers

#### Syringe Selection (`ChoixSeringue.cs`)
- Multiple syringe types with different stats
- UI-based selection system
- Stat application to player

## 📁 Project Structure

```
Assets/
├── Game/                           # Main game folder
│   ├── Script/                    # All game scripts
│   │   ├── Main/                  # Player controller
│   │   ├── AI/                    # Enemy AI
│   │   └── Other/                 # Utilities
│   ├── Scene/                     # Game levels
│   ├── Prefab/                    # Reusable game objects
│   └── Cinematics/                # Cutscene assets
├── Characters&Animations/          # Character models and animations
├── HUD/                           # UI elements (UXML files)
├── Sounds/                        # Audio assets
├── VFX/                           # Visual effects
├── Objects/                       # Level props and objects
├── LIGHTS/                        # Lighting setup
└── Abandoned_Asylum/              # Environment assets
```

## 🎯 Gameplay Loop

1. **Start**: Watch the cinematic intro
2. **Lobby (Hub)**: Meet the pharmacist at different locations based on quest progress
3. **Quest Reception**: Receive quest and enter the corresponding level building
4. **Level Gameplay**: Fight through enemies to complete objectives
5. **Syringe Selection**: Return to pharmacist and choose a syringe for stat upgrades
6. **Progression**: Advance to next level
7. **Final Boss**: Face the boss in the fourth level
8. **Victory/Game Over**: Reach the end screen

## 🚀 Getting Started

### Prerequisites
- Unity 2021.3 or later
- Universal Render Pipeline package

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Khrabehi/Chicoutifli.git
   ```
2. Open the project in Unity Hub
3. Open the `CinematicIntro` scene to start from the beginning or `Lobby` for quick testing
4. Press Play in the Unity Editor


## 🏆 Game Jam Achievements

Despite the 48-hour time constraint, we successfully implemented:
- ✅ Complete game loop from menu to end screens
- ✅ Multiple levels with distinct environments
- ✅ Complex AI behaviors
- ✅ Custom VFX and sound design
- ✅ Quest progression system
- ✅ Boss fight mechanics
- ✅ Cinematic intro