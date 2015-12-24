# Software #

## Scripts ##

### daemon ###

Will install into `/usr/local/bin/selfieBox`

Requirements:
* fully upgraded 'rasbian' installation,
* firmware updated (`rpi-update`) and the
* `wiringpi` package installed, More information on the `wiringpi` library can be found on it's   [homepage](https://projects.drogon.net/raspberry-pi/wiringpi/the-gpio-utility/).

#### config file ####

This daemon will read a config file on `/etc/selfieBox`,
values of variables set on that file will replace defaults
hardcoded in the daemon code.

### init script ###

Will install into `/etc/init.d/selfieBox`

This script will read during boot and the daemon will be
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
