# Basecamp Autobot

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![issues-badge](https://img.shields.io/github/issues/ODDS-TEAM/basecamp-autobot)](https://github.com/ODDS-TEAM/basecamp-autobot/issues)
[![GitHub stars](https://img.shields.io/github/stars/ODDS-TEAM/basecamp-autobot)](https://github.com/ODDS-TEAM/basecamp-autobot/stargazers)
[![hackmd-github-sync-badge](https://hackmd.io/NcHw4jliSfq6ftOgItH7qA/badge)](https://hackmd.io/NcHw4jliSfq6ftOgItH7qA)


🤖 Basecamp Autobot

### Ideas
1. It's easy to add new rules to autobot.
2. The autobot can send .gif file to chat rooms.
3. Modularized and configurable by yml. For example:

   ```
   type: schedule
   tasks:
        - Alarm.inspect
        - Alarm.notify
   options:
        schedule: 0 * * * *
   ```

   From the example above, `Alarm.inspect` and `Alarm.notify` will be automatic executed every begining of each hour.