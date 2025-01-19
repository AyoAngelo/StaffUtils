![a](images/staffutils2.png)

# Installation
**Bungeecord/Waterfall**:
- Download the latest BUNGEECOORD version available on this github repository
- Put the downloaded .jar file in folder "YOURBUNGEE/plugins"
- Restart your proxy (Plugins like ServerUtils or Plugman, can create some bugs)
- Setup the plugin with the configuration file (YOURBUNGEE/plugins/staffutils_bungeecord/config.yml)

**Velocity** (Soon available):
- Download the latest VELOCITY version available on this github repository
- Put the downloaded .jar file in folder "YOURVELOCITY/plugins"
- Restart your proxy (Plugins like ServerUtils or Plugman, can create some bugs)
- Setup the plugin with the configuration file (YOURVELOCITY/plugins/staffutils_velocity/config.yml)

**Spigot/Paper/Another** (Soon available):
- Download the latest SPIGOT version available on this github repository
- Put the downloaded .jar file in folder "YOURSPIGOT/plugins"
- Restart your proxy (Plugins like ServerUtils or Plugman, can create some bugs)
- Setup the plugin with the configuration file (YOURSPIGOT/plugins/staffutils_spigot/config.yml)

# Languages
The plugin comes with 2 built in languages, if you want, you can customize or create a new one. To create a new language, duplicate the lang_en.yml file and rename it like that: lang_LANGUAGEID.yml
To enable a language go in the configuration file (SERVER/plugins/staffutils_PLATFORM/config.yml) and set the key "language" to the id of the language you want to enable

**ALL MESSAGES SUPPORT PLACEHOLDERAPI'S PLACEHOLDER**

# Permissions
**Some permissions might be useless, it depends on the configuration choices**
| Permission | Description |
| --- | --- |
| `staffutils.reload` | Allow to reload the plugin's config.yml |
| `staffutils.screenshare.use` | Allow to start and stop a screenshare with /ss |
| `staffutils.screenshare.debug` | Allow to spectate all screenshares with /ss debug |
| `staffutils.screenshare.slogalert` | Allow player to receive slog-during-screenshare alerts |
| `staffutils.freeze.use` | Allow to use /freeze command on players |
| `staffutils.freeze.alerts` | Allow player to receive freeze alerts |
| `staffutils.freeze.exempt` | Gives freeze exempt to player |
| `staffutils.staffchat` | Allow to use staffchat |
| `staffutils.adminchat` | Allow to use adminchat |
| `staffutils.automod.alerts.default` | Allow player to receive automod words alerts |
| `staffutils.automod.alerts.ip` | Allow player to receive automod numeric ip alerts |
| `staffutils.automod.alerts.links` | Allow player to receive automod link alerts |
| `staffutils.automod.alerts.appeal` | Allow player to receive automod appeal alerts |
| `staffutils.automod.bypass` | Gives automod bypass to player |
| `staffutils.staffmsg.use` | Allow to use staffmsg |
| `staffutils.staffmsg.alerts` | Allow player to receive staffmsg alerts |
| `staffutils.report.alerts` | Allow player to receive report alerts |
| `staffutils.stafflist.use` | Allow to use /stafflist |
| `staffutils.stafflist.vanish.use` | Allow to use /stafflistvanish |
| `staffutils.stafflist.vanish.alerts` | Allow player to receive stafflist vanish alerts |
| `staffutils.staffvanish.use` | Allow to use staffvanish |
| `staffutils.staffvanish.alerts` | Allow player to receive staffvanish alerts |
| `staffutils.helpop.alerts` | Allow player to receive helpop alerts |

# Configuration file
A preview of config.yml

