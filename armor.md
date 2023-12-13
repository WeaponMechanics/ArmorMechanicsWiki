# Armor

The following config may only be used in the `Server > plugins > ArmorMechanics > Armor.yml` file. ArmorMechanics does not allow you to use any additional files.

```yaml
ArmorTitle:
  Type: <Material>
  Name: <String>
  Lore:
    - <Line 1>
    - <etc> 
  Durability: <Integer>
  Unbreakable: <true/false>
  Custom_Model_Data: <Integer>
  Skull_Owning_Player: <String>
  Enchantments:
    - <Enchantment>-<Level>
  Attributes:
    - <Attribute>-<Amount>-<Slot>
  Leather_Color: <Color>
  Trim_Pattern: <Pattern>
  Trim_Material: <Material>
  Deny_Use_In_Crafting: <true/false>
  Recipe:
    Shape:
      - "012"
      - "345"
      - "678"
    Ingredients:
      '0': <Item>
      '1': <Item>
      'etc...': <Item>

  # The above are all from MechanicsCore/WeaponMechanics
  # The following are all from ArmorMechanics

  Bonus_Effects: <BonusEffects>
```

**`ArmorTitle`**

This is the name of your armor. It must be unique. You can get your armor using `/am get ArmorTitle` (Replace ArmorTitle) with your unique name.

**`Type`: \<String>**

This is the material of your item, e.g. `diamond_hoe`. This is not case-sensitive. **NEVER USE MAGIC NUMBERS**. This plugin does not support numerical item ids. Instead of using 294, you **must** use `golden_hoe`.

For material lists for each version, please look [here](https://github.com/WeaponMechanics/MechanicsMain/wiki/References).

**`Name`: \<String>**

This is the display name for your item, like renaming your item in an anvil. You can use [color codes](https://github.com/WeaponMechanics/MechanicsMain/wiki/General#message-color-codes).

**`Lore`: \<String List>**

This is the lore of your item. There can be as many lines as you want. You can use [color codes](https://github.com/WeaponMechanics/MechanicsMain/wiki/General#message-color-codes).

**`Durability`: \<Integer>**

How damaged your item is. Make sure you only use this with things that can be damaged (bows, tools, swords, fishing rods).

**`Unbreakable`: \<Boolean>**

Sets if your weapon is unbreakable by vanilla durability. Note that this will ignore the `Durability` option.

**`Custom_Model_Data`: \<Integer>**

Sets the [custom model data](https://www.planetminecraft.com/forums/communities/texturing/new-1-14-custom-item-models-tuto-578834/) introduced in minecraft 1.14. Minecraft does not allow 3D models to be applied to worn armor (unless you use Optifine).

**`Hide_Flags`: \<Boolean>**

Hides all item flags (Enchantments, Attributes, Unbreakable, Destroys, Placed on, Potion effects, Dye color).

**`Skull_Owning_Player`: \<String>**

Sets the skull data of the skull. Make sure to use `Type: player_head` or `Type: player_skull` with this depending on your server version. You can use Custom Skulls using the format `"UUID URL"`, check out [this video](https://www.youtube.com/watch?v=16XfZm3xqPs) for more information.

**`Enchantments`:**

Adds enchantments with given levels to the item. The format is `Enchant-Level`. For the complete list of enchantments, please look [here](https://github.com/WeaponMechanics/MechanicsMain/wiki/References#Enchantments).

Example:

```yaml
  Enchantments:
  - "sharpness 5"
  - "smite 5"
```

**`Attributes`:**

The format is `attribute value slot`. When you don't define slot, the attribute will be applied no matter which slot it is in. For armor, it is recommended that you always define the slot.

Attributes:

* `GENERIC_MOVEMENT_SPEED`
* `GENERIC_MAX_HEALTH`
* `GENERIC_ATTACK_DAMAGE`
* `GENERIC_ATTACK_SPEED`
* `GENERIC_KNOCKBACK_RESISTANCE`
* `GENERIC_ARMOR`
* `GENERIC_ARMOR_TOUGHNESS`

Slots:

* `MAIN_HAND`
* `OFF_HAND`
* `FEET`
* `LEGS`
* `CHEST`
* `HEAD`

Example:

```yaml
  Attributes:
  - GENERIC_MAX_HEALTH 5 feet               # gain 2.5 hearts
  - GENERIC_KNOCKBACK_RESISTANCE 0.25 feet  # take 25% less knockback
  - GENERIC_MOVEMENT_SPEED -0.07 feet       # go very slow
```

**`Leather_Color`: \<Color>**

See [color serializer](https://github.com/WeaponMechanics/MechanicsMain/wiki/General#Color-Serializer).

**`Trim_Pattern`: \<Pattern>**

Choose one of: `COAST`, `DUNE`, `EYE`, `HOST`, `RASIER`, `RIB`, `SENTRY`, `SHAPER`, `SILENCE`, `SNOUT`, `SPIRE`, `TIDE`, `VEX`, `WARD`, `WAYFINDER`, or `WILD`.

Check [Spigot](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/inventory/meta/trim/TrimPattern.html) for the most up-to-date list.

Check [fandom](https://minecraft.fandom.com/wiki/Smithing\_Template#Armor\_trim\_patterns) for what the patterns look like.

**`Trim_Material`: \<Material>**

Choose one of: `AMETHYST`, `COPPER`, `DIAMOND`, `EMERALD`, `GOLD`, `IRON`, `LAPIS`, `NETHERITE`, `QUARTZ`, `REDSTONE`.

Check [Spigot](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/inventory/meta/trim/TrimMaterial.html) for the most up-to-date list.

**`Deny_Use_In_Crafting`: \<Boolean>**

If `true` this item can't be used in any kind of crafting.

**`Recipe`:**

This creates a crafting recipe for your item so you can craft it in a crafting table. You can only make recipes with shapes (So you have to specify a shape, like an iron sword. You can not have a shapeless recipe, like a flint and steel).

* `Shape`:
  * This is where you define where your items go.
  * Each item gets a unique character
  * You can have 3 items each line
* `Ingredients`:
  * These are the actual items that you put in the crafting table
  * You can use simple materials or advanced
  * Instead of explaining how to use this, just look at the examples

Examples:

The following creates a recipe like an emerald sword

```yaml
  Recipe:
    Shape:
      - "e"
      - "e"
      - "s"
    Ingredients:
      'e': EMERALD
      's': STICK
```

![crafting](https://user-images.githubusercontent.com/43940682/151718278-4619f84c-072c-46dc-958d-6c11db10534c.png)

```yaml
  Recipe:
    Shape:
      - "e e"
      - " # "
      - "e e"
    Ingredients:
      'e':
        Type: "diamond"
        Name: "&eTest"
        Lore:
          - "&7Testing testing 123"
      '#': STICK
```

**`Bonus_Effects`**

The Bonus Effects are applied to players when they wear the armor.
