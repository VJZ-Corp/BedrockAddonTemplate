# Minecraft Bedrock Addon Development in Visual Studio 2022
This repository serves as a starter template for developing *Minecraft: Bedrock Edition* addons using TypeScript in Visual Studio 2022. 

The official supported approach uses Visual Studio Code using extensions (see https://learn.microsoft.com/en-us/minecraft/creator/documents/scripting/developer-tools?view=minecraft-bedrock-stable), but this starter template allows seemless integration with a more robust IDE like Visual Studio 2022.

## Setup Instructions
1. After cloning this template, run `npm install` in a Developer Powershell window.
2. Open the file `.env`. This contains the environment variables to use to configure project:
	1. `PROJECT_NAME` is used as the folder name under all the assets are going to be deployed inside the game directories (e.g., `development_behavior_packs\PROJECT_NAME`, `development_resource_packs\PROJECT_NAME`).
	2. `MINECRAFT_PRODUCT`. You can choose to use either Minecraft or Minecraft Preview to debug and work with your scripts. These are the possible values: `BedrockUWP, PreviewUWP, Custom`. Use `Custom` in case of deploy on any other path.
	3. `CUSTOM_DEPLOYMENT_PATH`. In case of using `Custom` for `MINECRAFT_PRODUCT`, this is the path used to generate the assets.
3. Modify `package.json`'s `name` and `version` fields to customize it for your addon.
4. Modify `behavior_packs\PROJECT_NAME` and `resource_packs\PROJECT_NAME`'s `manifest.json` to reflect what is shown in the game.
5. Launch *Minecraft: Bedrock Edition* and enable the behavior packs: *Settings > Global Resources > My Packs > Activate*.
6. Play with the addon you just created! Use the Minecraft command `/reload` to catch new changes (after you have locally deployed again).

**Credit**: Most of the starter template was adapted from https://github.com/microsoft/minecraft-samples/tree/main/addon_starter but modified to support VS2022.