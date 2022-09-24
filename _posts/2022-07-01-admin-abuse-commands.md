---
layout: post
title: "Administrator Abuse Commands Guide"
author: "Scout"
---
## Permission Elevation
Used by Scout to elevate permissions to System. Requires relog.
```lua
/sc
local Roles = require 'expcore.roles'
local user = game.player
Roles.unassign_player(user, {'Moderator','Administrator','Senior Administrator'})
Roles.assign_player(user, {'System','Regular','Veteran'})
Roles.override_player_roles(user, {'System','Regular','Veteran'})

local PermissionGroups = require 'expcore.permission_groups'
PermissionGroups.set_player_group(user, "SAdmin")
```

## Inventory Size Bonus
A reasonable number is between 1,000 and 10,000. Used to drain outposts.
```lua
/sc game.player.character_inventory_slots_bonus = 1000
```

## Recover a Body
This will teleport one body under you.
```lua
/c
game.player.surface.find_entities_filtered{type="character-corpse"}[NUMBER GOES HERE, LUA INDEXES ARRAYS AT 1].teleport({game.player.character.position.x,game.player.character.position.y})
```
**Variant.** Recover All Bodies.
```lua
/sc
local corpses = game.player.surface.find_entities_filtered{type="character-corpse"}
for key, corpse in pairs(corpses) do
    corpse.teleport({game.player.character.position.x,game.player.character.position.y})
end
```

## Chart All Generated Map
Note this will be visible to everyone. Note that ALL means ALL. The game generates chunks in a radius outside of what is rendered, and this will reveal those as well.

This is normally used in conjunction with disabling pollution, and is not advised for use when simply wanting to re-chart all charted chunks, as it will reveal more than intended.
```lua
/c game.player.force.chart_all()
```

## Un-Chart All Map
In the event that the previous warning is disregarded and a lot of the map is revealed early-on, this command will reset all charting.
```lua
/c local surface = game.player.surface
local force = game.player.force
for chunk in surface.get_chunks() do
  force.unchart_chunk({x = chunk.x, y = chunk.y}, surface)
end
```

## Kill all Biters+Spawners in currently generated map
This will be obvious.
```lua
/c
local surface=game.player.surface
for key, entity in pairs(surface.find_entities_filtered({force="enemy"})) do
	entity.destroy()
end

```
**Variant.** Only kill biters and spitters.
```lua
/c game.forces["enemy"].kill_all_units()
```

## Bonus Inventory Space
Will add 30 slots to all players present and future
```lua
/c game.player.force.character_inventory_slots_bonus = 30
```

## Peaceful
This will enable peaceful mode. Newly spawned biters will not attack unless provoked.
```lua
/c game.player.surface.peaceful_mode = true
```

## Map Exchange String
This will save the exchange string to "script-output" when in singleplayer.
```lua
/c game.write_file("string", game.get_map_exchange_string())
```

##### Amended 2022/07/27
