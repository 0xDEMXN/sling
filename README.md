#                              Savolent#1095 code Re-write
Hey! I spent a lot of time tweaking object positions and adding additional holster locations, 
I then got the idea to link this to Ox_inventory and, well, here is the result!

An automatic holster script!

If you want to add additional weapons you just need their hash and prop ID and then add them to the config.
			allowone = Pistol
			allowtwo = Gun on Back
			allowthree = Gun on Back 2 (different rotation from back 1 since some weapons are rotated)
			allowmelee = Melee on Hip
			allowmelee2 = Melee on Hip 2 (different rotation from melee 1 since some weapons are rotated)
			allowmelee3 = Melee on Back

This script detects a weapon Equip/Unequip from ox_inventory and automatically holsters/unholsters the appropiate weapon and holster slot.
It will automatically unholster competeting slots (such as back and back2) when you try to holster something on top of it.
It will automatically unholster similiar weapons if you pull out an item that uses the same slot (such as a Pistol and a Tazer)

The /unholster command will delete all holstered weapons the player has on them.
Note: Refreshskin will drop the items to the ground, the same as any attached prop.

Original Readme Below
# Sling Script
 FiveM weapon sling script  
 Join my discord and find other cool scripts [here](https://discord.gg/U5GY4Cwepz)
 
# Description

This script allows players to sling their weapons to the back/front.

# Preview

You can see a preview of how this works [here](https://youtu.be/HwekOJofxxg)

# Features

- Allows to customize what weapons can be used (see config.lua)
- Allows to customize if a weapon can be used only in the back or if it can be used in the front too
- The command is configurable
- Keeps weapons attachaments on "unsling"
- Keeps weapons ammo on "unsling"
- Syncronized across network

# To-Do

- Adding weapons mag and attachaments to the object (currently i can't figure out a good way of doing it due to the coords)
- Adding keybinds to the script (currently clients can do it on their side using [console keybinds](https://cookbook.fivem.net/2020/01/06/using-the-new-console-key-bindings/)

# Config

The default config allows for the following weapons with all their components:
 - SMG
 - AR
 - Sniper Rifle (back only)
 - Heavy Sniper (back only)
 - Heavy Sniper Mk2 (back only)
 - Marksman rifle
 - Pump shotgun
 - Sawn-off shotgun
 - Marksman rifle MK2

You can add other weapons by finding their weapon hashes, component hashes and object names:
- [Weapon Hash](https://wiki.gtanet.work/index.php?title=Weapons_Models)
- [Component Hash](https://wiki.rage.mp/index.php?title=Weapons_Components)
- [Object list](http://gtahash.site/)

The "allowone" stands for if its allowed on the front or not. True = allowed, false = not allowed.


# Credits
This is based of [Scully's Sling Script](https://forum.cfx.re/t/standalone-law-enforcement-sling/1365649)

Indecision#7334 for helping me test and giving suggestions
