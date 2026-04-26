# Voxy World Gen V2

![Logo](src/main/resources/logo.png)

This is a rewrite of my old Voxy World Gen mod, this mod is NOT a fork of the passive chunk generator mod and instead is a entirely different mod.

## Features

- Generates chunks very fast in the background and auto-ingest them with voxy.
- Configurable generation speed and queue size.
- Tellus integration. https://github.com/Yucareux/Tellus
- Server-side support
<<<<<<< Updated upstream

## Dependencies

- **Minecraft**: 1.21.6 - 1.21.11 (Tested on 1.21.11, anything less is considered unstable and may not work)
- **Fabric Loader**: >= 0.16.0
- **Java**: 21 (Required)
- **Fabric API**
- **Cloth Config**: >= 15.0.127
=======
- `/voxygen` commands for runtime control

## Commands

| Command | Description |
|---------|-------------|
| `/voxygen start` | Resume background generation |
| `/voxygen stop` | Pause background generation |
| `/voxygen status` | Show current status, active tasks, remaining chunks |

> Requires OP level 2.

## Dependencies

- **Minecraft**: 1.21.1
- **Fabric Loader**: >= 0.18.3
- **Java**: 21 (Required)
- **Fabric API**
- **Cloth Config**: >= 15.0.127
- **Voxy**: compatible release for 1.21.1
>>>>>>> Stashed changes

## Building

This project requires Java 21.

```bash
# Clone the repo
git clone https://github.com/iSeeEthan/voxy_worldgen_v2.git

# Build
./gradlew build
```

Artifacts are output to `build/libs/`.

## Configuration

Config files are located in `config/voxyworldgenv2.json`.

## License

CUSTOM, refer to LICENSE file for more information.
