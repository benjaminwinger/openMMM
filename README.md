# openMMM
openMorrowind Mod Manager. A cli tool for linux to add mods to openMW

## Usage

* First copy openmmm.py to your path

```sudo cp openmmm.py /usr/bin```

* cd to where your uncompressed mod folders are stored

```cd /some/path```

* Make sure the structure of the folder is correct. Some mod archives contain a single 'Data Files' directory and some additional files, others put everything into where they are unpacked, still others put everything which belongs to the mod into a specially named folder and meta files (like readmes) into the folder where the mod is unpacked. You need to normalize this:

    Put all ESPs into the toplevel of the folder in which you want to put the mod.
    Put all resource folders into the toplevel of your mod folder. The relevant folders are 'BookArt', 'Fonts', 'Icons', 'Meshes', 'Music', 'Sound', 'Splash', 'Textures' and 'Video'. Not every mod contains all of these folders (and actually most mods don't contain most or even any of them), but if they belong to the mod, they must be in its toplevel.

    From the [openMW wiki](https://wiki.openmw.org/index.php?title=Mod_installation)

* Make sure the openmw-launcher is not running


* run openmmm.py and give it the path to the mod you want to install

```openmmm.py yourModFolder```

  This will copy the mod folder to ```~/MWmods/``` and add the needed data="PathToYourMod" in ```~/.config/openmw/openmw.cfg```. It will also make a backup of the config file in ~/.config/openmw/

* Start openMW by running

```
openmw-launcher
```



Your mods should now appear in the data tab of the launcher (if esp/esm files) or should show up in game (if textures)

## Issues

If you add mods when the openmw-launcher is running the mods will be removed from the config file when the openmw-launcher is closed

This project is not affiliated with openMW
