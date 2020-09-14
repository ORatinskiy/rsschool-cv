# Oleh Ratinskiy
### Contact Info
* Number: +380 68 523-25-05
* E-mail: 234854@gmail.com
* Telegram: @oratinskiy

### Summary
My main goal is to become a successful developer. I'm very interested in studying something new that will help me in future. I understand that I always have to improve skills to be up to date. In addition, I hate wasting my precious time.

### Skills
* HTML Basics
* CSS Basics
* JS Basics
* Python Basics

### Code example
##### Python bot, which converts text into speech
```python
from gtts import gTTS
import config
import os
import telebot
bot = telebot.TeleBot(config.token)
name = ''
 
 
@bot.message_handler(commands=['start'])
def start_message(message):
    bot.send_message(message.chat.id, 'Привіт, введи своє ім\'я')
 
 
@bot.message_handler(func=lambda m: True)
def reg_name(message):
    global name
    name = message.text
    myText = "Привіт "
    myText += name
    language = 'uk'
    output = gTTS(text=myText, lang=language, slow=False)
    output.save("output.ogg")
    voice = open('output.ogg', 'rb')
    bot.send_voice(message.chat.id, voice)
bot.polling(none_stop=True)
```

### English level
B2+