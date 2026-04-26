# Voxy World Gen V2

![Logo](src/main/resources/logo.png)

Background chunk pre-generation for [Voxy](https://modrinth.com/mod/voxy). Generates chunks silently in the background and auto-ingests them into Voxy's LOD system — no need to manually fly around.

## Features

- Fast background chunk generation with automatic Voxy ingestion
- Configurable generation speed and queue size
- TPS-aware throttling — backs off automatically when server is under load
- Tellus integration for terrain sampling
- Server-side support with multiplayer chunk streaming
- `/voxygen` commands for runtime control
- Colored chat feedback: gold `Voxygen |` prefix, green for success, red for errors
- Smart state detection — warns if generation is already running/stopped
- Generation starts **paused** by default — requires `/voxygen start` (configurable via `autoStartOnLoad`)
- F3 debug overlay shows generation status (paused/running/throttled), stats, rate, ETA

## Commands

| Command | Description |
|---------|-------------|
| `/voxygen start` | Resume background generation |
| `/voxygen stop` | Pause background generation |
| `/voxygen status` | Show current status (PAUSED/RUNNING/THROTTLED), active tasks, remaining chunks |

> Requires OP level 2.

## Configuration

Config file: `config/voxyworldgenv2.json`

| Option | Default | Description |
|--------|---------|-------------|
| `enabled` | `true` | Enable/disable the mod |
| `autoStartOnLoad` | `false` | Auto-start generation on world load (if `false`, requires `/voxygen start`) |
| `showF3MenuStats` | `true` | Show generation stats in the F3 debug overlay |
| `generationRadius` | `128` | Chunk radius for background generation |
| `maxQueueSize` | `20000` | Maximum chunks queued for generation |
| `maxActiveTasks` | `20` | Maximum concurrent generation tasks |

## Dependencies

- **Minecraft**: 1.21.1
- **Fabric Loader**: >= 0.18.3
- **Java**: 21 (Required)
- **Fabric API**
- **Cloth Config**: >= 15.0.127
- **Voxy**: compatible release for 1.21.1

## Building

```bash
git clone <repo>
./gradlew build
```

Artifacts are output to `build/libs/`.

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for a full list of changes.

## License

CUSTOM, refer to LICENSE file for more information.
