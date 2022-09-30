---
layout: post
title: "Administrator Commands Guide"
author: "Scout"
---
## Disable Friendly Fire, Artillery, Nuclear
This should be ran when the game first starts. Omit lines regarding Artillery depending on the polls.
```lua
/c
game.player.force.friendly_fire = false
game.player.force.technologies["atomic-bomb"].enabled=false
game.player.force.technologies["atomic-bomb"].visible_when_disabled=true
game.player.force.technologies["artillery"].visible_when_disabled=true
game.player.force.technologies["artillery"].enabled=false
game.player.force.recipes["artillery-targeting-remote"].enabled=false
```

## Inventory Gift
```lua
/c game.player.force.character_inventory_slots_bonus = 30
```

### Revert
```lua
/c game.player.force.character_inventory_slots_bonus = 0
```

## High-Artillery Map
```lua
/c
game.player.force.friendly_fire = false
game.player.force.artillery_range_modifier = 2
game.player.force.technologies["atomic-bomb"].enabled=false
game.player.force.technologies["atomic-bomb"].visible_when_disabled=true
```

## Revert All
```lua
/c game.player.force.reset()
```

## Promote to Veteran from Console
Does not require a relog.
```lua
/sc
local Roles = require 'expcore.roles'
local player = 'Warforged_Raven'
Roles.assign_player(player, {'Regular','Veteran'})
Roles.override_player_roles(player, {'Regular','Veteran'})
```

## Force Automatic-Mode Trains
Used to counter mass-base deconstruction
```lua
/c
for _, v in pairs(game.player.force.get_trains()) do
    v.manual_mode = false
end
```

## Remove Ghost Spam
This will remove **all** ghosts placed by a specific user. Useful for cleaning up griefing.
```lua
/c
for _, v in pairs(game.player.surface.find_entities_filtered{force=game.player.force}) do
    if v.type == "entity-ghost" and v.last_user.name == "MAFANYA" then
      v.destroy()
    end
end
```

## Force-Build Ghosts
This will build **all** ghosts placed by a specific user. Useful for cleaning up griefing.
```lua
/c
for _, v in pairs(game.player.surface.find_entities_filtered{force=game.player.force}) do
    if v.type == "entity-ghost" and v.last_user.name == "Spzi" then
      v.revive()
    end
end
```

## Remove Deconstruction-Queued Entities
This will remove **all** entities queued for deconstruction, no matter if they are in a botnet or not.
```lua
/c for _, entity in pairs(game.player.surface.find_entities_filtered{to_be_deconstructed=true}) do
    entity.destroy()
end
```

## Remove Pollution
This will wipe the map of pollution and disable future pollution generation.
```lua
/c for _, surface in pairs(game.surfaces) do
  surface.clear_pollution()
end
game.map_settings.pollution.enabled = false
```

## Remove Landfill without /editor
This will kill your character if not in `/spectate`. Use with caution.
```lua
/c
local tiles = game.player.surface.find_tiles_filtered{position=game.player.position,radius=5,name="landfill"}
local replace = {}
for i, tile in pairs(tiles) do
    replace[i] = {position=tile.position, name="water"}
end
game.player.surface.set_tiles(replace)
```

## Force-Changing a Tag
I am unsure if this replaces the tag in persistent storage or not.
```lua
/sc game.players["zampaman"].tag = "- Tag Goes Here"
```

## Veterans Jail
This will allow veterans to jail others.
```lua
/c
local Roles = require 'expcore.roles'
Roles.get_role_from_any("Veteran").allowed_actions["command/jail"] = true
Roles.get_role_from_any("Veteran").allowed_actions["command/unjail"] = true
```
Undo:
```lua
/c
local Roles = require 'expcore.roles'
Roles.get_role_from_any("Veteran").allowed_actions["command/jail"] = false
Roles.get_role_from_any("Veteran").allowed_actions["command/unjail"] = false
```

## View Statistics
The first number is maps played, and the second is playTime - AfkTime, in hours. Note that this only applies for tracked data (ie. from when we started using the database)
```lua
/sc
local PlayerData = require 'expcore.player_data'
local Statistics = PlayerData.Statistics
local stats = Statistics:get("i_cant_think_of_a_username", {})
local playTime, afkTime, mapCount = stats.Playtime or 0, stats.AfkTime or 0, stats.MapsPlayed or 0
game.player.print(mapCount)
game.player.print((playTime - afkTime) / 60)
```
### Amended 2022/08/12 by Scout
