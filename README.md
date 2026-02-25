# Two Worlds – Mod Installer v1.0.3

Installs `.wd` mod files for Two Worlds 1 and automatically activates them in the Windows Registry.

## Quick Guide

1. **Launch the installer** – The game directory is detected automatically (Steam, GOG, CD, SDK)
2. **Select mod** – Click "Browse..." and choose the `.wd` file
3. **Install** – One click does everything:
   - Creates the `Mods` folder next to the game EXE
   - Copies the `.wd` file into it
   - Activates the mod in the registry (`HKCU\SOFTWARE\Reality Pump\TwoWorlds\Mods`)
4. **Play** – Launch Two Worlds, the mod is active right away

No admin rights required.

## Supported Installations

- Steam (all libraries, automatic detection via appmanifest)
- GOG Galaxy
- CD/Retail (Reality Pump / TopWare)
- SDK (`D:\Games\TwoWorlds`)

## Building

Prerequisite: `pip install pyinstaller`

```
pyinstaller --onefile --windowed --name "TwoWorlds_Mod_Installer" --add-data "Logo.png;." --icon "Logo.ico" tw_mod_installer.py
```

Or simply run `build.bat`. The finished EXE will be in `dist\`.

## Help Menu

- **Quick Guide** – Short usage guide built into the tool
- **About / Credits** – Credits with clickable links

## Credits

- **Alchemy Fox Studio** – [alchimist-sotw.de](https://alchimist-sotw.de/) · [github.com/MedievalDev](https://github.com/MedievalDev?tab=repositories)
- **Buglord** (Registry logic) – [Mod Selector Source](https://github.com/buglord/Two-Worlds-1-Misc-Projects/tree/main/Mod%20Selector)
