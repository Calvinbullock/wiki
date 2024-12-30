# Setting up a new swapfile on Linux

# Steps to set up the swapfile
## Create the swapfile
- `sudo dd if=/dev/zero of=/swapfile bs=1M count=1024` -- create a 1MB swapfile at root
- `sudo chmod 600 /swapfile` -- set the correct permissions for the swapfile
- `sudo mkswap /swapfile`   -- sets /swapfile to actually be a swapfile

## Enable the swap file
- `sudo swapon /swapfile`   -- turn on swap (should get no output if works)
- `swapon --show`            -- double check swapfile is setup -- if desired

## Set up the system config
- `sudo vim /etc/fstab`
- `/swapfile      none        swap        defaults        0 0` -- this is the new line that you need to added to fstab
