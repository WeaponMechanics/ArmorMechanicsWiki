# Armor Sets

The following config may only be used in the `Server > plugins > ArmorMechanics > Set.yml` file. ArmorMechanics does not allow you to use any additional files.

Usually you want to your sets to have all 4 pieces of armor, but this is not specifically required. Check out the `Scuba_Set` as an example. In it's config, I commented out `#Boots: "Scuba_Boots"`. This allows player to get the benefits of the `Scuba_Set` without wearing any boots, or by wearing boots of their choice. You can also use this to "mix and match" sets. For example, give a set bonus to a Helmet and Chestplate, and a different set bonus to leggings and boots. Your players may have a hard time understanding this, so be careful.

```yaml
<SetName>:
  Helmet: <String>
  Chestplate: <String>
  Leggings: <String>
  Boots: <String>
  Bonus_Effects: <BonusEffects>
```

**SetName**

This is the name of your set. You can get the set in game using `/am giveset @p <Set-Name>`. This name cannot be the same as any other set or armor, so I recommend adding `Set` to the end of your name. For example `Scuba` becomes `ScubaSet`. This will help you avoid issues in the future.

**Helmet: \<String>**

The armor title of the helmet for this set. If you don't include this line, players will be able to wear any helmet along with this set.

**Chestplate: \<String>**

The armor title of the chestplate for this set. If you don't include this line, players will be able to wear any chestplate along with this set.

**Leggings: \<String>**

The armor title of the leggings for this set. If you don't include this line, players will be able to wear any leggings along with this set.

**Boots: \<Boots>**

The armor title of the boots for this set. If you don't include this line, players will be able to wear any boots along with this set.

**Bonus\_Effects: \<BonusEffects>**

The bonus effects that are applied to the player while they wear this set. I like to send the players a message that they have equipped a set. You can add fireworks, potion effects, etc. Note that this field is REQUIRED for a set, as after all, why have a set without bonus effects?
