winston-slack

Winston Transport for Slack chat integration

`$ npm install winston-slack`

Also requires install of winston

`$ npm install winston`


Basic transport that works just like all other winston transports. Sends logged messages to a specified slack chat channel

additonal options:

`webhookUri:` a Slack incoming webhook uri (see. https://api.slack.com/)

`username:` name displayed in the chat channel. default "winston-slack"

<code>


    var winston = require('winston');
    var something = require('winston-slack').Slack;

    winston.add(something, {
        webhookUri: "https://hooks.slack.com/services/T621Y9D62/B65DNT20H/HHHHHHHHHHHHHHHHHHHHH",
        channel: "#test-channel",
        username: "ErrorBot",
        level: 'error',
        handleExceptions : true
    });
</code>
