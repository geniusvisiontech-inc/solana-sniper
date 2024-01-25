# Guide on how to run my project without errors!

## Chapter 1: Install the requirements.
1. Install `Python`. The version for python does not matter as long as it is above **3.0**.
2. Run the command `pip install -r requirements.txt` (Note: you machine might have `python3` and `pip3`).
3. If you get errors while installing, please copy and paste the error in chatgpt. **DO NOT Text ME THE ERROR**. Github is a developers community and you must know the basics already.

## Chapter 2: Config file.
### Section 1: Telegram.
**Note:** Use a temporary number for telegram account as use of telethon is subject to ban.
1. Go to [Telegram API development tools](https://my.telegram.org/auth?to=apps).
2. Enter your number, you will receive the code in your telegram application. Enter code and press next.
3. Fill out the form as follows:
      - App Title: Solana Sniper
      - Short Name: SolBot
      - URL: https://my.telegram.org/
      - Platform: Desktop
4. You will receive `api_id` and `api_hash` which you should replace in config.ini file.
5. **Session name** can be anything. First time, when you run the bot, it will ask for your number and the code. At this point `telethon library` will create your telegram session.
6. **Sender Username**, it is the username of channels from where you will receive. Note that the sender in the channel is most likely having the same username as channel username. An example is given below:
![Example1](https://i.ibb.co/Cvqtbhx/Screenshot-2024-01-02-233151.png)

## Section 2: Investment
-  Config.ini already has description due to which I wont write about it here.

## Section 3: DISCORD Webhook URls
- Skipping it will end your bot and give error. So best is to create a dummy webhook in a server and add it to both webhook url and error in config.ini.
1. Create a discord server, goto channel settings, goto integrations and create a webhook. Copy the url and add it to config file.

## Section 4: Wallet Key
- Every wallet has different settings. With intention of testing this bot, you must already have this information.
- But when you get the key, it may look something like this `asuhduiahsw812y98dajsdui172yashduiahsuidh11sjhdahduiashduh1892hdhsuahdh199d89hashANDSO1ON`

## Section 4: Birdeye
**Skip**

## Section 5: INFURA URL
1. Goto alchemy and create your endpoint for solana. Copy the https url and add it to config.ini

## Finally
1. You can create a test channel using main telegram account, then join it with the one that is suppose to be in the solana sniper bot, and then add the username to config.ini.
      - **Note**: some users faced issues e.g. when they send a message in the channel from the telegram account in bot, it does not show up. But if the message is sent by someone else in the channel, it does work.
      - **Detailed Note Example:** my main tg is kokiez4000, I created a second tg with the username kokiezTest and used a temporary number. I setup api settings for kokiezTest, then created a channel using kokiez4000             and added kokiezTest to the channel. When I send message in channel from kokiezTest, it will not show up in bot but if I send message from kokiez4000 in channel, it will work...
2. Run `python main.py`.
3. It will display **Message Received** if telethon is working and CA will show up if the **senderusernames are correct**.

## Happy Trading 🎉
