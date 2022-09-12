# Open-Bot-EN
Welcome to the OpenSource Project "Open-Bot", this is the version in english!
This Project is about discord Bots in Python, this Instruction will help you, when you set up your own Discord-Bots, from the begin, until the hosting.
The project will become a lot of updates, which are already being planned!

### Installation of the software
At first you need to download Python(https://www.python.org/downloads/) and install it with die "PIP" Plugin.
Now you need to download an IDE to edit the code, i recommend you Visiual Studio Code(https://code.visualstudio.com/download), then you need to install DiscordPY:
```
Linux/macOS
python3 -m pip install -U discord.py[voice]

Windows
py -3 -m pip install -U discord.py[voice]
```

### Creating the bot
At(https://discord.com/developers/applications) you need to create 2 applications, then go in these applications and create an bot.
Then you go in the category bot an turn the first 2 options on and the last 3 off.
Now you need to to go to OAuth2 and select "bot" and "applications.commands", then set the authorization to admin, now you need to invite your 2 bots to 
your server. Now you need to go to the option "bot" and Reset the token. Everbody who have the token, can do everything with your bot, but you can reset 
the token

### Connect the script to Discord
You have 1 token from your main bot and 1 token from your Server-Stats bot. Now 
you need to replace "Your Token" with the token from your bot. So the token from the main-Bot in the main script and the token from the Server-Stats Bot in 
the server-stats script.
