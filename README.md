# ZMiTAC 2

### todo:
- nickname change
- rules
- player streak
- player matches today (count)
- better ranking


### in future:
- goofy bot for fandom dziekana

ZMiTAC 2 is a simple application written in one (two) evenings, used to track pool games in DS. BABILON!!!

![ZMiTAC 2](https://raw.githubusercontent.com/suchencjusz/zmitac2/refs/heads/main/image.png)

# Ussage

### docker compose

```
services:
  web:
    image: suchencjusz/zmitac2:main
    ports:
      - "5000:5000"
    environment:
      - MONGO_URI=mongodb+srv://
      - ADMIN_PASSWORD=dupa1234
    #volumes:
    # - ./custom.css:/app/app/static/styles.css
    restart: unless-stopped

  cloudflared:
    image: cloudflare/cloudflared
    command: tunnel --token ${TOKEN}
    restart: unless-stopped
```

### development

```
git clone https://github.com/suchencjusz/zmitac2
cd zmitac2
pip install -r requirements.txt
python3 -m venv venv
```

Linux
```source ./venv/Scripts/activate```

Windows
```.\venv\Scripts\activate```



