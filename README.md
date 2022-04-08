# Better Discord Notification
A GitHub actions for sending a better Discord notification embed, which can also be customized.

## Usage
### Inputs
``webhook-url`` - The Discord webhook URL this notification will be send to.  
``embed-color`` - The embed's color.  
``footer-icon`` - A small icon to put on the footer. Required in order to show the commit message count.  

### Example
```yml
steps:
  - name: Send Notification
    uses: Retr0-01/better-discord-notification@main
    with:
      webhook-url: ${{ secrets.CI_DISCORD_WEBHOOK_PUBLIC }}
      embed-color: '3093151'
      footer-icon: 'https://cdn.discordapp.com/attachments/712252851283296260/961953852897255454/706526933973860412.png'
```