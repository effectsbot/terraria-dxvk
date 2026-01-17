# FNA-Terraria
This repository contains up to date builds of [FNA](https://github.com/FNA-XNA/FNA) for use with Terraria on Linux. It also includes additional libraries to allow use of FNA3D's D3D11 driver, which uses [dxvk](https://github.com/doitsujin/dxvk) behind the scenes.

# How do I use this?
Download the latest tarball from releases, extract it, then move the extracted files into their respective directory.
```
FNA.dll --> $HOME/.local/share/Steam/steamapps/common/Terraria
FNA.dll.config --> $HOME/.local/share/Steam/steamapps/common/Terraria
lib64/* --> $HOME/.local/share/Steam/steamapps/common/Terraria/lib64
```

If you're using the flatpak version of Steam, move them into the following directories instead.
```
FNA.dll --> $HOME/.var/app/com.valvesoftware.Steam/data/Steam/steamapps/common/Terraria
FNA.dll.config --> $HOME/.var/app/com.valvesoftware.Steam/data/Steam/steamapps/common/Terraria
lib64/* --> $HOME/.var/app/com.valvesoftware.Steam/data/Steam/steamapps/common/Terraria/lib64
```

Once you're done with that, add this line to Terraria's launch options, which is accessible under its properties.
```
FNA_PLATFORM_BACKEND=SDL2 %command% /gldevice:D3D11
```
`/gldevice:D3D11` is optional if you prefer using the OpenGL backend. `FNA_PLATFORM_BACKEND=SDL2` on the other hand is not.

If you accidentally delete something from your game's directory, open up Steam, then go into Terraria's properties and verify the integrity of its files under the "Installed Files" tab.

If you want to revert back to Terraria's FNA build, remove everything inside the `lib64` directory in your game's folder. After that, verify the integrity of its files.

# How do I build/compile this myself?

WIP
