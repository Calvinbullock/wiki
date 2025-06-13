#  Hide apt update Ubuntu pro adds

## hide
- `/etc/apt/apt.conf.d/20apt-esm-hook.conf` - open this file and comment out the lines in the fucntion / if like statments

## or

## move / replace the file
- `sudo mv /etc/apt/apt.conf.d/20apt-esm-hook.conf /etc/apt/apt.conf.d/20apt-esm-hook.conf.bak
- `sudo touch /etc/apt/apt.conf.d/20apt-esm-hook.conf``
