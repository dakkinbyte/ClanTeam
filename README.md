# Clan Team Plugin

## Overview

The Clan Team plugin is designed for the Oxide modding framework, specifically for Rust game servers. It automatically manages and organizes clan members into teams, ensuring that players within the same clan are grouped together. This plugin leverages the Clans plugin to retrieve clan information and manage team assignments.

## Features

- Automatically creates and manages teams for clan members.
- Ensures that clan members are always in the same team.
- Handles clan creation, updates, and destruction events.
- Integrates with the Clans plugin to retrieve clan and member information.
- Provides feedback and logging for various operations and errors.

## Requirements

- **Oxide Modding Framework**: This plugin is built for servers running the Oxide framework.
- **Clans Plugin**: The Clan Team plugin requires the Clans plugin to function properly.

## Installation

1. Ensure that your Rust server is running the Oxide modding framework.
2. Install the Clans plugin if it is not already installed.
3. Place the `ClanTeam.cs` file into the `oxide/plugins` directory of your Rust server.
4. Restart the server or load the plugin using the Oxide console command: `oxide.reload ClanTeam`.

## Usage

The plugin automatically manages clan teams without the need for manual intervention. It listens for clan-related events and updates team assignments accordingly.

### Key Functions

- **GenerateClanTeam**: Creates a team for a given list of clan member IDs.
- **IsAnOwner**: Checks if a player is the owner of their clan.
- **ClanTag**: Retrieves the clan tag for a given member ID.
- **ClanPlayers**: Retrieves a list of clan members for a given player.
- **ClanPlayersTag**: Retrieves a list of clan members for a given clan tag.

### Hooks

- **OnClanCreate**: Triggered when a new clan is created.
- **OnClanUpdate**: Triggered when a clan is updated.
- **OnClanDestroy**: Triggered when a clan is destroyed.
- **OnPlayerSleepEnded**: Triggered when a player wakes up, ensuring they are in the correct team.

## Logging

The plugin provides console output for various operations, including errors and successful operations, to help with debugging and monitoring.

## Troubleshooting

- Ensure the Clans plugin is installed and loaded correctly.
- Check the server console for any error messages or logs provided by the plugin.
- Verify that the Oxide framework is up to date.

## Contributing

Contributions to the Clan Team plugin are welcome. Please fork the repository and submit a pull request with your changes.

## License

This plugin is open-source and available under the MIT License. See the LICENSE file for more information.
