# Commando MongoDBProvider
![Node.js Package](https://img.shields.io/github/workflow/status/johnweland/commando-mongodb/Node.js%20Package?label=Node.js%20Package&logo=github&style=for-the-badge)
[![Downloads](https://img.shields.io/npm/dt/commando-mongodb?style=for-the-badge)](https://www.npmjs.com/package/commando-mongodb)
[![Version](https://img.shields.io/npm/v/commando-mongodb/latest?style=for-the-badge)](https://www.npmjs.com/package/commando-mongodb)

A MongoDB provider for discord.js-commando

## About
> ***UPDATE*** This update provides backward compatibility with older versions of [discord.js][discord.js], these changes should also be getting implemented in to [Dizzy's][Dizzy] work on [commando-provider-mongo][commando-provider-mongo]. When/if that happens I encourage folks to return to using [commando-provider-mongo][commando-provider-mongo] as this was never entended to be a *copy-cat-package* only a fix should the original never see an update.

This is a slight rework of the [commando-provider-mongo][commando-provider-mongo] package by [Dizzy][Dizzy]. This rework is designed to work with [discord.js][discord.js] v12 and later. If you are running an earlier version of [discord.js][discord.js] please use [Dizzy's][Dizzy] [commando-provider-mongo][commando-provider-mongo] package.

[Commando](https://github.com/discordjs/Commando) is the official framework for [discord.js][discord.js], to allow for easy development of discord bot commands and functionality.

## Installation
```bash
npm install --save mongodb commando-mongodb
```

## Usage
```js
const MongoClient = require('mongodb').MongoClient;
const MongoDBProvider = require('commando-provider-mongo');

...

client.setProvider(
	MongoClient.connect('mongodb://localhost:27017').then(client => new MongoDBProvider(client, '<db_name>'))
).catch(console.error);

...
```

## License
MIT © [John Weland](https://github.com/johnweland)



[discord.js]:https://github.com/hydrabolt/discord.js
[commando-provider-mongo]:https://www.npmjs.com/package/commando-provider-mongo
[Dizzy]:https://github.com/ItsDizzy