Some option are only for bungeecord/velocity
```yaml
# StaffUtils 2.0.0 - by @AyoAngelo on Telegram
# Documentation / Help -> https://github.com/AyoAngelo/StaffUtils/blob/main/README.md

# DO NOT TOUCH
config-version: 2.0.0
# DO NOT TOUCH

# Should the players know you're using StaffUtils?
credits: true

language: IT

# Screenshare, also known as ss
screenshare:
  enabled: true
  enableBanClickTemplates: true
  enableMessageToSuspect: true
  enableDebugRole: true
  enableSlogAlert: true
  freezeSuspect: false
  enableFreezeMessage: false
  screenshareServer: 'yourServer'
  screenshareTeleportCoordinates: "0, 0, 0"

# Freeze
freeze:
  enabled: true
  enableAlerts: true
  enableFrozenNotify: true

# Staffchat, the chat reserved to the staff
staffchat:
  enabled: true
  enableStaffChatSym: true
  staffChatSym: '#' # Required if enableStaffChatSym is set to true

# Adminchat, the chat reserved to the server's admins
adminchat:
  enabled: true
  enableAdminChatSym: true
  adminChatSym: '%' # Required if enableAdminChatSym is set to true

# Automod (beta)
# full guide and explanation of automod can be found in the documentation
automod:
  enabled: false
  enableSmartFinds: true
  enableNoSpaceChecking: true
  enableStaffAlert: true
  enableUserAlert: true
  enableAppeal: true
  censor: true

  blockLinks:
    enableBlockLinks: true
    action: 'MUTE' # Available: MUTE, BAN, WARN, NOTHING
    duration: '10s' # Use common format: 5s, 7m, 8d, 2w, 3mo, 7y, permanent
    reason: 'You sent a prohibited link in chat! (Automod)'
    whitelistedLinks: # in case of false positive use link's whitelist
      - 'minecraft.net'

  blockNumericIps: # To avoid doxing
    enableBlockNumericIps: true
    action: 'BAN' # Available: MUTE, BAN, WARN, NOTHING
    duration: 'permanent' # Use common format: 5s, 7m, 8d, 2w, 3mo, 7y, permanent
    reason: 'You sent a ip in chat! (Automod)'

  blacklistedWords:
    AutomodExample: # the name does not count
      blockedWord: 'AutomodExample' # The detected word(s) (divide the words with a semicolon -> ; <- to put more words)
      action: 'MUTE' # Available: MUTE, BAN, WARN, NOTHING
      duration: '10s' # Use common format: 5s, 7m, 8d, 2w, 3mo, 7y, permanent
      reason: 'You said a bad word! (Automod)'
    AutomodExample2: # the name does not count
      blockedWord: 'Ez; Failed' # The detected word(s) (divide the words with a semicolon -> ; <- to put more words for the same reason)
      action: 'MUTE' # Available: MUTE, BAN, WARN, NOTHING
      duration: '10m' # Use common format: 5s, 7m, 8d, 2w, 3mo, 7y, permanent
      reason: 'You very said a bad word! (Automod)'

  whitelistedWords: # in case of false positive use word's whitelist
    - 'AutomodWhitelistExample'

# Noswear, alerts for prohibited words to the staff
noswear:
  enabled: true
  enableSmartFinds: true
  enableNoSpaceChecking: true
  enableUserAlert: true
  censor: true

  blacklistedWords:
    - 'BlackListExample'

  whitelistedWords: # in case of false positive use word's whitelist
    - 'WhitelistExample'

# StaffMSG, allow staffers to write messages to the players with a specific alert
staffmsg:
  enabled: true
  enableTitleNotify: true
  enableActionBarNotify: true
  enableSound: true
  enableAlerts: true
  sound: 'minecraft:block.note_block.pling'
  soundVolume: 1.0
  soundPitch: 1.0

# Report, enable players to reports another players
report:
  enabled: true
  enableReportsOnOffline: false
  requireReason: true
  commandCooldown: 20 # In seconds

# Stafflist
stafflist:
  enabled: true
  enableCommandPermission: false
  stafflistRanks:
    owner:
      format: ' &8• &4Owner &8» &f$list' # Use $list for the staffer's list
      height: 4
    admin:
      format: ' &8• &cAdmin &8» &f$list' # Use $list for the staffer's list
      height: 3
    mod:
      format: ' &8• &eModerator &8» &f$list' # Use $list for the staffer's list
      height: 2
    helper:
      format: ' &8• &3Helper &8» &f$list' # Use $list for the staffer's list
      height: 1

# Stafflist vanish, allow staffers to hide from stafflist
stafflistvanish:
  enabled: true
  enableAlerts: true

# Staffvanish, allow staffers to disable all staff's commands and alerts
staffvanish:
  enabled: true
  enableAlerts: true

# Helpop, allow players to ask question or send a message to the staffers
helpop:
  enabled: true
  commandCooldown: 20 # In seconds
  enableActionBarNotify: true
  enableSound: false
  sound: 'minecraft:block.note_block.chime'
  soundVolume: 1.0
  soundPitch: 1.0
```
