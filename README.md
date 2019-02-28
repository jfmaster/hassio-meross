# hassio-meross

An update to [Spencer Oberstadt's custom component](https://github.com/soberstadt/homeassistant-config/blob/master/custom_components/meross.py) to work with my HA 0.88.1 install (I use HASSIO, but plain old Home Assistant should be fine).

I only tested with my mss110 smart outlets, which I got for dirt cheap on amazon.

**Does NOT require MQTT.** I tried MQTT and had partial success, but I could only see them in HA. The command topic wouldn't work and I couldn't power my switches. This was my second try and worked perfectly for my needs.

Just copy the custom_components folder into your config directory and restart.
