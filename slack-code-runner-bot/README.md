# JavaScript Slack Bot

A simple bot which allows users to execute short-lived Javascript code snippets directly in Slack.

## Getting Started

1. Create a new app on Slack or have your administrator do it for you
2. Obtain the `Bot User OAuth Access Token` from the Slack webUI (inside the red box)
   and export it 
   
   `export SLACK_BOT_TOKEN=<YOUR_TOKEN_HERE>`
3. Deploy the Binaris function `bn deploy public_slackRunner`
4. Copy the URL printed by `bn deploy` and enter it as the `Request URL` on the "Event Subscriptions" page in the Slack webUI. This will send your function-bot a challenge.
5. Finally, on the same "Event Subscriptions" page scroll slightly down and "Add Workspace Event". There are many options here but if you want your bot to respond in all public channels use `message.channels`
6. You may need to reinstall your slack application to take advantage of the changes

### Running some code

You should now be able to test your function-bot in action by sending a message such as

````
@provemewrong
```
const a = 5;
const b = 10;
return a + b;
```
````

*Expected Response*

`Output`

```
15
```