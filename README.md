# math-evaluator
### Easy, safe, ultra light

Mostly Made for discord.js but you can use for other's too!

## Usage 
```js
//Discord.js
const eval = require("math-evaluator");
const Discord = require('discord.js');
const bot = new Discord.Client();
const prefix = '-' //you can use any prefix you like :)

bot.on('ready', async () => console.log('Ready'));

bot.on('message', async message => {
    let messageAray = message.content.split(' ');
    let args = messageAray.sl
    ice(1);
    if(message.content.startsWith(`${prefix}eval`)) {
        let toEval = args.join(' ');
        let result = await eval(toEval);
        message.channel.send(result);
    }
})
// Asynchronous function
(async () => {
    let result = await mathexpression('1+1')
        .catch(e => console.log(e));
    console.log(result);
})();

// Synchronous function
(() => {
    let result = mathexpression('1+1')
        .then(r => console.log(r))
        .catch(e => console.log(e));
})();
```
### Facing any problems> let me know! Thanos 2.0#4501
