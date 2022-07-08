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
Note this will be visible to everyone.
```lua
/c game.player.force.chart_all()
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

## Peaceful
This will enable peaceful mode. Newly spawned biters will not attack unless provoked.
```lua
/c game.player.surface.peaceful_mode = true
```


##### Amended 2022/07/08
