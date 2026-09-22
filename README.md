# KSA Free Bot

A safe, beginner-friendly Discord bot that is simple to run and easy to understand.

KSA Free Bot provides the everyday tools a small community needs without an external database, paid service, or complicated dashboard. Configuration stays in a local `.env` file, while polls and birthdays are stored in readable JSON files.

The project was created as a transparent alternative for beginners who have encountered unsafe downloads, hidden code, or people asking for payment just to set up a basic bot. The code is intentionally small enough to inspect, learn from, and build on.

## Highlights

- 12 top-level slash commands with 14 useful actions
- Server information, user information, avatars, and ping checks
- Polls with button voting and persistent results
- Private birthday details that store only the month and day
- Custom embeds for announcements
- Fun commands including coin flips, dice rolls, and random choices
- Clear help messages and straightforward Windows start and stop scripts

## Download

Download the latest package from the [Releases page](https://github.com/KSAGlory/KSA-Free-Bot/releases).

## Commands

| Command | Purpose |
| --- | --- |
| `/help` | Show the available commands |
| `/ping` | Check the bot's connection latency |
| `/uptime` | Show how long the bot has been online |
| `/serverinfo` | Display information about the server |
| `/userinfo` | Display information about a member |
| `/avatar` | Show a member's avatar |
| `/embedmessage` | Create a custom embed message as an administrator |
| `/poll create` | Create a button poll |
| `/poll end` | End a poll and show its results |
| `/birthday set` | Privately save a birthday month and day |
| `/birthday view` | Privately view saved birthday information |
| `/coinflip` | Flip a coin |
| `/roll` | Roll a die with a chosen number of sides |
| `/choose` | Choose between several options |

## Requirements

- Python 3.10 or newer
- A Discord application and bot token
- Permission to invite the bot to your server

## Setup

### 1. Create the Discord application

Open the [Discord Developer Portal](https://discord.com/developers/applications), create an application, add a bot, and copy its token. Keep the token private.

### 2. Invite the bot

Use the OAuth2 URL Generator with these scopes:

- `bot`
- `applications.commands`

Grant the bot these permissions:

- View Channels
- Send Messages
- Embed Links
- Read Message History

### 3. Find your server ID

Enable Developer Mode in Discord, right-click your server, and select **Copy Server ID**.

### 4. Configure the project

Copy `.env.example` to `.env`, then add your values:

```env
DISCORD_TOKEN=your_bot_token
DISCORD_GUILD_ID=your_server_id
```

Never commit or share the completed `.env` file.

### 5. Start the bot

On Windows, run `start.bat`. The script creates a virtual environment, installs the required packages, and starts the bot. Use `stop.bat` when you want to stop it.

You can also run it manually:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
python bot.py
```

## Polls and birthdays

Poll data and birthday entries are stored locally in JSON files. They remain available after a restart, and you can inspect or back them up without special tools.

## Privacy and security

- Bot tokens stay in the local `.env` file
- No analytics or telemetry
- No external database
- Poll and birthday data stays on the machine running the bot

Only give the bot the permissions it needs, and replace the token immediately if it is ever exposed.

## Common problems

- If commands do not appear, confirm that `applications.commands` was included when inviting the bot.
- If the bot cannot reply, check its channel permissions.
- If startup fails, confirm that Python is installed and the `.env` values are correct.
- If you changed the server, update `DISCORD_GUILD_ID` and restart the bot.

## Project files

- `bot.py` contains the commands and bot behavior.
- `storage.py` handles local JSON storage.
- `requirements.txt` lists the Python dependencies.
- `.env.example` documents the required configuration.
- `start.bat` and `stop.bat` provide simple Windows controls.
- `stop-bot.ps1` verifies the process before stopping the bot.

## Building on the project

The code is intentionally kept approachable so new developers can learn from it and add their own commands. When contributing, keep changes focused, protect user data, and never include real tokens or server IDs.

## License

This project is available under the [MIT License](LICENSE).

## Author and community

- Author: **KSAGlory**
- Community: [discord.gg/ksahub](https://discord.gg/ksahub)

Copyright © 2026 KSAGlory. All rights reserved.
