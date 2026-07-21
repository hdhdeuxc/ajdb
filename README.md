from rubka.asynco import Robot, Message, filters
import asyncio

TOKEN = "توکن روبیکا که گرفتی رو اینجا بذار"
bot = Robot(TOKEN)

@bot.on_message(filters.text("سلام"))
async def salam_handler(app, message: Message):
    await message.reply("سلام 🌸")

asyncio.run(bot.run())
