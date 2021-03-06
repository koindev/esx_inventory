# esx_inventory | Only works with this [es_extended](https://github.com/0rangeFox/es_extended)

### I will accept PR or do bug fixes, if you found one, [just report it on section "issues"](https://github.com/0rangeFox/es_extended/issues). You can [join on my support discord](https://discord.gg/5vrjddj) to get help.

# Description
Adds the following features

- Inventory Hud with Slots
[![Image from Gyazo](https://i.gyazo.com/08082a66b8da85aee146d1ed64f36fb4.png)](https://gyazo.com/08082a66b8da85aee146d1ed64f36fb4)
[![Image from Gyazo](https://i.gyazo.com/e00dd9c44cac5fd5b20ef59f0647ffc8.jpg)](https://gyazo.com/e00dd9c44cac5fd5b20ef59f0647ffc8)
- Drops with HUD
[![Image from Gyazo](https://i.gyazo.com/51b7d1f95254bdc9acf2b77d1683ef19.png)](https://gyazo.com/51b7d1f95254bdc9acf2b77d1683ef19)
[![Image from Gyazo](https://i.gyazo.com/76abd2c0f5e65daa5e6504507e25a90e.jpg)](https://gyazo.com/76abd2c0f5e65daa5e6504507e25a90e)
- Pay with HUD
- Give with HUD
- Hot keys 1 - 5
- Shops with HUD
[![Image from Gyazo](https://i.gyazo.com/9dbd4621c463b2e71c7e9e4edeec7057.jpg)](https://gyazo.com/9dbd4621c463b2e71c7e9e4edeec7057)
- Trunks with HUD
[![Image from Gyazo](https://i.gyazo.com/6cf05119320210ae1df929f0803515bc.jpg)](https://gyazo.com/6cf05119320210ae1df929f0803515bc)
- Glovebox with HUD
[![Image from Gyazo](https://i.gyazo.com/2ed7a9365c5f8ec52be3ed3a16abb493.jpg)](https://gyazo.com/2ed7a9365c5f8ec52be3ed3a16abb493)
- Weapons as Items
[![Image from Gyazo](https://i.gyazo.com/94fb987ed7e683a56188ce96b5b643b3.jpg)](https://gyazo.com/94fb987ed7e683a56188ce96b5b643b3)

# Explanation

## Weapons as Items
Weapons are read from the `items` table with the prefix `WEAPON_`. Add all usable weapons into the `items` table with their limit.
Ammo for each weapon is stored in `ammos` table however I do not support addition of ammo yet.

## Hotbar Keys
The weapon wheel is disabled for the use of hot keys. Weapons being used as items is needed in this case

# Installation
[Download `disc-base`](https://github.com/DiscworldZA/gta-resources/tree/master/disc-base)

Add the disc-base and esx_inventory to resource folder `[esx]/[inventory]`

Execute SQL : `esx_inventory.sql`

Add the following lines to your config:
```
start disc-base
start esx_inventory
```

# Editing CSS
The source CSS is written in SASS, which is a superset of the CSS3 syntax. Compiling this will require some form of a SASS compiler to compile it into valid vanilla CSS that a browser (or in this case, NUI/CEF) can understand and parse. Can easily get a Visual Studio Code extension to achieve this, a good one to try is [Live SASS Compiler](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass), once installed add the below to your VSCode config and it'll compile the SCSS files into CSS and put it in the correct location.

```JSON
"liveSassCompile.settings.formats":[{
        "format": "compressed",
        "extensionName": ".min.css",
        "savePath": "~/../"
    },
]
```