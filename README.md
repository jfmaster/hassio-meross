# hassio-meross
=================================

An update to [Spencer Oberstadt's custom component](https://github.com/soberstadt/homeassistant-config/blob/master/custom_components/meross.py) to work with my HA 0.88.1 install (I use HASSIO, but plain old Home Assistant should be fine).

It is built using the awesome [MerossIot Python library](https://github.com/albertogeniola/MerossIot), which is already really well-developed.


Tested only with my MSS110 smart outlets (which I got for dirt cheap on amazon), however the MerossIot page claims to work with all of these device types:
- MSS310 both hw v1 and v2 (Thanks to DanoneKiD)
- MSS310H (Beta, status not updated) (Thanks to virtualdj)
- MSS210 (Thanks to ictes)
- MSS110 (Thanks to soberstadt)
- MSS425E (Thanks to ping-localhost)


# Install
=================================

- **Copy custom_components folder into your config directory**
```
For my HASSIO + SSH setup, my folder path will be just: /config/custom_components
```

- **Add your credentials to configuration.yaml**
```
meross:
  username: me@me.com
  password: !secret meross
```
- **Check for errors and restart Home Assistant. Look at your states page or unused lovelace components page for the added switches.**
