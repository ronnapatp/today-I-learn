# Discord.js version 13(Latest)

Discord.js [version 13](https://discord.js.org/#/docs/main/13.1.0/general/welcome) have many update from discord.js [version 12](https://discord.js.org/#/docs/main/v12/general/welcome)

### For example [(Embed)](https://discordjs.guide/popular-topics/embeds.html#embed-preview) 

- Version 12 
``` javascript
// at the top of your file
const { MessageEmbed } = require('discord.js');

// inside a command, event listener, etc.
 const exampleEmbed = new MessageEmbed()
	.setColor('#0099ff')
	.setTitle('Some title')
	.setURL('https://discord.js.org/')
	.setAuthor('Some name', 'https://i.imgur.com/AfFp7pu.png', 'https://discord.js.org')
	.setDescription('Some description here')
	.setThumbnail('https://i.imgur.com/AfFp7pu.png')
	.addFields(
		{ name: 'Regular field title', value: 'Some value here' },
		{ name: '\u200B', value: '\u200B' },
		{ name: 'Inline field title', value: 'Some value here', inline: true },
		{ name: 'Inline field title', value: 'Some value here', inline: true },
	)
	.addField('Inline field title', 'Some value here', true)
	.setImage('https://i.imgur.com/AfFp7pu.png')
	.setTimestamp()
	.setFooter('Some footer text here', 'https://i.imgur.com/AfFp7pu.png');

 msg.channel.send(exampleEmbed);
```
- Version 13
``` javascript
// at the top of your file
const { MessageEmbed } = require('discord.js');

// inside a command, event listener, etc.
const exampleEmbed = new MessageEmbed()
	.setColor('#0099ff')
	.setTitle('Some title')
	.setURL('https://discord.js.org/')
	.setAuthor('Some name', 'https://i.imgur.com/AfFp7pu.png', 'https://discord.js.org')
	.setDescription('Some description here')
	.setThumbnail('https://i.imgur.com/AfFp7pu.png')
	.addFields(
		{ name: 'Regular field title', value: 'Some value here' },
		{ name: '\u200B', value: '\u200B' },
		{ name: 'Inline field title', value: 'Some value here', inline: true },
		{ name: 'Inline field title', value: 'Some value here', inline: true },
	)
	.addField('Inline field title', 'Some value here', true)
	.setImage('https://i.imgur.com/AfFp7pu.png')
	.setTimestamp()
	.setFooter('Some footer text here', 'https://i.imgur.com/AfFp7pu.png');

channel.send({ embeds: [exampleEmbed] });
```
- Result

![image](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi.stack.imgur.com%2FGjYXz.png&f=1&nofb=1)


### Version 13 docs
[Click here!](https://discordjs.guide/#before-you-begin)

### Read release from discord.js
[Github discord.js release v13.0.1](https://github.com/discordjs/discord.js/releases/tag/13.1.0)


## About discord.js

**Imagine a bot**

discord.js is a powerful [Node.js](https://nodejs.org/en/)  module that allows you to interact with the Discord [API](https://discord.com/developers/docs/intro)  very easily. It takes a much more object-oriented approach than most other JS Discord libraries, making your bot's code significantly tidier and easier to comprehend.



Usability, consistency, and performance are key focuses of discord.js, and it also has nearly 100% coverage of the Discord API. It receives new Discord features shortly after they arrive in the API.

## Source
- [discord.js.org](https://discord.js.org/#/)
- [discord.js.org/#/docs/](https://discord.js.org/#/docs/main/stable/general/welcome)
- [discordjs.guide](https://discordjs.guide/)


(15/8/2021 6:25 PM)
