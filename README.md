# Basecamp Autobot

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![issues-badge](https://img.shields.io/github/issues/ODDS-TEAM/basecamp-autobot)](https://github.com/ODDS-TEAM/basecamp-autobot/issues)
[![GitHub stars](https://img.shields.io/github/stars/ODDS-TEAM/basecamp-autobot)](https://github.com/ODDS-TEAM/basecamp-autobot/stargazers)
[![hackmd-github-sync-badge](https://hackmd.io/NcHw4jliSfq6ftOgItH7qA/badge)](https://hackmd.io/NcHw4jliSfq6ftOgItH7qA)


🤖 Basecamp Autobot

### Ideas

1. It's easy to add new rules to autobot.
1. The autobot can send .gif file to chat rooms.
1. Modularized and configurable by yml. For example:

   ```yaml
   type: schedule
   tasks:
        - Alarm.inspect
        - Alarm.notify
   options:
        schedule: 0 * * * *
   ```

   From the example above, `Alarm.inspect` and `Alarm.notify` will be automatic executed every begining of each hour.
1. Autobot should recommened the lunch menu.
1. Autobot should have Thai name
1. Autobot should have command when call it such as <command> lunch.
  (Mybe commands is Thainame such as สมจิต กินข้าวโว้ย)
1. Autobot to add a new item in a to-do list: `Autobot, create "Don't forget drink to water" in "sudo proof"`
1. Autobot to book meeting room.
1. Autobot to customize the schedule reminder.
1. Autobot to add people into the new channel, For example: `Autobot, add here in "new channel"`
1. Autobot to count total attendee in an event by count wording: +1
1. Autobot can tag everyone on Campfire like @channel on Slack
1. Autobot to send document template file, For example: `certification of employment`
