# **Super Mario Eclipse - Custom Texture Pack**

This repository contains a custom texture pack for **Super Mario Eclipse**, a modification of Super Mario Sunshine. The texture pack significantly enhances the visual quality of the game and is available in the **Releases** section of the main branch.

Earlier releases provided separate HD and 4K versions. These versions have now been merged into a single texture pack. The current version is based mostly on the former 4K pack, while some extremely large textures were reduced in resolution where the difference would not be visible in-game. This keeps the visual quality very close to the previous 4K version while reducing the overall file size.

## **Table of Contents**
1. [Texture Pack](#texture-pack)
2. [How to Install Custom Textures in Dolphin](#how-to-install-custom-textures-in-dolphin)
3. [Upscaling Process](#upscaling-process)
4. [Unmodified Texture Dumps](#unmodified-texture-dumps)
5. [Texture Dumping Tool](#texture-dumping-tool)
6. [Contributing](#contributing)
7. [Credits](#credits)
8. [Contact](#contact)

---

## **Texture Pack**

The current release contains a single texture pack. It replaces the previous separate HD and 4K versions.

The old HD version was primarily a downscaled version of the higher-resolution textures, while the old 4K version used the original higher-resolution textures. In the current merged version, around 95-98% of the textures are still based on the former 4K version.

Some very large textures were reduced in resolution because they are never displayed at their full size in-game. For example, if a texture is much larger than what can be shown on a 4K display, Dolphin or the game would downscale it anyway. In those cases, reducing the texture resolution does not create a visible difference during gameplay, but it helps reduce the download size and storage requirements.

In practice, the current texture pack should look very similar to the previous 4K pack while being smaller and easier to distribute.

---

## **How to Install Custom Textures in Dolphin**

### **1. Preparing Dolphin Emulator**
Ensure that the latest version of Dolphin Emulator is installed. The latest version can be downloaded from [https://dolphin-emu.org/](https://dolphin-emu.org/).

### **2. Configuring Dolphin Emulator Settings**
The following settings must be enabled in Dolphin to correctly load the custom textures:

1. Open Dolphin Emulator.
2. Go to `Graphics Settings` > `Advanced` tab and enable:
   - **Load Custom Textures**: This setting allows the emulator to load external texture packs.
   - **Prefetch Custom Textures** (Optional): Improves performance by preloading all textures into memory. This may require more RAM.

### **3. Increasing Internal Resolution**
To display high-resolution textures correctly, it is recommended to increase the internal resolution:

1. Go to `Graphics Settings` > `Enhancements` tab.
2. Set the **Internal Resolution** according to your display and hardware capabilities.

For the best visual result, use an internal resolution that matches or exceeds your display resolution. Lower internal resolutions may still work, but the texture pack may not appear as sharp as intended.

> **Note**: The native-resolution goop graphics hack is not recommended while using this texture pack, as it can prevent some enhanced textures from being displayed as intended.

### **4. Place Textures in the Correct Directory**
Navigate to Dolphin Emulator's **User Directory**:

- **Windows**: Go to `C:\Users\<YourUsername>\AppData\Roaming\Dolphin Emulator\Load\Textures\`. You can also quickly access this by typing `%appdata%` in the Windows search bar, then navigating to `Dolphin Emulator/Load/Textures/`.
- **macOS**: Navigate to `~/Library/Application Support/Dolphin/Load/Textures/`.
- **Linux**: Navigate to `~/.local/share/dolphin-emu/Load/Textures/`.

Place the texture files directly in the `GMSE04` folder inside the `Load/Textures` directory.

**Important:**
- If the texture pack you downloaded already contains a `GMSE04` folder, do **not** copy the entire folder into `Load/Textures/GMSE04`. Instead, open the `GMSE04` folder from the texture pack and place its contents directly into `Load/Textures/GMSE04`.
- If the texture pack contains only the texture files without a `GMSE04` folder, place those texture files directly into `Load/Textures/GMSE04`.
- If the `GMSE04` folder does not exist in the `Load/Textures` directory, create it manually and place the files there.

### **5. Launching the Game**
Once the textures are placed in the correct folder and the settings are configured, launch **Super Mario Eclipse** in Dolphin. The custom textures will load automatically.

---

## **Upscaling Process**

Follow these steps to upscale textures using **chaiNNer**:

1. Download and install the latest version of chaiNNer here: [https://github.com/chaiNNer-org/chaiNNer/releases](https://github.com/chaiNNer-org/chaiNNer/releases).  
2. Install all packages (`PyTorch`, `NCNN`, and `ONNX`, including all sub-packages of each package) in the Dependency Manager of chaiNNer.  
3. Download and open the chain from `OTHER_FILES/UPSCALING.chn` in chaiNNer and get the four different models used in the chain from here: [https://github.com/Venomalia/Hdcube](https://github.com/Venomalia/Hdcube).  
4. In chaiNNer, after you have loaded the chain, change the paths of the **input** and **output** folders as well as the paths for the four models used in the chain.  
5. Press the **Start** button to begin upscaling and wait until it is finished. Tip: Press the **Lock Icon** in the bottom left of chaiNNer to prevent accidentally modifying the chain while it is running.

---

## **Unmodified Texture Dumps**

The repository contains original, unmodified textures dumped from Super Mario Eclipse. These textures can be found in the `TEXTURE_DUMPS/GMSE04` folder and can be used for reference or modification. These are the base textures extracted from the game before any enhancements.

---

## **Texture Dumping Tool**

For those interested in extracting textures, the **DolphinTextureExtraction-tool** can be used to dump textures from the game. This tool is useful for both standard and custom texture creation.

- **Download**: [https://github.com/Venomalia/DolphinTextureExtraction-tool](https://github.com/Venomalia/DolphinTextureExtraction-tool)

> **Note**: Some textures, such as HUD, UI, and font textures, may need to be manually dumped, as not all textures are automatically captured by the tool.

---

## **Contributing**

To contribute to this project, follow these steps:

1. **Fork the repository**: This will create a personal copy of the project on your GitHub account.
2. **Make the necessary changes**: Modify or add the relevant texture files in the current texture pack structure.
3. **Open a pull request**: Pull requests should be opened on the `dev` branch. Be sure to explain the changes made in the pull request description.
4. **Submit the pull request**: After submission, your changes will be reviewed. If they meet the project requirements, they may be merged.

### **Important Notes for Contributing:**
- The texture pack now uses a single merged version instead of separate HD and 4K versions.
- Please make sure your changes fit the current pack structure and do not reintroduce separate HD or 4K texture versions.
- Pull requests should target the `dev` branch, not the `main` branch.

For discussions, suggestions, or questions, feel free to join the **Super Mario Eclipse Discord Server**:  
[https://discord.com/invite/u6NHuHVRpJ](https://discord.com/invite/u6NHuHVRpJ)

---

## **Credits**

- **iZePlayz**: Creator of the HD and 4K textures and the merged texture pack.
- **AlexWolfz**: Converted the textures to DDS format.
- **Venomalia**: Created the Dolphin Texture Dumping tool and upscaling models.
- **CoNesTra**: Created the autosave and loading icons.
- **KaonsYT**: Created some HUD textures for the characters and water meter.
- **CanOfDarkFruit**: Added many textures created and shared by people on Discord.
- **Many other people from the Super Mario Eclipse Discord Server!**

---

## **Contact**

For inquiries or further assistance, please reach out via GitHub or the Discord server.
