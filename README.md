# Better Discord Notification 
![GitHub release (latest by date)](https://img.shields.io/github/v/release/Retr0-01/better-discord-notification?style=flat-square)
[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/Retr0-01/better-discord-notification/test-notification.yml?branch=main&label=test%20workflow&style=flat-square)](https://github.com/Retr0-01/better-discord-notification/actions/workflows/discord-notification.yml)
![GitHub](https://img.shields.io/github/license/Retr0-01/better-discord-notification?style=flat-square)  
A GitHub action for sending an enhanced, fully customizable, Discord notification embed.

## Usage
*All options must be quoted. If your `webhook-url` is provided by using secrets, do not quote it.*
| Input             | Type   | Required | Description                                                        | Default |
| ----------------- | ------ | -------- | ------------------------------------------------------------------ | ------- |
| ``webhook-url``   | string | yes      | The Discord webhook URL this notification will be send to.         | -       |
| ``msg-content``   | string | no       | The message that will be included in the Webhook.                  | -       |
| ``embed-color``   | int    | no       | The embed's color, in decimal form.                                | 0       |
| ``footer-icon``   | string | no       | A small icon to put on the footer.                                 | [Image](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png) |
| ``ignore-hidden`` | bool   | no       | Branches that contain the phase `hidden/` in them will be ignored. | true    |

## Example Workflow
```yml
name: Discord Notification

on:
  push:
    branches: [ main ] # Replace main with your branch name.

jobs:
  Notify:
    runs-on: ubuntu-latest
    name: Send Notification
    steps:
      - name: Send Notification
        uses: Retr0-01/better-discord-notification@main
        with:
          webhook-url: ${{ secrets.CI_DISCORD_WEBHOOK }} # It is recommended to store your webhooks using actions secrets
          msg-content: '@everyone'
          embed-color: '3093151'
          footer-icon: 'https://cdn.discordapp.com/attachments/712252851283296260/961953852897255454/706526933973860412.png'
          ignore-hidden: 'false'
```

### Results
![image](https://user-images.githubusercontent.com/61121754/162499543-01ecfe49-8d3b-4291-8504-6d07cf8370f5.png)

