# Hassbian

https://home-assistant.io/docs/hassbian/installation/


# Keyboard Layout

In `/etc/default/keyboard`

```
XKBLAYOUT="us"
```

# Restarting

sudo systemctl restart home-assistant@homeassistant.service

# pyenv

```
sudo su homeassistant
source /srv/homeassistant/bin/activate
```

# Z-Wave

See
https://home-assistant.io/docs/installation/virtualenv/#installing-python-openzwave-in-a-virtualenv

Get Z-Wave working:

https://community.home-assistant.io/t/openzwave-z-wave-notification-driverfailed-nodeid-255-homeid-0-notificationtype-driverfailed/2553/2

Install z-way, then remove it from auto starting, then reboot.

in configuration.yaml:

```
zwave:
  usb_path: /dev/ttyAMA0
  config_path:
/srv/homeassistant/lib/python3.4/site-packages/libopenzwave-0.3.2-py3.4-linux-armv7l.egg/config
```

## Docker Installation 

http://blog.alexellis.io/getting-started-with-docker-on-raspberry-pi/

```
curl -sSL get.docker.com | sh
sudo systemctl enable docker
sudo systemctl start docker
sudo usermod -aG docker pi
```

docker-compose third party install:

https://github.com/hypriot/arm-compose#installation


## Z-Wave configuration

Use docker-compose image:

https://www.reddit.com/r/homeassistant/comments/522n6x/manually_install_home_assistant_with_openzwave/

Service starts on port ```8080```

# Cast devices

in configuration.yaml:

```
media_player:
  - platform: cast
```


