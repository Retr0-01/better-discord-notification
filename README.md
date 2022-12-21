# Better Discord Notification 
![GitHub release (latest by date)](https://img.shields.io/github/v/release/Retr0-01/better-discord-notification?style=flat-square)
[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/Retr0-01/better-discord-notification/discord-notification.yml?branch=main&label=test%20workflow&style=flat-square)](https://github.com/Retr0-01/better-discord-notification/actions/workflows/discord-notification.yml)
![GitHub](https://img.shields.io/github/license/Retr0-01/better-discord-notification?style=flat-square)  
A GitHub action for sending an enhanced, fully customizable, Discord notification embed.

## Usage
| Input           | Type   | Description                                                |
| --------------- | ------ | ---------------------------------------------------------- |
| ``webhook-url`` | string | The Discord webhook URL this notification will be send to. |
| ``embed-color`` | int    | The embed's color, in decimal form. MUST be quoted like the example.                        |
| ``footer-icon`` | string | A small icon to put on the footer.                         |

## Example
```yml
steps:
  - name: Send Notification
    uses: Retr0-01/better-discord-notification@main
    with:
      webhook-url: ${{ secrets.CI_DISCORD_WEBHOOK_PUBLIC }} # It is recommended to store your webhooks using actions secrets
      embed-color: '3093151'
      footer-icon: 'https://cdn.discordapp.com/attachments/712252851283296260/961953852897255454/706526933973860412.png'
```

### Results
![image](https://user-images.githubusercontent.com/61121754/162499543-01ecfe49-8d3b-4291-8504-6d07cf8370f5.png)
