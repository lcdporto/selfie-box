# Software #

## Scripts ##

### daemon ###

Will install into `/usr/local/bin/selfieBox`

Requirements fully upgraded 'rasbian' installation, firware updated (`rpi-update`) and the `wiringpi` package installed.

More information on the `wiringpi` library can be found on it's   [homepage](https://projects.drogon.net/raspberry-pi/wiringpi/the-gpio-utility/).

### init script ###

Will install into `/etc/init.d/selfieBox`

This script will read read during boot and the daemon will be
started as a system service.

To the automatically run on system boot the service must be
activated.
```
sudo update-rc.d selfieCam defaults
```


If you wish to remove the service from boot:
```
 sudo update-rc.d selfieCam remove
```
