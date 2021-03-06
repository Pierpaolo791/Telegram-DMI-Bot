# Telegram-DMI-Bot

**Telegram-DMI-Bot** is the platform that powers **@DMI_bot**, a Telegram bot aided at helping students find informations about professors, classes' schedules, administration's office hours and more.

### Using the live version
The bot is live on Telegram with the username [@DMI_Bot](https://telegram.me/DMI_Bot).
Send **'/start'** to start it, **'/help'** to see a list of commands.

Please note that the commands and their answers are in Italian.

--- 

### Setting up a local istance
If you want to test the bot by creating your personal istance, follow this steps:
* **Clone this repository** or download it as zip.
* **Copy config/token.conf.dist into "token.conf" and write your telegram bot token here.** (If you don't have a token, message Telegram's [@BotFather](http://telegram.me/Botfather) to create a bot and get a token for it)
* **Send a message to your bot** on Telegram, even '/start' will do. If you don't, you could get an error.
* If your system supports bash shell scripting, **launch "restarter.sh"**. Alternatively, you can launch "main.py" with your Python interpreter, even if doing so will not restart the bot in the event of a crash.

### System requirements

- Python 2
- python-pip
- python-bs4
- python-beautifulsoup
- language-pack-it

#### To install with *pip*

- python-telegram-bot
- pydrive
- requests

### Special functions

#### - /news /spamnews

You can enable these commands setting **disable_chatid_logs = 0**

These functions allow to send to all users that used at least once the bot and stored in logs/chatid.txt a message.
**/news** with this command you write the message (example: /news "This is a news!").
With **/spamnews** the bot will send to all users the message.

Notes: only some users are allowed to use these commands indeed there is an if condition that check the chatid of the user that can use them

#### - /stats
You can enable these commands setting **disable_db = 0** and copy **data/DMI_DB.db.dist** into **data/DMI_DB.db**

This command shows the statistics of the times where the commands are used in the last 30 days.

#### - /drive /request /adddb
You can enable these commands setting **disable_drive = 0**, configure the GoogleDrive credentials and copy **data/DMI_DB.db.dist** into **data/DMI_DB.db**.

**/drive**: command to get the GoogleDrive files
**/request** allows the user to send the subscribe request to get the access for /drive
**/adddb** allows some special users to give the access to /drive to another user

##### **Configure Drive**
- open a project on the Google Console Developer
- enable Drive API
- download the drive_credentials.json and put it on config/
- copy **config/settings.yaml.dist** into **config/settings.yaml**, then configure it


### License
This open-source software is published under the GNU General Public License (GNU GPL) version 3. Please refer to the "LICENSE" file of this project for the full text.

### Credits
This project is made possible thanks to the contributions of [Stefano Borzì](https://github.com/Helias), [Adriano Ferraguto](https://github.com/adrianoferraguto),[Vincenzo Filetti](https://github.com/veeenz), [Simone Di Mauro](https://github.com/simone989), [Alessandro Maggio](https://github.com/Tkd-alex), [Alessio Piazza](https://github.com/Squalex95)
