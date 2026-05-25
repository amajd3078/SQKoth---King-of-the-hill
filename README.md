# SQKoth - King of the hill — Official Stable Release v1.0.0

An advanced, highly-optimized, and completely autonomous **King of the Hill (KOTH)** event system engineered entirely in pure Skript. Designed specifically for high-performance PvP server environments and fully compatible with low-spec hardware hosts like Aternos without causing any ticks drop or background memory leaks.

---

## 💎 Key Features

* **Zero Addon Dependencies:** Runs 100% on standard Vanilla Skript (2.6+). No extra plugins or heavy addons required.
* **Absolute Math Calibration Engine:** Automatically sorts maximum and minimum coordinates in the background. Setup your arena vectors in any direction without breaking the zone bounding box!
* **Contested & Anti-Cheat Logic:** Accurately detects when multiple players push the hill. Freezes the countdown instantly if more than one user enters the region.
* **ExcellentCrates & Vault Hooked:** Distributes physical item keys and automated virtual cash currency balance directly to the victor upon successful hold completion.
* **Fancy Hologram Integration:** Dynamically updates your active server hologram (`koth_hologram`) frame-by-frame with clean waiting cycles and active player tracking metrics.

---

## ⚙️ Core Configuration (Options Panel)

You can easily modify rewards, interval cooldown counters, and hold timers at the very top of the script file inside the configuration zone:

```skript
options:
    prefix: &6&lS&e&lQ&b&lKOTH &8»&f
    hologram: koth_hologram 
    
    # Reward Settings
    reward_money: 5000            # Total cash distributed to the winner
    crate_name: common            # ExcellentCrates ID for keys distribution
    key_amount: 1                 # Amount of keys dropped into the winner's inventory
    
    # Cycle Timers Configuration
    setnext_interval: 3600        # Background interval delay between auto-events (In seconds)
    settime_capture: 10 seconds   # Uninterrupted hold timer required to secure the hill victory
    auto_close_empty: 15 minutes  # Match shutdown buffer if the arena stays totally empty
```

---

## 📖 Deep System Manual & Operation Flow

### ⏳ 1. The Waiting Phase (Idle Countdown Loop)
Once the server boots or reloads, the script initializes into the **Waiting Phase**. The automated internal looping scheduler begins counting down toward the next match deployment sequence. Every single second, the system pushes a silent data refresh directly to your hologram entity showing:
* **`SQKOTH EVENT`**
* **`Next Event In: MMm SSs`** (Live remaining countdown)
* **`Get Ready for Battle!`**

### ⚔️ 2. The Active Phase (Live Arena Calculations)
When the countdown hits zero (or an administrator triggers the event manually via commands), the match switches to the **Active Phase**:
1. **Global Broadcast:** A clean, slash-free server announcement alerts all online players that the hill is open for capture, printing rewards details.
2. **Hologram Shifting:** The hologram metrics immediately recalibrate to show live arena tracking arrays:
   * **`Status: CAPTURING / CONTESTED / WAITING`**
   * **`Time: [Remaining Seconds]s`**
   * **`Capper: [Player Name]`**
3. **Region Evaluation Engine:** The script actively runs spatial boundary looping scripts every 1 second:
   * **Single Player Present:** Shuts down idle loops, flashes `CAPTURING`, and counts down from `10s` smoothly.
   * **Multiple Players Present:** Drops anchor, flips status to `CONTESTED`, and freezes the timer. The ticker will not budge until competitors eliminate each other.
   * **Empty Zone Event:** Refreshes status to `WAITING` and hard-resets the countdown variable back to its initial state to completely prevent cheap exploit wins.

### 🎉 3. The Victory Phase (Rewards & Clean-up Initialization)
If a dominant combatant successfully holds the secure line for a full, uninterrupted capture cycle:
* The live state turns off and the idle background scheduling cycle turns back on.
* Firework rockets are automatically summoned straight onto the victor's current coordinates alongside a universal sound prompt.
* Vault processes inject the hardcoded currency prize, and console layers dispatch physical keys straight into the player's slots using native **ExcellentCrates** scripts.

---

## 🛠️ In-Game Admin Commands Array

Ensure you possess the administrative permission node **`sqkoth.admin`** before trying to map coordinate data vectors or forcing manual loop states:

* **`/sqkoth set1`** — Calibrates the first boundary vector block at your precise location. (Stand on the lower-left edge block).
* **`/sqkoth set2`** — Calibrates the second boundary vector block at your precise location. (Stand on the upper-right edge block).
* **`/sqkoth start`** — Forces an active phase immediately, overrides timer loops, and spawns the capture engine matrix.
* **`/sqkoth stop`** — Forcefully terminates any active matching state, wipes capture trackers, and returns the world to idle wait states.
* **`/sqkoth status`** — Pulls live data streams from the caching core to inspect current phase values, positions state variables, and interval thresholds.
* **`/sqkoth reload`** — Safely flushes memory blocks, unloads dead caching threads, and parses script updates from your core file directory.

you can join my discord server if you want [: **`https://discord.gg/28pTmAYCwH`**
