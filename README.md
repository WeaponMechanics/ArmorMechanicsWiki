# Home

### Modules

* Armor
* Armor Sets
* Bonus Effects

### Information

ArmorMechanics is an addon for [WeaponMechanics](https://www.spigotmc.org/resources/.99913/) which adds sets of armor with special bonus effects. Key features include:

* Potion Effects on armor
* Bullet resistances from guns
* Immunity from certain potion effects
* Special effects when equipping/dequipping/damaging armor
* Set bonuses when wearing a full set of armor

### Getting Started

To install the plugin

1. Download the latest [WeaponMechanics](https://www.spigotmc.org/resources/weaponmechanics-1-9-4-1-19.99913/) version
2. Download the latest ArmorMechanics version
3. Add the 3 jar files (`MechanicsCore`, `WeaponMechanics`, and `ArmorMechanics`) to the `YourServer > plugins` folder.
4. Start your server.

ArmorMechanics will generate a new folder at `YourServer > plugins > ArmorMechanics`. In there, you will be able to add/change configurations.

### Frequently Asked Questions

> **There is an error in the console when the plugin starts!**

First, make sure _BOTH_ `WeaponMechanics` and `MechanicsCore` are installed and running on your server. If they are red in `/plugins`, you can ask for help [here](https://discord.gg/ERVgpfg).

If there is an error in your config, chances are, ArmorMechanics is trying to tell you which mistake you made. Look in console for lines starting with `[Server thread/ERROR]: [ArmorMechanics]`, as these will give you more information about what went wrong.

Sometimes, an error can also be a YAML formatting issue. Make sure to use notepad++ to edit `.yml` files! Common issues:

* Using tabs instead of spaces (notepad++ fixes this for you)
* Correct indentation for each line
* "All strings are surrounded by quotes".
  * This is especially important when using color codes.
* Incorrect spelling. Double check your spelling using the wiki.

If you are unsure if your YAML file is correctly formatted, try using a [YAML Validator](https://jsonformatter.org/yaml-validator).

Now that you have tried EVERYTHING possible, you should [get in contact with us](https://discord.gg/ERVgpfg) so we can help fix your issue.

> **Can you add more sets of armor?**

No, but **you** can! If you use this wiki, you can create your own sets of armor that are specialized for your server. Besides, your own custom armor is far more cool.

> **I think I found a bug, where can I report it?**

Please make all of your bug reports on our [github](https://github.com/WeaponMechanics/ArmorMechanics/issues/new/choose). You may also use that link to make feature requests, and report performance issues.
