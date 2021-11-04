# Jak udělat základního discord bota v pythonu
Uděláme si bota v pythonu

# Stavba základního kódu

```py
import discord
from discord.ext import commands

bot = commands.Bot(command_prefix="d!", intents=discord.Intents.all()) # místo "d!" si dej tvůj vlastní prefix (informace o prefxsech níže)
token =  'tvuj token' # o tokenech níže


@bot.event
async def on_ready(): # on ready znamená, že když je bot ready tak to napíše do konzole: 'je ready'
    print("je redy")


@bot.command
async def ping(ctx):
  await ctx.send("pong")
  
bot.run(token)
```
