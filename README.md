# 🧠 no_you_fight_bot.py

> "No *you* fight, bot!" — Me, very drunk, on Twitter.

---

A script born from one of the most gloriously stupid arguments I've ever had on the internet. It does one thing: repeatedly replies to a Twitter user with `@USERNAME No You!` every 5 seconds. That's it. That’s the whole bot. And yes, it was hilarious at the time.

## 📌 What It Does
- Authenticates with Twitter using Twython.
- Spams the target user with `No You!` tweets.
- Continues until manually stopped or Twitter rate-limits you into oblivion.

## ⚙️ Requirements
- Python 3.x
- [`twython`](https://github.com/ryanmcgrath/twython)
- A Twitter developer account
- A sense of humor

```bash
pip install twython
```

## 🔐 Environment Variables
Before running, set the following environment variables:

```bash
export APP_KEY_HERE='your_app_key'
export APP_SECRET_HERE='your_app_secret'
export OAUTH_TOKEN_HERE='your_oauth_token'
export OAUTH_TOKEN_SECRET_HERE='your_oauth_token_secret'
```

## 🧨 Script Logic
```python
from twython import Twython
import time
import os

APP_KEY = os.environ['APP_KEY_HERE']
APP_SECRET = os.environ['APP_SECRET_HERE']
OAUTH_TOKEN = os.environ['OAUTH_TOKEN_HERE']
OAUTH_TOKEN_SECRET = os.environ['OAUTH_TOKEN_SECRET_HERE']
user = USERNAME

while True:
    twitter = Twython(APP_KEY, APP_SECRET, OAUTH_TOKEN, OAUTH_TOKEN_SECRET)
    text_to_tweet = (f"@{user} No You!")
    twitter.update_status(status=text_to_tweet)
    print(f"Trolling {user} until they give up")
    time.sleep(5)
```

## ⚠️ Warnings
- Might get you suspended from Twitter (or X now, I guess).
- Should not be used maliciously. This is archived for the meme.

## 🧠 Why Does This Exist?
Because sometimes the internet isn’t about productivity. Sometimes it’s about chaotic, petty, glorious bot-powered revenge. 

## 📷 Bonus
No actual screenshot here, but imagine a wall of "@USERNAME No You!" tweets spanning a night of drunken keyboard combat. 

## 🧼 Cleanup
If you use this and feel shame later, just rename it to `yes_and.py` and pretend it was an improv bot all along. 😉

