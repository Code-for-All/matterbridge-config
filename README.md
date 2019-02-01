# Code for All's one ring to rule them all

A Matterbridge config file to connect all of our communications.

## Joining

1. Provide the channels that you want to connect
   a. Send a pull request updating the files in this repo
   a. Open an issue specyfing which channels would you like to link. 
      We suggest that on your Slack you open the references of default channels here: #cfall-general, #cfall-introductions, #cfall-readingroom, #cfall-events, #cfall-wins, #cfall-just-starting, #cfall-random, #cfall-members (private for members). 
      We would love also to link your active open channels. Should we link your #general to Code for All's #cfcountry-general?
2. Create a bot app
   a. [Create bot app](https://github.com/42wim/matterbridge/wiki/Slack-bot-setup) in your workspace and send privately the bot token `xoxb-*` to @kaymadejski. Also invite the bot to the channels you created above (ie. `/invite @matterbridgecfall`). Proposed bot name: `Matterbridge-CfAll`. Set bot to be Always Online`.
   b. Invite krzysztof.madejski at `epf.org.pl` to your workspace and related channels. I will then be able to install the bot. You might get the message: `Hi, it's Krzysztof from ePanstwo & Code for All. I'm setting up the Matterbridge bot to connect main slack channels within Code for All network. You can read more about it on https://github.com/42wim/matterbridge and https://github.com/Code-for-All/matterbridge-config.`

## Run it

Run Matterbridge with `sudo docker run -ti --env-file .env -v matterbridge-config/matterbridge.toml:/matterbridge.toml 42wim/matterbridge`.

## Notes
###Creating bot app

Secure: Restrict API Token Usage on https://api.slack.com/apps `OAuth & Permissions` specifying IP <TODO>

