# StaffUtils ![staffutils](images/staffutils.png)
Staffutils official repository, the plugin will be open-source soon

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

