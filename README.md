# 🏆 SQKOTH — The Ultimate King of the Hill Mini-Engine

An ultra-optimized, modular, and performance-centric **King of the Hill (KOTH)** event management engine designed for modern Minecraft servers. Built on a zero-addon architecture, it ensures maximum stability, flawless performance, and high-end graphical outputs without straining cloud hosting footprints.

---

## 🎯 Project Overview & Objective

The primary objective of **SQKOTH** is to provide server administrators with an independent, lightweight, and fully automated PvP event solution. It bridges the gap between complex Java plugins and heavy scripting by utilizing standard Minecraft command structures combined with native performance filtering. 

### Core Pillars:
* **Zero-Addon Footprint:** Requires absolutely no external Skript addons (such as SkBee or SkQuery), neutralizing version incompatibility issues.
* **Performance-First Logic:** Replaces resource-heavy multi-world baseline looping with centralized structural proximity coordinate math, eradicating Server Tick (TPS) drops.
* **Flawless Visual Integration:** Dynamically communicates with specialized holographic displaying platforms using strict syntax rendering pipelines.

---

## 💻 Administrative Commands & Configurations

### 📄 Comprehensive Command Hierarchy
All administrative tools utilize modern command arguments with built-in memory safety gates:


| Command | Permission | Description |
| :--- | :--- | :--- |
| `/sqkoth` | `sqkoth.admin` | Accesses the graphical administrative control menu frame. |
| `/sqkoth set` | `sqkoth.admin` | Binds the central zone location coordinates and teleports the registry hologram. |
| `/sqkoth remove` | `sqkoth.admin` | Flushes region coordinates from database and broadcasts safe error modes. |
| `/sqkoth start` | `sqkoth.admin` | Forces the immediate execution of a match session bypassing countdowns. |
| `/sqkoth stop` | `sqkoth.admin` | Terminates the active capturing cycle and resets the state machines. |
| `/sqkoth reload` | `sqkoth.admin` | Hot-reloads configuration file modules and cleans runtime variables. |

### ⚙️ Quick Settings Options (`options:`)
Modify these variables at the very top of the provided script file (`sqkoth.sk`) to customize the environment:

* `prefix`: Define the localized chat prefix.
* `hologram`: Set the exact registered identifier name matching your holographic system layout.
* `hill_radius`: Horizontal boundary radius check ($X$ and $Z$ axis distance around the center block).
* `hill_height`: Vertical ceiling boundary detection check ($Y$ axis distance limit above/below center).
* `reward_money`: Set the custom Vault cash distribution value given to winners.
* `crate_command`: Modify the automated crate key rewarding command string to fit your network ecosystem.
* `start_interval_saved`: Automated cycle cooldown timer until the next game triggers automatically (in seconds).
* `koth_time_saved`: Capture holding duration threshold required to secure a victory (in seconds).
* `no_player_timeout`: Anti-stalemate duration gate that closes inactive matches if zero capture interaction happens (in seconds).

---

## 🛠️ Step-by-Step Production Deployment Guide

Deploying SQKOTH requires strict alignment with production protocols to ensure the data structures initialize correctly inside the Minecraft runtime engine. Follow these exact steps:

### Phase 1: Dependency Verification & Network Setup
1. Ensure your server environment is running a compatible software branch (**Paper**, **Purpur**, or **Spigot**) on version **1.21.1**.
2. Install the mandatory foundation plugins into your `/plugins/` folder: **Skript**, **FancyHolograms**, **Vault**, and an economy provider (e.g., **EssentialsX**).
3. Restart the server node to fully mount the configuration systems and operational pipelines.

### Phase 2: Core Script Installation (Ready-Made File)
1. Download the complete ready-made **`sqkoth.sk`** script file directly from this GitHub repository.
2. Drop the downloaded **`sqkoth.sk`** file straight into your server file registry path: `/plugins/Skript/scripts/`.
3. Open the file to tweak the `options:` configurations (rewards, commands, times) to match your setup, and save it.
4. Execute the runtime compilation command inside your terminal or in-game chat to mount the engine:  
   ```bash
   /sk reload sqkoth
   ```
5. Confirm that the terminal outputs a `Green Log` indicating successful structural compilation with zero syntax restrictions.

### Phase 3: Holographic Platform Configuration
1. Travel to your designated PvP arena map environment.
2. Stand exactly on the desired center point block and initialize the database anchor inside your hologram plugin by creating a text element carrying your identifier tag using the exact syntax below:
   ```bash
   /holo create text koth_hologram
   ```
3. Expand the layout array to hold exactly **4 operational stacked lines** by adding padding blocks to avoid Java array overflow errors during real-time data streaming:
   ```bash
   /holo edit koth_hologram addline .
   ```
   *(Repeat this action until your hologram structure registers a total height size of 4 distinct rendering lines).*

### Phase 4: Final Database Anchoring & Live Testing
1. Stand right back on the center capturing block platform.
2. Execute the sovereign initialization bridge:
   ```bash
   /sqkoth set
   ```
   *This command instantly locks the core coordinates inside the script's global registry and seamlessly binds the FancyHolograms entity location directly to your stance.*
3. Test your system layout resilience by running:
   ```bash
   /sqkoth remove
   ```
   The engine should instantly flush the position maps and fire the native safety system, changing the holographic presentation to clean text stating: `Please define the area or put me back in it`.
4. Re-run `/sqkoth set` to anchor it permanently. The deployment is complete! Your engine is ready for production.

---

## 🤝 Community & Support

If you need any help setting up the script, run into any issues, or just want to report a problem, you are more than welcome to join our community! It's not strictly for developers—anyone is welcome to get support or ask questions.

* **💬 Join our Discord Server:** [https://discord.gg/DYkUr5mK3n]

---
*Developed with care, performance optimization, and easy configuration for everyone.*
