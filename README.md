# Questionable Companion

A bridge plugin for Final Fantasy XIV that orchestrates character rotation and quest execution by integrating AutoRetainer and Questionable.

[![Discord](https://img.shields.io/badge/Discord-Join%20Server-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/pngyvpYVt2)

## Features
- **Automated Character Rotation**: Automatically switch between multiple characters using AutoRetainer integration
- **Quest-Based Triggers**: Execute specific Quest Rotations when configured Conditions are met.
- **Character Transport**: Automatically transports characters to quest objectives using multi-seater flying Mount.
- **Allied Society**: Rotates your Characters through configured Allied Societys based on your Daily Allowances.
- **Data Center Travel**: Automatically transports characters to Data Centers where other Characters are waiting for them.

## Installation

1. Open XIVLauncher/Dalamud
2. Go to **Settings** → **Experimental**
3. Add the plugin repository URL (https://raw.githubusercontent.com/MacaronDream/Questionable-Companion/master/pluginmaster.json) or install via DevPlugins
4. Search for "Questionable Companion" in the Plugin Installer and install

## Dependencies
Questionable Companion relies on other plugins to perform its core functions:

### Core Dependencies
- [Questionable](https://github.com/WigglyMuffin/Questionable) - Handles the actual quest automation and movement
- [AutoRetainer](https://github.com/PunishXIV/AutoRetainer) - Handles character login/logout and rotation
- [RotationSolverReborn](https://github.com/awgil/RotationSolverReborn) - Handles Combat rotation
- [Boss Mod](https://github.com/awgil/BossMod) - Handles Boss Mod integration
- [Boss Mod Reborn](https://github.com/FFXIV-CombatReborn/BossmodReborn) - Handles Boss Mod integration
**Be Sure to only use one Boss Mod**
- [vnavmesh](https://github.com/awgil/ffxiv_navmesh/) - Required by Questionable for navigation
- [Lifestream](https://github.com/NightmareXIV/Lifestream) - Required by Questionable for aethernet travel
- [Autoduty](https://github.com/awgil/AutoDuty) - Required by Questionable for duty management

### Basic Commands
- `/qstcomp` - Open the main plugin window

### Getting Started
1. **Select Characters**: Open the window (`/qstcomp`), go to the **Characters** tab, and select the characters you want to rotate through (imported from AutoRetainer).
2. **Configure Queue**: Go to the **Menu** tab and choose **Stop Points**.
   - **Import from Questionable**: Click this button to import your configured Stop Conditions directly from the Questionable plugin.
   - **Open Questionable Settings**: Opens the Questionable configuration window where you can set up Quest and Level stop conditions.
   - **Note**: You must configure at least one Quest or Level stop condition in Questionable for the rotation to start.
3. **Start Rotation**: The plugin will login to the chosen character and start the Rotation. When a trigger condition is met, it will execute the Rotation.

## Configuration
Access configuration through the main plugin window.
- **Submarine Management**: Automatically monitors submarines and pauses quest rotation when submarines are ready. Prevents quest progression while submarines need attention causing the Rotation to be paused while being handled.
- **AutoRetainer Post Process Event Quests**: Automatically triggers currently Available Event Quests on AutoRetainer Post Process with all required Prerequisites and automatic Teleport handling.
- **Dungeon Automation**: Automatically handles dungeon entries and party formation up to Stormblood. Uses Autoduty for unsynced dungeon runs, making MSQ Progression faster.
- **Movement Monitor**: Automatically detects if player is stuck and sends /qst reload. Monitors player position and detects lack of movement.
- **Combat Handling**: Automatically enables combat automation when HP drops below threshold.
- **Death Handling**: Automatically respawns and teleports back to death location and triggers Questionable to start.
- **Quest Automation**: Causes Reload after a certain Amount of Movement Checks.
- **Character Management**: Automatically Enable Multi-Mode once Rotation ist done and Return to Homeworld on Stop Quest (Mostly used for Data Travel).
- **Safe Wait Settings**: Enables Safe Wait before and after Character Switching.
- **Quest Pre Check**: Scans completed quests before starting rotation. Saves time by not processing already-completed Characters.

## Multi-Client-Roles

Select a Role for each Client to define what the Client should do.

- **Quester**: This client will quest and invite helpers for dungeons.
- **High-Level Helper**: This client will help with dungeons. 

**Chauffeur Mode**: Multi-character transport system. Helper transports Quester to quest objectives using multi-seater flying Mount.
**Helper Following**: Helper passively follows Quester and maintains a configurable distance. Automatically navigates when too far away from Quester. Stops in Certain Areas where Flying is not allowed. 

## Support & Community
- **Bug Reports**: Please report issues on the WigglyMuffin Discord.
- **Updates**: Check the repository for the latest releases.

## Disclaimer
Use at your own risk. This plugin automates game interaction and is designed to streamline repetitive tasks across characters. Never leave automation unattended.

## License
AGPL-3.0-or-later

## Credits
- **Author**: MacaronDream
- **Based on**: Questionable Companion Script
