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

### The on_message(message) function
At the event:
```
@client.event
async def on_message(message):
    if message.author == client.user:
        return
```
is the function, that he bot can answer to an message:
```
    if message.content.startswith('hello'):
        await message.channel.send('Hello!')
```
With this function the bot caan do a lot of things, like the voicechannel or the suppport function.

### Set the bot status
```
activity = discord.Game(name="Activity", type=1)
```
You can replace the "activity" with everything what you want

### Set up the welcome and autoroles function
```
autoroles = {
    "ID of your Server": {'memberoles': ["Memberroles"],  }
```
You need to delete the "ID of your Server" with the quotation marks and replace it with the ID of your server, then delete "Memberroles" with the quotation marks and 
replace it with the standard memberrole id´s, now you need to delete "ID from your Welcome channel" with the quotation marks and replace it with the ID of the welcome 
channel.
You can replace the 
```
"Hi {member.mention} willkommen auf meinem Server!"
```
with your own welcome message, when you want that the bot says the name of new member,
you need to have the"{member.mention}.

### Set up the support function
```
channel = await guild.create_text_channel(str(message.author))
         await channel.set_permissions(message.author,send_messages=True,read_message_history=True,read_messages=True)
         await channel.set_permissions(discord.utils.get(message.author.guild.roles, id = ("Member") ),send_messages=False,read_messages =                        False,read_message_history=False)
         await channel.set_permissions(discord.utils.get(message.author.guild.roles, id = ("Staff") ),send_messages=True,read_messages =                          True,read_message_history=True)
```
Here you can see "Member" and "Staff", you need to set the permissions for every role, so not everybody can see that this channel exist, you can 
delete "Member" and the quotation marks and replace it with the ID of 1 memberroles, when you have e.g 5 Memberroles, you need to copy the memberline
and put in the right memberrole-id for all the 5 memberroles, you need to do the same with th e roles for "Staff"

### Hosting
