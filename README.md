Minecraft Server Watcher

A lightweight Discord bot that monitors a Minecraft Java Edition server. It provides real-time notifications in Discord when players log in or out and includes a status command for quick server checks.
✨ Features

    Live Player Tracking: Sends a message to a designated Discord channel when someone joins (✅) or leaves (❌) the server.

    Status Command: Use !status to see the current player count, server version, latency, and a list of online players in a clean Discord Embed.

    Railway Ready: Pre-configured for easy deployment on Railway using Nixpacks.

    Dual-Config Support: Works via environment variables (production) or a config.json file (local development).

🚀 Deployment (Railway)

    Fork/Upload this repository to your GitHub.

    Create a New Project on Railway and connect your repository.

    Add Environment Variables: In the Railway dashboard, go to Variables and add the following:

        DISCORD_TOKEN: Your Discord Bot Token from the Developer Portal.

        CHANNEL_ID: The ID of the Discord channel where notifications should be sent.

        MINECRAFT_SERVER: The IP address of your Minecraft server (e.g., play.hypixel.net).

        CHECK_INTERVAL: How often to check the server in seconds (default is 30).

💻 Local Setup

    Install Dependencies:
    Bash

    pip install -r requirements.txt

    Configure: Create a config.json file in the root directory:
    JSON

    {
      "discord_token": "YOUR_TOKEN_HERE",
      "channel_id": 1234567890,
      "minecraft_server": "your.server.ip",
      "check_interval": 30
    }

    Run:
    Bash

    python main.py

🛠 Tech Stack

    Language: Python 3.11 

    Library: discord.py 

    API: mcstatus for querying Java servers 

    Hosting: Configured for Railway via railway.json and Procfile 

📝 Commands

    !status: Displays an embed with server latency, version, and the current player list.
