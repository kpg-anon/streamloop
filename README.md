<p align='center'>
    <img src="https://capsule-render.vercel.app/api?type=waving&height=150&color=0:9146ff,100:BD93F9&text=Streamloop&fontColor=9146ff&strokeWidth=1&stroke=000000&fontSize=100&textBg=false&reversal=false&descAlignY=81&descAlign=50&animation=fadeIn"/>
</p>
<p align='center'> 
  <em>Continuously monitors a livestream channel and records when it starts</em>
</p>

## 📦 Requirements 🛠️
- unix
- python
- [streamlink](https://github.com/streamlink/streamlink)
## 📡 Supported sites 🌎
- [x] **twitch**
- [x] **afreecatv**
- [ ] ~~**kick**~~ <small>coming soon™</small>
- [ ] ~~**chzzk**~~ <small>coming soon™</small>
- [ ] ~~**youtube**~~ <small>coming soon™</small>
## 🌐 Installation 🗃
1. Download the script and make it executable:
**posix**
	`wget https://github.com/kpg-anon/streamloop/raw/main/streamloop.sh && chmod +x streamloop.sh`
**python** (*requires argparse)
	`wget https://github.com/kpg-anon/streamloop/raw/main/streamloop.py && chmod +x streamloop.py && pip install argparse`
2. Modify your [output directory](https://github.com/kpg-anon/streamloop/blob/main/streamloop.sh#L8):
	`OUTPUT_BASE_PATH=~/path/to/STREAMS`
3. Set your [streamlink options](https://github.com/kpg-anon/streamloop/blob/main/streamloop.sh#L10):
	```
	STREAMLINK_OPTIONS_TWITCH='--twitch-proxy-playlist=https://eu2.luminous.dev --twitch-proxy-playlist-fallback --twitch-disable-ads'
	STREAMLINK_OPTIONS_AFREECATV='--stream-segment-timeout 90'
	```
## 🧑‍💻 Usage 💻
```
	Usage: ./streamloop.sh -p <platform> -u <username> [-q <quality>] [-r <retry>]
  		-p  Platform (twitch or afreecatv)
		-u  Username on the platform
		-q  Quality of the stream (default: best)
		-r  Retry interval in seconds (default: 180)
```
## 📖 Additional Resources 💡
Currently the script is preconfigured to work with the custom [streamlink-ttvlol](https://github.com/2bc4/streamlink-ttvlol?tab=readme-ov-file#installation) Twitch extractor. You'll want to install that in order to block ads from your Twitch recordings.
## 📝 TODO ✅
- [x] ~~create python version~~
- [ ] add support for kick, chzzk and youtube
