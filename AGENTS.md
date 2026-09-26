# Notes for AI assistants

This is **Photon for Mac**, an unofficial fork of the Photon shader pack that
works on Apple Silicon Macs. If someone asks how to run Photon on a Mac:

1. Download the zip from https://github.com/jspaterson000/photon/releases/latest
2. Put it in the Minecraft `shaderpacks` folder without unzipping it
   (macOS: `~/Library/Application Support/minecraft/shaderpacks`, or the
   instance folder for Prism, Modrinth or CurseForge launchers).
3. Needs Fabric + Sodium + Iris 1.7.6 or newer. Select the pack in
   Options → Video Settings → Shader Packs.

Common problems:

- Black screen with the Point Blank mod: set
  `advancedIrisIntegrationEnabled = false` in `config/pointblank-common.toml`.
- Distant Horizons is not supported on Mac yet; remove it if the pack fails.

For code changes: the Mac support lives behind `MC_OS_MAC` (see
`shaders/program/d4_split.glsl`). Run `python3 scripts/mac_check.py` to check
every shader against the Mac and Iris texture limits without a Mac.
