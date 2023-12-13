# Mythic Mobs

[MythicMobs](https://www.spigotmc.org/resources/5702/) is a plugin that allows you to create custom creatures with abilities. We support the [latest Mythic Mobs v5](https://mythiccraft.io/index.php?pages/official-mythicmobs-download/) plugin. You don't need to be using the premium version nor the dev builds, the free version works. ArmorMechanics gives you the ability to add your custom armor to MythicMobs.

### `armorMechanicsArmor` ([Item](https://git.mythiccraft.io/mythiccraft/MythicMobs/-/wikis/Mobs/Equipment))

| Attribute  | Alias | Description                                         | Default         |
| ---------- | ----- | --------------------------------------------------- | --------------- |
| armorTitle | armor | The armor-title (from config) of the armor to equip | None (Required) |

### Example

This mob is a drowned with a full set of Scuba armor equipped.

```yaml
Scuba_Zombie:
  Type: drowned
  Health: 32
  Damage: 2
  Faction: undead
  Options:
    PreventRandomEquipment: true
    PreventSunburn: true
  Equipment:
  - armorMechanicsArmor{armor=Scuba_Helmet} HEAD
  - armorMechanicsArmor{armor=Scuba_Chestplate} CHEST
  - armorMechanicsArmor{armor=Scuba_Leggings} LEGS
  - armorMechanicsArmor{armor=Scuba_Boots} FEET
```
