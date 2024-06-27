#### This is a Telegram Bot written in Python for Downloading Videos From Terabox.
----
#### <b>Fill this Values in [config.env](config.env)</b>
- `BOT_TOKEN`: The Telegram Bot Token that you got from [@BotFather](https://t.me/BotFather). `Str`
- `TELEGRAM_API`: This is to authenticate your Telegram account for downloading Telegram files. You can get this from <https://my.telegram.org>. `Int`
- `TELEGRAM_HASH`: This is to authenticate your Telegram account for downloading Telegram files. You can get this from <https://my.telegram.org>. `Str`
- `FSUB_ID`: The Force Subscribe Channel, users will not be able to use your bot without joining the Channel. (Enter the Channel/Group ID starting with -100). `Int`
- `DUMP_CHAT_ID`: The Dump Channel, all leeched videos will be Forwared Here. (Enter the Channel/Group ID starting with -100). `Int`
  
---
### For farther assistance visit my support group: [**@HxBots**](https://telegram.me/HxBots).
---

## Deployment

### Render
#### Step 1: 
[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy?repo=https://github.com/oVo-HxBots/Terabox-Downloader-Bot)

#### Step 2: Register at [Uptime-Robot](https://dashboard.uptimerobot.com/)

#### Step 3: Add new monitor. Use Link from render deployment for monitor.

 ----
 
### VPS

#### Prerequisites

#### 1. Installing requirements

- Clone this repo:

```
git clone https://github.com/oVo-HxBots/Terabox-Downloader-Bot/ && cd Terabox-Downloader-Bot
```

- For Debian based distros

```
sudo apt install python3 python3-pip
```

Install Docker by following the [Official docker docs](https://docs.docker.com/engine/install/#server).
Or you can use the convenience script: `curl -fsSL https://get.docker.com |  bash`


- For Arch and it's derivatives:

```
sudo pacman -S docker python
```

------

#### 2. Build And Run the Docker Image

Make sure you still mount the app folder and installed the docker from official documentation.

- There are two methods to build and run the docker:
  1. Using official docker commands.
  2. Using docker-compose.

------

#### Build And Run The Docker Image Using Official Docker Commands

- Start Docker daemon (SKIP if already running, mostly you don't need to do this):

```
sudo dockerd
```

- Build Docker image:

```
sudo docker build . -t terabox
```

- Run the image:

```
sudo docker run -p 80:80 -p 8080:8080 terabox
```

- To stop the running image:

```
sudo docker ps
```

```
sudo docker stop id
```

----

#### Build And Run The Docker Image Using docker-compose

**NOTE**: If you want to use ports other than 80 and 8080 change it in [docker-compose.yml](docker-compose.yml).

- Install docker compose

```
sudo apt install docker-compose
```

- Build and run Docker image:

```
sudo docker-compose up --build
```

- To stop the running image:

```
sudo docker-compose stop
```

- To run the image:

```
sudo docker-compose start
```

- To get latest log from already running image (after mounting the folder):

```
sudo docker-compose up
```

---
