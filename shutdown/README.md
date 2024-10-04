`mbp_shutdown.sh` is a pre-shutdown script for my MBP.

Make sure the script is executable:

```
chmod +x mbp_shutdown.sh
```

`com.user.shutdown.plist` is the launch agent. Must be copied to `/Library/LaunchAgents/` (you'll need administrator priveleges to do this).

To load the launch agent:

```
launchctl load /Library/LaunchAgents/com.user.shutdown.plist
```

If you've already loaded a previous version of the script, unload it first before loading a new one:

```
launchctl unload /Library/LaunchAgents/com.user.shutdown.plist
launchctl load /Library/LaunchAgents/com.user.shutdown.plist
```
