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

#### auth file ####

The username and password need to authenticate into the API are
kept on a separate file (`/etc/selfieBox.auth`) so it can be kept
on the `.gitignore` file.

### init script ###

Will install into `/etc/init.d/selfieBox`

This script will read during boot and the daemon will be
started as a system service.

To the automatically run on system boot the service must be
activated.
```
sudo update-rc.d selfieBox defaults
```


If you wish to remove the service from boot:
```
sudo update-rc.d selfieBox remove
```
