# ![logo](https://raw.githubusercontent.com/azerothcore/azerothcore.github.io/master/images/logo-github.png) AzerothCore
## Autofish AzerothCore Module
This module acts as a customizable, built in fishbot

### Features:

 - Auto Catching Fish
 - Auto Looting Fish
 - Auto recasting the fishing line
 - Customizable timings to account for latency
 - **(Optional)** Require players to have an item equipped and/or in bags

### Installation:

1. Clone the repository into your AzerothCore modules directory
2. Run Cmake
3. Rename or copy `mod_autofish.conf.dist` to `mod_autofish.conf`
4. Edit `mod_autofish.conf` to enable or disable features to your liking

### How to Use In-Game:

1. **Have a Fishing Pole** (example item ID `6256`) in your inventory. The module requires this item by default to activate autofishing.
   - The required item check is controlled by `AutoFish.RequiredItemId` in `mod_autofish.conf`.
   - You can also require an item to be **equipped** (rather than in bags) by setting `AutoFish.RequiredEquipId`.
   - Set either or both to `0` to disable the item requirement.
2. **Cast your fishing line** as you normally would (spell "Fishing" — ID `18248`).
3. When a fish bites and the bobber turns **READY**, the module will automatically:
   - **Reel in** the fish (click the bobber for you)
   - **Loot** the catch (if `AutoFish.ServerAutoLoot` is enabled)
   - **Recast** your fishing line (if `AutoFish.AutoRecast` is enabled)
4. Adjust `AutoFish.RecastDelayMs` and `AutoFish.AutoLootDelayMs` in the config to account for your server's latency.

> **Note:** Autofishing only works for real players. It is automatically disabled for playerbots.
