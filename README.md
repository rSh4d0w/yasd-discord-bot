# Yet Another Stable Diffusion Discord Bot

## Installation

This installation is intended for debian or arch flavored linux users. YMMV.

Clone my SD fork of [dalle-flow](https://github.com/AmericanPresidentJimmyCarter/dalle-flow/tree/stable-diffusion) and checkout the right branch with the following commands:

```bash
https://github.com/AmericanPresidentJimmyCarter/dalle-flow/
git checkout stable-diffusion
```

Then follow the instructions in the above [link](https://github.com/AmericanPresidentJimmyCarter/dalle-flow/tree/stable-diffusion) to install. DO NOT use the prebuilt docker image but instead follow the steps under "Run natively".

```bash
python flow_parser.py
jina flow --uses flow.tmp.yml
```

Jina should display lots of pretty pictures to tell you it's working. It may take a bit on first boot to load everything.

At this time, if you haven't already, you will need to put the stable diffusion weights into `stable-diffusion/models/ldm/stable-diffusion-v1/model.ckpt`.

Somewhere else, clone this repository and follow these steps:

```bash
git clone https://github.com/AmericanPresidentJimmyCarter/yasd-discord-bot/
cd yasd-discord-bot
python3 -m virtualenv env
source env/bin/activate
pip install -r requirements.txt
```

Then you can start the bot with:

```bash
python bot.py YOUR_DISCORD_BOT_TOKEN
```

Where YOUR_DISCORD_BOT_TOKEN is your token. Once the bot is connected, you can read about how to use it with `>help`.

OPTIONAL: If you aren't running jina on the same box, you will need change the address to connect to declared as constant `JINA_SERVER_URL` in `imagetool.py`.

## Something is broken

Open an issue here.

## Closing remarks

Be cool, stay in school.

## License

[MIT](https://choosealicense.com/licenses/mit/)