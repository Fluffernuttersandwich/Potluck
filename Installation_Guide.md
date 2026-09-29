# 🍲 Potluck Installation Guide

This guide covers installing **Potluck** through Wabbajack.

---

## 📚 Table of Contents

- [Before You Begin](#before-you-begin)
- [Clean Stardew Valley Installation](#clean-stardew-valley-installation)
- [Vortex](#vortex)
- [Game Directory](#game-directory)
- [AppData Mods](#appdata-mods)
- [SMAPI](#smapi)
- [Mod Organizer 2](#mod-organizer-2)
- [Install Potluck](#install-potluck)
- [Launch Potluck](#launch-potluck)

---

## Before You Begin

Potluck expects a **clean, fresh Steam installation of Stardew Valley on Windows 10 or 11**.

Do not install Potluck over an existing manually modded, Vortex-managed, or SMAPI-modded game installation.

Before continuing, remove any previous Stardew Valley mods and mod-management leftovers.

---

## Clean Stardew Valley Installation

A normal Steam uninstall may leave modded or manually added files behind.

For the cleanest starting point:

1. Uninstall Stardew Valley through Steam.
2. After uninstalling, locate the old Stardew Valley game directory.
3. If the directory still exists, **delete the remaining Stardew Valley folder and its contents**.
4. Reinstall Stardew Valley through Steam.
5. Launch the unmodded game once to confirm it works normally.
6. Close the game before installing Potluck.

Potluck should start from a clean game installation, not one that previously contained SMAPI or other manually installed mods.

---

## Vortex

If you previously managed Stardew Valley with **Vortex**, make sure it is no longer deploying mods into the game.

Before installing Potluck:

1. Open Vortex.
2. Disable all Stardew Valley mods.
3. Purge deployed Stardew Valley mods.
4. Run Deploy.
5. Confirm Vortex is no longer managing or deploying files into your Stardew Valley installation.

**Do not leave Vortex-managed Stardew Valley mods enabled or deployed while using Potluck.**

Vortex and Potluck's Mod Organizer 2 installation should not manage the same Stardew Valley setup at the same time.

---

## Game Directory

Your Stardew Valley game directory must not contain leftover manually installed mods or files from a previous modded installation.

This includes old copies or remnants of:

- SMAPI
- Mods
- Mod loaders
- Frameworks
- Manually installed mod files
- Files previously deployed by Vortex

This is why uninstalling Stardew Valley, deleting the remaining game directory, and reinstalling is strongly recommended.

**Do not copy your old modded game directory into the fresh installation.**

---

## AppData Mods

Some Stardew Valley mods or previous setups may leave files outside the main Steam game directory.

Check your Stardew Valley-related folders under Windows **AppData** and remove any old `Mods` folder or previously installed mod files that could be loaded independently of Potluck.

Windows key + R will open the Windows Run prompt. Paste `%AppData%\StardewValley` into the Run prompt and hit Enter (or Ok). 

If you intentionally keep backups of old mods, store them somewhere that Stardew Valley and SMAPI will not treat as an active mod directory. If you see a Mods folder in this AppData folder section, delete it.

Potluck should not be mixed with a second collection of mods stored outside its MO2 installation.

---

## SMAPI

**Do not install your own copy of SMAPI into the Stardew Valley game directory.**

Potluck already provides the supported SMAPI installation through its Mod Organizer 2 environment.

Installing another copy manually can create conflicts and makes troubleshooting significantly more difficult.

---

## Mod Organizer 2

**Do not download or install your own copy of Mod Organizer 2 for Potluck.**

Wabbajack installs the correct portable MO2 environment for Stardew Valley as part of Potluck.

Always launch Potluck using the copy of Mod Organizer 2 provided with the mod list.

---

# 📦 Install Wabbajack

Download the latest version of the Wabbajack application from:

https://www.wabbajack.org/

Open Wabbajack and sign into **Nexus Mods** when prompted.


<img width="2136" height="970" alt="image" src="https://github.com/user-attachments/assets/eb91534e-1664-452d-b24f-8921a4f32fe0" />

> [!TIP]
> Keep the Wabbajack application installation and your mod list outside Windows-protected folders.

Avoid installing Wabbajack or the Potluck modlist into locations such as:

``` text
C:\Program Files\
C:\Program Files (x86)\
C:\Users\<You>\Documents\
C:\Users\<You>\Desktop\
C:\Users\<You>\OneDrive\
```

You _cannot_ run the wabbajack.exe from: 
``` text
C:\
```


I'd recommend creating a folder like one of these for installing the wabbajack.exe file into like this:
``` text
C:\Wabbajack
or
D:\Wabbajack
```


<img width="1414" height="748" alt="image" src="https://github.com/user-attachments/assets/10369f77-189e-4009-a204-d78c112d7fe0" />


Do **not** use your Stardew Valley game directory as the Potluck installation location. 

Do not run the wabbajack.exe from your game directory either!

------------------------------------------------------------------------

### Create the Potluck Installation Folder

A simple folder near the root of an SSD is recommended.

Choose one like the Examples below:

``` text
C:\Wabbajack_ModLists\Potluck
or
D:\Wabbajack_ModLists\Potluck
or
E:\Potluck
```

Your Wabbajack folder, Potluck installation folder, and vanilla Stardew Valley game installation are all **separate locations**.

---

## Install Potluck

1. Launch **Wabbajack**.
2. Gears icon. Confirm you are signed into your NexusMods account within the Wabbajack app.
3. Browse Lists tab > Search for Stardew Valley
4. Select **Potluck**.
5. Choose your Potluck installation location. Must not be a protected Windows folder. 
6. Wabbajack will populate a downloads folder within the installation folder.
7. Start the installation process.
8. Allow Wabbajack to complete the installation.

A **Nexus Mods Premium** account is strongly recommended for automated downloads. Free accounts require hours of clicking.

---

## Launch Potluck

1. Open the Potluck installation folder.
2. Launch the included **Mod Organizer 2** exe file.
3. Use the supplied **Potluck default profile**.
4. Launch Stardew Valley using the configured Potluck/SMAPI executable inside MO2.

For your first launch, do not add, remove, update, or disable mods.

Confirm the default Potluck installation works correctly before customizing it.


> [!TIP]
> With MO2 open, pin it to your system tray. Or, make a shortcut on your desktop for easy access.

---

**Installation complete. Welcome to Potluck. 🍲**
