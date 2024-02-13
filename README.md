# Getting started with Cities Skylines II Modding


## Requisites

- Visual Studio 2022 or other IDE
- Knowledge of C# Programming Language and [ECS]() (Entity Component System)

## 1. Requirements

### 1. Install BepInEx v5

Download and Install [BepInEx 5](https://thunderstore.io/c/cities-skylines-ii/p/BepInEx/BepInExPack/) by extracting the contents of the Archive to your Cities Skylines II installation directory (C:/Program Files (x86/Steam/steamapps/common/Cities Skylines II). Make sure this directory now additionally includes the following files:

- `BepInEx` (folder)
- `doorstop_config.ini`
- `winhttp.dll`

Make sure to edit the `BepInEx/config/BepInEx.cfg` file and set `Enable` to `true` for the `Logging.Console` section, like so:

```cfg
[Logging.Console]
## Enables showing a console for log output.
# Setting type: Boolean
# Default value: false
Enabled = true
```



### 2. Set up Solution for your Mod
1. Clone/Download [Example Mod](https:github.com/89pleasure/cities2-no-unique-buildings) (credit to 89pleasure for providing) to your computer


2. Using your IDE or any other Search and Replace-Tool, replace all occurences of `NoUniqueBuildings` with your mod name. Make sure to also rename the `.sln` file, the `.csproj` file and the project folder to your new chosen name


3. Open the `.sln` file with your IDE. You should now see the project structure of the mod. Wait for NuGet to restore the packages.


4. Open `GlobalProperties.props.dist` and rename it to `GlobalProperties.props`. Change the `GamePath` to your Cities Skylines II game folder and choose the correct BepInEx version. This will copy the dll to your BepInEx plugins folder automatically (on build).

5. Start Cities Skylines II (not using Thunderstore/Modman) and check if the mod is loaded. You should see a console window with your mod name and version. 

6. You can now start coding your mod. The `YourModNameSystem.cs` file is the main entry point for your mod.


### Additional Ressources

- [Wiki Page](https://wiki.ciim.dev/) done by CaptainOfCoit
- [Cities Skylines II Wiki](https://cs2.paradoxwikis.com/Cities_Skylines_II_Wiki)
- [Unofficial Cities Skylines II Modding Discord](https://discord.gg/vd7HXnpPJf)