# README #

BotMock - Test Botkit and Slack responses

### Setup ###

1. Run `npm install`
2. Run `npm test`

### How To Use ###

You can include `botMock.js` in your own Botkit project to mock Botkit responses. 

```
var bot;
if(env !== 'test'){
    bot = require('../app/bots/bot');
}
else{
    var botMock =  require('../test/mock/botMock');
    bot = new botMock.controller('userSlackId', 'userName').bot;
}
```

Just inject `botMock.js` during tests instead of your normal `bot` declaration. `test/controllerSpec` and `test/apiSpec` include examples for testing
Botkit controller responses and api responses, respectively. 