# How to Login to Wifi From Command Line

```bash
#first - list out available networks
nmcli device wifi list

# login to the chosen network (don't include the <>)
nmcli device wifi connect <network_ssid> password <password>

```
