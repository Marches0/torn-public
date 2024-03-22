# Alliances
## factionAlliances.json
|Property|Type|Description|
|--|--|--|
|alliances|`AllianceMember[]`|The alliances in Torn.|

## `AllianceMember`
|Property|Type|Description|
|--|--|--|
|name|`string`|The name of this entity. For _Factions_, it is recommended to use the name returned from the Torn API rather than the one given here.|
|id|`int?`|The Faction ID of this entity in Torn. Only has a value if the entity is a _Faction_. If the entity is an _Alliance_ or _Faction Family_, it is `null`.|
|children|`AllianceMember[]`|Entities which belong to this entity.|

Entities come in three types, although the only material difference is whether they have an `id` or not.
  - _Alliances_, which consist of Faction Families and Factions. These are the highest level of the hierarchy.
  - _Faction Families_, which consist of Factions.
  - _Factions_, which map to in-game Torn Factions. These are the lowest level of the hierarchy.