# Topic-Wrapper
api wrapper for v3
> Post Requests
```js
const TBL = require("topic-api"); // We import our api
const stats = new TBL("Your BotID", "Your Bot Api token") // Add botID string, And Authorization token from the bot page
    setInterval(() => { 
        stats.postStats("Guilds count" /*, "Shards Count" */) // Post guilds count and shards count
        }, 3e5)
    }) 
```

> Get Requests
```js
    // get bot stats
    stats.getStats((data) => {
        console.log(data)
    })
```
# Webhooks

```js
const TBL= require("topic-api")
const TBL = new tbl("botID", "botAuth", {webPort: 3000, webPath: "/TBLhook", webAuth: "auth to your webhook"});

TBL.webhook.on("votes", (vote) => {
    console.log(vote) // get vote 
})
TBL.webhook.on("ready", console.log) // Owhen the web will start you will recive this message
TBL.webhook.on("destroyed", console.log) // any err that will be generated
```
