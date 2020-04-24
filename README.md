# GiveawayBot
A complete code for a Discord bot to do contests. Easy to modify and free ! Also available in french.

This code is open source, you can modify it in your own way. If you want to, consider leaving the link to this Github project in a place on the bot to show that you respect the work of others.

Presentation:

This template is here to help you build a bot that will make Giveaways.
This code is complete and has several functions such as :

- The bot saves the giveaways so they won't be deleted if the bot needs to restart.
- The bot can change language.
- The bot can be configured (lounge logs, special role to manage launch a giveaway if the member does not have permission to manage messages...)

And lots of other features to discover !

Configuration :

First of all you will need Node, you can download it by just clicking [here](https://nodejs.org/en/download/). The most recent version is recommended.

First of all, let's indicate our access path, in the command prompt :

```
cd (the access link of your bot's folder, example var/www/mybot)
```

We are going to use several modules, to install them do this in your command prompt :

```
npm i
```

All the module names are in "package.json" and "package-lock.json" all the files are useful don't forget to delete them.
Then we'll fill in everything the bot will need to ensure proper operation.
Open the file "bot.js" which is located in the "config" folder.
Fill it out as below :

```js
module.exports = {

    token: "",

    idbot: "",

    prefix: "",

    basiclang: "",

    embeds: {
        color: "",
        footers: ""
    },

    start: {
        loading: "",
        activity: "",
    },

    events: {
        addcolor: "",
        remcolor: ""
    },

    reaction: "",

    grole: "",

    auth: {
        support: "",
        dperms: ""
    },
};
```

Don't panic everything is indicated in the file for what you need to fill out.
However, I remind you of all the functions below :

- `token`, the token of your bot.
- `idbot`, the ID of your robot.
- `prefix`, the prefix of your robot.
- `basiclang`, the basic language of the bot, "fr" for French and "en" for English.
- `color`, embed color (in English).
- `footers`, embed footer.
- `loading`, loading status.
- `activity`, bot status.
- `addcolor`, the color of the event add (in English).
- `remcolor`, the color of the event remove (in English).
- `reaction`, reaction to the giveaways if you in the console you see 'unknown emoji' that's what this emoji is not recognized by Discord.
- `grole`, if the member doesn't have permission to handle messages he can still use the giveaways commands if he has the role configured right here.
- `support`, the link of your Discord server.
- `dperms`, the permissions that the bot asks on we want to add it on a Discord server (8 = moderator).

Start the bot :

```
#With Node
node index.js

#With pm2
pm2 restart index.js
```

Note for pm2 : 

```
pm2 start = start bot
pm2 stop = stop bot
pm2 restart = restart bot
```

With Node you just have to redo (node index.js).

If in the console you see `Ready on [...] servers, for a total of [...] users.` The bot is ready !
If you see an error in the console, don't hesitate to fix it or to let me know.

Storage part :

Remember not to delete "json.sqlite" as it contains all current / cancelled / modified giveaways.

Thank you for using this code !
