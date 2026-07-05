<!-- 1) BANNER -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:7C5CFF,100:B69CFF&height=170&section=header&text=unity-zombie-shooter&fontColor=ffffff&fontSize=44&desc=3D%20zombie%20wave-shooter%20built%20in%20Unity&descAlignY=62&descSize=16&animation=fadeIn" width="100%"/>
</p>

<!-- 2) TYPING SVG -->
<p align="center">
  <a href="https://github.com/dyntr">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=18&pause=1000&color=7C5CFF&center=true&vCenter=true&width=680&lines=FPS+movement%2C+raycast+shooting+%26+NavMesh+AI;Clear+the+zombies+to+unlock+the+next+level" alt="typing"/>
  </a>
</p>

<!-- 3) BADGES -->
<p align="center">
  <img src="https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white"/>
  <img src="https://img.shields.io/badge/Unity_2022.3_LTS-000000?style=flat-square&logo=unity&logoColor=white"/>
  <img src="https://img.shields.io/badge/NavMesh_AI-000000?style=flat-square"/>
  <img src="https://img.shields.io/badge/TextMeshPro-000000?style=flat-square"/>
  <img src="https://img.shields.io/badge/status-school%20project-6e7681?style=flat-square"/>
</p>

## Overview

A first-person 3D zombie shooter built in Unity as a school project: a main menu, two playable levels, and a game-over screen, with NavMesh-driven enemy AI and wave-based level progression.

## ✦ Features

- **First-person controller** — `Rigidbody`-based WASD movement with jump (`Movement.cs`), and mouse-look with pitch clamped to ±90° so the camera can't flip (`PlayerLook.cs`).
- **Raycast shooting** — `Gun.cs` fires a ray from the camera through the mouse position on left-click, then spawns a physical bullet prefab (`Bullet.cs`) aimed at the hit point, which applies damage on trigger collision and destroys itself on impact.
- **NavMesh enemy AI** — zombies path to the player every frame via `NavMeshAgent.SetDestination` (`EnemyAI.cs` / `EnemyWalk.cs`), dealing contact damage through `ZombieAttack.cs` and freezing/deactivating on death.
- **Health system** — both player (`PlayerHealth.cs`) and enemies (`Health.cs`) track HP with a UI `Slider`; the player's death loads the `GameOver` scene, an enemy's death notifies the wave counter.
- **Wave counter** (`ZombieCounter.cs`, singleton) tracks zombies remaining out of the total for the level and automatically loads the next level once the wave is cleared.
- **Randomized spawning** — `EnemySpawner.cs` instantiates enemies at a random spawn point on a fixed timer (`InvokeRepeating`).
- **Main menu** (`MainMenu.cs`) with Start / back-to-menu / quit, unlocking the cursor for menu navigation and locking it back for gameplay.
- **4 scenes**: `MENU` → `Level1` → `Level2` → `GameOver`.

## 🛠 Built with

C#, Unity 2022.3 LTS, Unity NavMesh AI (`NavMeshAgent`), TextMeshPro (UI), plus third-party Asset Store packs for the skybox and character/environment models.

## 📦 Getting started

Open the project folder in Unity Hub with Unity **2022.3.x**, open the `MENU` scene under `Assets/Scenes/`, and press Play. WASD to move, mouse to look, left-click to shoot.

## 🎓 What I learned

Core FPS mechanics from scratch — mouse-look with clamped rotation, camera-based raycasting, physics-driven projectiles — Unity's NavMesh pathfinding for enemy AI, the singleton pattern for state that needs to survive across a single play session (the zombie counter), and structuring a multi-scene game flow (menu → levels → game over).

## 🚀 Status

Built during studies at SPŠE Ječná — a school project / prototype, not a polished shipped game. Uses Unity Asset Store packs for art (skybox, character models) rather than original assets.

<!-- FOOTER -->
---
<p align="center">
  <sub>Part of <a href="https://github.com/dyntr">Patrick Dyntr's</a> portfolio · Built by <a href="https://github.com/dyntr">@dyntr</a></sub>
</p>
