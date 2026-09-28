# Shadow Dungeon

## Game Title

**Shadow Dungeon**

## Team Members

- Nguyen Tien Dung
- Pham Huy Hoang

## Game Concept

Shadow Dungeon is a cooperative 3D multiplayer dungeon RPG developed as a
final project for 3D Programming. Players choose a hero, explore a dangerous
dungeon, cooperate with other players, and use different abilities to defeat
enemy creatures and the dungeon boss.

The project is a customized version of Unity's multiplayer sample, adapted
with a new Shadow Dungeon identity, interface, controls, and multiplayer
configuration.

## Gameplay Objective

Players must work together to survive the dungeon, defeat enemy waves, support
their teammates, and defeat the final boss. Team coordination, movement,
target selection, and the effective use of hero abilities are important for
completing the level.

## Main Features

- Cooperative multiplayer gameplay.
- Multiple playable hero classes with different abilities.
- Character selection and in-game hero actions.
- Enemy encounters, boss combat, and dungeon exploration.
- Server-authoritative movement and combat synchronization.
- Multiplayer sessions through Unity Gaming Services.
- Customized Shadow Dungeon menu, HUD, title logo, and branding.
- `W/A/S/D` keyboard movement and `X` runtime network statistics toggle.

## Advanced Feature

- Real-time multiplayer synchronization using RPCs, NetworkVariables, and
  NetworkTransform.
- Server-authoritative gameplay to keep important game state consistent across
  clients.
- Unity Gaming Services Sessions and Relay for online player connection.
- Authentication profiles for identifying players and testing multiple local
  instances.
- Latency-masking action animations and runtime network statistics for
  observing network performance.

## Engine and Technology

- **Engine:** Unity `6000.0.52f1`
- **Language:** C#
- **Networking:** Unity Netcode for GameObjects `2.4.3`
- **Online services:** Unity Gaming Services Authentication `3.5.1` and
  Multiplayer Services `1.1.4`
- **Transport:** Unity Transport `2.5.1`
- **Camera:** Cinemachine `3.1.3`
- **Rendering:** Universal Render Pipeline `17.0.4`
- **Version control:** Git and Git LFS

## Controls

- `W/A/S/D`: Move the character.
- Left mouse button: Select a target or interact with the game world.
- `1`, `2`, `3`: Use hero actions.
- `4`: Open the emote bar.
- `X`: Toggle Runtime Network Stats.

## Run Instructions

### Requirements

- Unity Hub.
- Unity `6000.0.52f1`.
- Git and Git LFS.
- Internet access for Unity packages and online multiplayer sessions.
- For Ubuntu, use the Linux version of Unity Hub and a 64-bit Unity Editor.

### Clone and download assets

```bash
git clone https://github.com/Hoang271205/DemoDungeon.git
cd DemoDungeon
git lfs install
git lfs pull
```

### Open and run the project

1. Open **Unity Hub**.
2. Select **Add** and choose the cloned `DemoDungeon` folder.
3. Open it with Unity `6000.0.52f1`.
4. Wait for Unity to import the assets and finish compiling the project.
5. Open the project and press **Play** in the Unity Editor.
6. From the main menu, select **START SESSION** for online multiplayer or
   **START WITH DIRECT IP** for a local/direct-IP session.

The first launch may take longer while Unity creates the `Library` cache.

### Build a standalone version

Use Unity's **Build Profiles** window to select the target platform and build
the game. The repository does not include generated `Library`, `Builds`, or
`UserSettings` folders.

On Ubuntu, a Linux build can be started with:

```bash
chmod +x ShadowDungeon.x86_64
./ShadowDungeon.x86_64
```

## Asset and Resource Sources

- The original project structure, multiplayer sample assets, and networking
  reference implementation are based on Unity's Boss Room sample:
  [Unity Multiplayer Samples - Boss Room](https://github.com/Unity-Technologies/com.unity.multiplayer.samples.coop).
- Networking and multiplayer concepts are based on the official
  [Unity Netcode for GameObjects documentation](https://docs-multiplayer.unity3d.com/netcode/current/)
  and [Unity Gaming Services documentation](https://docs.unity.com/ugs/).
- Unity package dependencies are managed through the project's
  `Packages/manifest.json` and `Packages/packages-lock.json` files.
- Shadow Dungeon-specific branding, title artwork, menu changes, HUD changes,
  and control text were customized for this final project.
- Third-party notices and license information are available in
  [LICENSE.md](LICENSE.md) and [Third Party Notices.md](Third%20Party%20Notices.md).

## AI Tools Used

- **OpenAI Codex:** Used as a development assistant for codebase analysis,
  Unity input customization, Runtime Network Stats key customization, README
  preparation, build troubleshooting, and project verification.
- AI assistance supported the development process; the team remained
  responsible for integrating, testing, and presenting the final project.
