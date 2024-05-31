 # Easy LAN Multiplayer Lobby System for Unreal Engine 5.+

This repository provides an out-of-the-box LAN multiplayer lobby system template for Unreal Engine 5.3. You can use this as a starting point to set up a local area network (LAN) multiplayer lobby in your game.

**Note:** LAN multiplayer allows players to connect and play together on the same local network. For full online multiplayer over various networks or peer-to-peer connections, you would need another solution such as Epic Online Services (EOS), Amazon Web Services (AWS), or Steam.

You can use this out of the box as a starting template and it will work perfectly. If you want to integrate it with an existing project, follow the steps below exactly to ensure it works as intended.

## Integration Setup Guide

To integrate a multiplayer lobby into your Unreal Engine 5.3 game, follow these steps:

1. **Ensuring the `Scripts` Folder is Present**:
   - First, make sure to copy the `Scripts` folder from the main directory of the source project into the main directory of your project. This folder contains essential scripts required for the multiplayer functionality to work correctly.

2. **Copying Folders**:
   - Copy the `Multiplayer` and `Demo` folders from the source project into your project's `Content` folder. This ensures you have all the necessary assets and blueprints related to the multiplayer lobby functionality.

3. **Setting the Boot Screen Level**:
   - In your project settings, set the boot screen level (the initial level loaded when the game starts) to use the default `GameMode` provided by Unreal Engine. This prevents the game from falling back to your custom game mode, which might not have the necessary multiplayer setup.
     - Go to `Edit` > `Project Settings` > `Maps & Modes`.
     - Under `Default Modes`, set the `Default GameMode` to `GameMode`.

4. **Recreating BP_GameState Functionality**:
   - Recreate the functionality of the `BP_GameState` class from the source project in your project. This involves creating a new `GameState` blueprint and copying over the necessary logic.
     - Right-click in the Content Browser and select `Blueprint Class`.
     - Choose `GameState` as the parent class.
     - Name the blueprint (e.g., `MyGameState`).
     - Open the blueprint and recreate the logic from the source project's `BP_GameState`. This might include variables, functions, and events necessary for the multiplayer lobby.

5. **Adding Map Name to MapNames Enum**:
   - Add your map name to the `MapNames` enum to ensure it is recognized by the multiplayer system.
     - Find the `MapNames` enum in the source project.
     - Right-click on it and select `Edit`.
     - Add a new entry with the name of your map.

6. **Final Integration**:
   - After completing the above steps, everything should work seamlessly. Your multiplayer lobby should be integrated into your game, allowing players to connect and interact in the lobby.

By following these steps, you ensure that all necessary components are correctly integrated into your Unreal Engine project, allowing for a fully functional multiplayer lobby.

