
# cleaning up a Linux system

## apt / debian based

### pkg cleaning
- `sudo apt autoremove` -- helps remove unused dependacnies

### cache cleaning (/var/cache/apt)
- `sudo apt autoclean` -- clears out the apt cache for unused pkgs
    - `sudo apt clean` -- cleans all the cache out (don't use this as often)

### repos clean up
- `/etc/apt/sources.list` - edit the repos in this file
- `/etc/apt/sources.list.d/` - edit the repos in this file
