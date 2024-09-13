# **Super Mario Eclipse - 4K & HD Custom Texture Packs**

This repository contains 4K and HD texture packs for **Super Mario Eclipse**, a modification of Super Mario Sunshine. The texture packs significantly enhance the visual quality of the game and are available in both PNG and DDS formats, depending on performance and quality requirements in the Dolphin Emulator.

## **Table of Contents**
1. [Texture Packs](#texture-packs)
2. [How to Install Custom Textures in Dolphin](#how-to-install-custom-textures-in-dolphin)
3. [Upscaling Process](#upscaling-process)
4. [Unmodified Texture Dumps](#unmodified-texture-dumps)
5. [Texture Dumping Tool](#texture-dumping-tool)
6. [Contributing](#contributing)
7. [Credits](#credits)

---

## **Texture Packs**

There are four different versions of the texture packs available for download in the **Releases** section of the main branch:

- **4K PNG Texture Pack**: Offers maximum visual quality.
- **HD PNG Texture Pack**: Provides high quality while maintaining a balance between quality and performance.
- **4K DDS Texture Pack**: Optimized for faster loading times while retaining 4K textures.
- **HD DDS Texture Pack**: Optimized for performance with fast loading times and high-quality textures.

Each version is designed to meet different performance needs, ensuring users can choose based on their hardware capabilities.

---

## **How to Install Custom Textures in Dolphin**

### **1. Preparing Dolphin Emulator**
Ensure that the latest version of Dolphin Emulator is installed. The latest version can be downloaded from [https://dolphin-emu.org/](https://dolphin-emu.org/).

### **2. Configuring Dolphin Emulator Settings**
The following settings must be enabled in Dolphin to correctly load the custom textures:

1. Open Dolphin Emulator.
2. Go to `Graphics Settings` > `Advanced` tab and enable:
   - **Load Custom Textures**: This setting allows the emulator to load external texture packs.
   - **Prefetch Custom Textures** (Optional): Improves performance by preloading all textures into memory.

### **3. Increasing Internal Resolution**
To display high-resolution textures correctly, it is essential to adjust the internal resolution:

1. Go to `Graphics Settings` > `Enhancements` tab.
2. Set the **Internal Resolution** according to your display and hardware capabilities:
   - For 1080p displays, the HD texture pack is recommended for better performance.
   - If your system is capable, the 4K texture pack can be used even on a 1080p display, as it provides better quality than the HD pack.
   - For 1440p (2K) or higher displays, the difference between the HD and 4K packs becomes more apparent. Using the 4K pack is recommended for the best visual experience.

   **Note**: Adjusting the internal resolution is necessary to properly display high-resolution textures. Without this adjustment, the textures may not appear as intended.

### **4. Place Textures in the Correct Directory**
Navigate to Dolphin Emulator’s **User Directory**:

- **Windows**: Go to `C:\Users\<YourUsername>\AppData\Roaming\Dolphin Emulator\Load\Textures\`. You can also quickly access this by typing `%appdata%` in the Windows search bar, then navigating to `Dolphin Emulator/Load/Textures/`.
- **macOS**: Navigate to `~/Library/Application Support/Dolphin/Load/Textures/`.
- **Linux**: Navigate to `~/.local/share/dolphin-emu/Load/Textures/`.

Place the texture files directly in the `GMSE04` folder inside the `Load/Textures` directory.

**Important:**
- If the texture pack you downloaded already contains a `GMSE04` folder, do **not** copy the entire folder into `Load/Textures/GMSE04`. Instead, open the `GMSE04` folder from the texture pack and place its contents directly into `Load/Textures/GMSE04`.
- If the texture pack contains only the texture files (without a `GMSE04` folder), place those texture files directly into `Load/Textures/GMSE04`.
- If the `GMSE04` folder doesn’t exist in the `Load/Textures` directory, create it manually and place the files there.

### **5. Launching the Game**
Once the textures are placed in the correct folder and the settings are configured, launch **Super Mario Eclipse** in Dolphin. The custom textures will load automatically.

---

## **Upscaling Process**

Follow these steps to upscale textures using **Chainner**:

1. Download and install the latest version of Chainner here: [https://github.com/chaiNNer-org/chaiNNer/releases](https://github.com/chaiNNer-org/chaiNNer/releases).  
2. Install all packages ("PyTorch", "NCNN", "ONNX" including all sub-packages of each package) in the Dependency Manager of Chainner.  
3. Download & open the chain from `OTHER_FILES/UPSCALING.chn` in Chainner and get the 4 different models used in the chain from here: [https://github.com/Venomalia/Hdcube](https://github.com/Venomalia/Hdcube).  
4. In Chainner, after you have loaded the chain, change the paths of the **input** and **output** folders as well as the paths for the 4 models used in the chain.  
5. Press the **Start** button to begin upscaling and wait until it’s finished. (Tip: Press the **Lock Icon** in the bottom left of Chainner to prevent accidentally modifying the chain while it's running).

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
2. **Make the necessary changes**: Ensure that the textures you modify or add are updated in all four texture versions (`4K PNG`, `4K DDS`, `HD PNG`, and `HD DDS`). Consistency across the packs is required.
3. **Open a pull request**: Pull requests should be opened on the `main` branch. Be sure to explain the changes made in the pull request description.
4. **Submit the pull request**: After submission, your changes will be reviewed, and if they meet the requirements (i.e., all texture versions are updated), the pull request will be merged.

### **Important Notes for Contributing:**
- Pull requests **must** apply updates to **all four texture packs** (`4K PNG`, `4K DDS`, `HD PNG`, and `HD DDS`). This ensures that all versions remain synchronized.
- Contributions that update only one or a few of the packs will not be merged.

For discussions, suggestions, or questions, feel free to join the **Super Mario Eclipse Discord Server**:  
[https://discord.com/invite/u6NHuHVRpJ](https://discord.com/invite/u6NHuHVRpJ)

---

## **Credits**

- **iZePlayz**: Creator of the HD and 4K textures.
- **AlexWolfz**: Converted the textures to DDS format.
- **Venomalia**: Created the Dolphin Texture Dumping tool and upscaling models.

---

## **Contact**

For inquiries or further assistance, please reach out via GitHub or the Discord server.
