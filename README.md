
hassio-meross
============

An update to [Spencer Oberstadt's custom component](https://github.com/soberstadt/homeassistant-config/blob/master/custom_components/meross.py) to work with my HA 0.88.1 install (I use HASSIO, but plain old Home Assistant should be fine).

It is built using the [MerossIot Python library](https://github.com/albertogeniola/MerossIot), which uses the Meross API and is extremely fast. Much, much faster than using IFTT and probably still faster than going through Google Assistant middleware.

Devices
============

Tested only with my MSS110 smart outlets (which I got for dirt cheap on amazon), however the MerossIot page claims to work with these devices:
- MSS310 both hw v1 and v2 (Thanks to DanoneKiD)
- MSS310H (Beta, status not updated) (Thanks to virtualdj)
- MSS210 (Thanks to ictes)
- MSS110 (Thanks to soberstadt)
- MSS425E (Thanks to ping-localhost)


Install
============

- **Copy custom_components folder into your config directory**
```
For my HASSIO + SSH setup, just copy custom_components into /config.
```

- **Add your credentials to configuration.yaml**
```
meross:
  username: me@me.com
  password: !secret meross

# I added these lines to prevent some frequent log status messages I noticed
logger:
  logs:
    meross_powerplug: warning
```
- **Check for errors and restart Home Assistant. Look at your states page or unused lovelace components page for the added switches.**



Contributing / Getting Help
============

Check out the big community forums post which led to this repo. [Here](https://community.home-assistant.io/t/are-meross-switches-compatible-with-any-existing-components/51548).
