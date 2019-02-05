# Code for All's one ring to rule them all

A [Matterbridge](https://github.com/42wim/matterbridge/) config file to connect all of our communications.

## Shared channels

General ones:
- `#introductions` - Introduce yourself to the community! Where are you based, what do you work on, why do you expect from partnership in Code for All? 
- `#general` - Post here if no other channel is applicable. Post job offers.
- `#random` and others similar (ie. rename #eat-for-all to #random-eat-for-all)
- `#fundraising` - Sharing possibilities for fundraising for the network and cross-partner cooperation. 
- `#readingroom` - Aggregated news from all organizations via RSS bot
- `#wins` – Sharing our achievements throughout the year (if possible link related post). Posts will be used for external communication, yearly reports, donors 
- `#just-starting` – We share information about our new projects at their earliest stage to enable cooperation on them.
- `#events` - Purpose: Sharing events we are organizing or planning to attend. If you want to start start discussion about common session's proposals or other event-related talk start a subchannel (ie. #events-ogp-summit) and invite interested people there.
- `#members` [private] – [Official members](https://codeforall.org/members) of the Code for All network

Topical:
- `#sensors` - Hardware for social change

Meta to our work:
- `#fellows` – A place to complain on government beaurocracy ;) 

Geographical:
- `#region-[region]` - ie. #region-europe for Europe related talk (altough in that very specific case we have #code-for-europe)
- `#code-for-[country]` - ie. #code-for-mexico. They might be linked to organization's own #general channel. There are also groups such as @codeforafrica.  Purpose: Connect with people on the ground in Mexico. Check our work at [link to website].


## Adding new organizations and channels

1. Provide the channels that you want to connect
      We suggest that on your Slack you open the references of default channels here: `#cfall-general`, `#cfall-introductions`, `#cfall-readingroom`, `#cfall-events`, `#cfall-fundraising`, `#cfall-wins`, `#cfall-just-starting`, `#cfall-random`, `#cfall-members` (private for members). 
      
      We would love also to link your active open channels. Should we link your `#general` to Code for All's `#cfcountry-general`?
      
    - Send a pull request updating the files in this repo (`matterbridge.toml` and `template.env`)
    - **OR** [Open an issue](https://github.com/Code-for-All/matterbridge-config/issues/new/choose) specyfing which channels would you like to link. 
       
2. Create a bot app

    - [Create bot app](https://github.com/42wim/matterbridge/wiki/Slack-bot-setup) in your workspace and send privately the bot token `xoxb-*` to @kaymadejski. Also invite the bot to the channels you created above (ie. `/invite @matterbridgecfall`). Proposed bot name: `Matterbridge-CfAll`. Set bot to be Always Online`.
    - **OR** Invite krzysztof.madejski at `epf.org.pl` to your workspace and related channels. I will then be able to install the bot. You might get the message: `Hi, it's Krzysztof from ePanstwo & Code for All. I'm setting up the Matterbridge bot to connect main slack channels within Code for All network. You can read more about it on https://github.com/42wim/matterbridge and https://github.com/Code-for-All/matterbridge-config.`

## How to run Matterbridge

We only need one instance of Matterbridge running that will talk to all organizations' bots. Code for All staff will maintain it.

FYI: Matterbridge can be run with above definitions with `sudo docker run -ti --env-file .env -v matterbridge-config/matterbridge.toml:/matterbridge.toml 42wim/matterbridge`.

## Notes
### Creating bot app

Secure: Restrict bot's API Token Usage on https://api.slack.com/apps `OAuth & Permissions` specifying IP <TODO when deployed in production>

