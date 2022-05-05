<h1 align="center">
    🔮 Discord js Akinator 🔮
</h1>

A Discord.js v13 Module that allows you to Create an Akinator Command for Your Discord Bot within Seconds of Installation.


## Features

- 🌎 <b>100+ Languages Supported!</b> | Lightning fast translation has been made possible by Google Translate and hard-coded mappings!

- ▶️ <b>Buttons!</b> | Don't want to type out responses to questions? This package gives you the option to use discord's buttons to easily click your answer of choice!

- 🎮 <b>Multiple Game Types!</b> | This package will allow you to choose whether Akinator will guess an Animal, Character or Object!

- 🙋 <b>Child Mode!</b> | Want to filter out NSFW questions? You can choose to enable Akinator's Child Mode to keep your games squeaky clean!

- ⚡️ <b>Quick & Easy Setup</b> | This package was built with the intentions of working out-of-the-box. Only one parameter is required at least!

## Install Package

Let's take a look at how you can install this package into your Discord Bot Project.

`npm i djs-akinator --save`

For versions 3.0.0 and Above, you'll also need discord.js v13. This can easily be installed with:

`npm i discord.js@13 --save`

For versions earlier than 3.0.0, you'll need discord.js v12. However it is recommended you update to patch bugs and security vulnerabilities, as well as get the newest features from this package!

`npm i discord.js@12 --save`

## Example Code

```js
const { Client, Intents } = require("discord.js");
const akinator = require("djs-akinator");
const client = new Client({ intents: [Intents.FLAGS.GUILDS, Intents.FLAGS.GUILD_MESSAGES] });

client.on("ready", () => {
    console.log("Bot is Online")
});

const PREFIX = "+";

//Example options

const language = "en"; //The Language of the Game
const childMode = false; //Whether to use Akinator's Child Mode
const gameType = "character"; //The Type of Akinator Game to Play. ("animal", "character" or "object")
const useButtons = true; //Whether to use Discord's Buttons
const embedColor = "#2f3136"; //The Color of the Message Embeds - Discord Embed Color Like SyncMe Discord Bot

client.on("messageCreate", async message => {
    if(message.content.startsWith(`${PREFIX}akinator`)) {
        akinator(message, {
            language: language, //Defaults to "en"
            childMode: childMode, //Defaults to "false"
            gameType: gameType, //Defaults to "character"
            useButtons: useButtons, //Defaults to "false"
            embedColor: embedColor //Defaults to "#2f3136"
        });
    }
});

client.login("Discord Bot Token")
```

## Contact Us

- 👋  [Join Our Discord Server](https://discord.gg/Yn7ctmKmvq)!

## SyncMe Discord Bot
- 👋  [Invite SyncMe](https://discord.com/api/oauth2/authorize?client_id=699548270892023868&scope=bot+applications.commands&permissions=8)