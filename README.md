import discord
from discord.ext import commands

# Replace 'YOUR_BOT_TOKEN' with the actual token you copied from the Discord Developer Portal
bot_token = 'MTA3NTQ4MDEyNjc3MjQ5ODUyNQ.G-lRcP.smLpPr9qu4E8JABwZJIyungZ6--7HsKrHC-7mA'

# Prefix for bot commands
bot_prefix = '!'

# Create a new bot instance with a specified command prefix
bot = commands.Bot(command_prefix=bot_prefix)

# Event: Bot is ready and connected to Discord
@bot.event
async def on_ready():
    print(f'Logged in as {bot.user.name}')

# Command: !hello
@bot.command()
async def hello(ctx):
    await ctx.send(f'Hello {ctx.author.mention}!')

# Run the bot with the specified token
bot.run(MTA3NTQ4MDEyNjc3MjQ5ODUyNQ.G-lRcP.smLpPr9qu4E8JABwZJIyungZ6--7HsKrHC-7mA)
