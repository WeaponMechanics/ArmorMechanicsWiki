# Bonus Effects

```yaml
  Bonus_Effects:
    Potion_Effects:
      - <PotionMechanic>
    Immune_Potion:
      - <PotionEffectType>
    Bullet_Resistance:
      Base: <Percentage>
      Per_Weapon:
        - <WeaponTitle> <Percentage>
    Equip_Mechanics: <Mechanics>
    Dequip_Mechanics: <Mechanics>
    Damage_Mechanics: <Mechanics>
```

**`Potion_Effects`**

See the [PotionMechanic](https://github.com/WeaponMechanics/MechanicsMain/wiki/PotionMechanic) for more information.

```yaml
    Potion_Effects:
      - "Potion{potion=WATER_BREATHING}"
```

**`Immune_Potion`**

Potion effects of any level on this list cannot affect the player. Here is a [list of potion effects for your version](https://github.com/WeaponMechanics/MechanicsMain/wiki/References#Potion-Effects).

**`Bullet_Resistance`**

Defines a percentage of damage reduction. For example `Base: 0.01` is 1% damage reduction to all WeaponMechanics damage. Negative values will INCREASE the amount of damage dealt by a gun. If you want specific weapons to have more/less resistance, you can add them to the `Per_Weapon` list. Here is a simple example:

```yaml
    Bullet_Resistance:
      Base: 0.05 # 5% resistance
      Per_Weapon:
        - ArmorPiercingGun 0.0 # No resistance since this gun pierces armor
```

**`Mechanics`**

If you are unfamiliar with Mechanics, it is a complex system designed for WeaponMechanics that allows you to send messages/titles/sounds/potion effects/fireworks/etc. You can use Mechanics to tell the player that they equipped armor, or play a sound. Maybe you want to set off a firework.

`Equip_Mechanics` are played when the bonus effect is applied to the player.\
`Dequip_Mechanics` are played when the bonus effect is removed from the player.\
`Damage_Mechanics` are played when the player is damaged.

See the wiki for [Mechanics](https://github.com/WeaponMechanics/MechanicsMain/wiki/Mechanics) for more instructions on how to configure them.
