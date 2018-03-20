# Prerequisites
Download Hypriot tool "flash", available here : https://github.com/hypriot/flash

# Purpose
Each RPI has his own config file. Flash allow us to prepare RPI automatically, with pre-installed software and config specified in configs files.

## Additionnal packages added
Two additional softwares are added :
- ntp
- python3-blinkt (allow us to manage Pimoroni LED pinned on each RPI)

## Credentials
Default Hypriot credentials used :
- Login : pirate
- Password : hypriot

# Use case
Here's the command :
```
flash \
--hostname node-1 \
--bootconf config.txt \
--userdata ./rpi-config.yml \
https://github.com/hypriot/image-builder-rpi/releases/download/v1.5.1/hypriotos-rpi-v1.5.1.img.zip
```

Don't forget to change the hostname.
The full list is available here : https://blog.hypriot.com/downloads/

# Go further
You can also use local img with the script :
```
flash \
--hostname node-1 \
--bootconf config.txt \
--userdata ./node1-user-data.yml \
hypriotos-rpi-v1.5.1.img.zip
```