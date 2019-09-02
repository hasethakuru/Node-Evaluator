# Node Evaluator
### Node Evaluator is a Easy, safe, ultra light Mathematical Calculator For Javascript

Mostly Made for discord.js but you can use for other libraries too!

## Installation
```js
npm i node-evaluator
```

## Usage 
```js
//Discord.js
const eval = require("node-evaluator");
const Discord = require('discord.js');
const bot = new Discord.Client();
const prefix = '-' //you can use any prefix you like :)
 
bot.on('ready', async () => console.log('Ready'));
 
bot.on('message', async message => {
    let messageArray = message.content.split(' ');
    let args = messageArray.slice(1);
    if(message.content.startsWith(`${prefix}evaluate`)) {
        let toEval = args.join(' ');
        let result = await eval(toEval);
        message.channel.send(result);
    }
});
// Asynchronous function
(async () => {
    let result = await eval('1+1')
        .catch(e => console.log(e));
    console.log(result);
})();

// Synchronous function
(() => {
    let result = eval('1+1')
        .then(r => console.log(r))
        .catch(e => console.log(e));
})();
```
### Facing any problems? let me know! Thanos 2.0#4501

