# Allowing KDEconnect through firewall

## Step 1: Create the Application Profile
You need to create a profile file in the UFW directory. Run this command to create and edit the file:

```Bash
sudo /etc/ufw/applications.d/kdeconnect
```

## Step 2: Paste the Definition
Copy and paste the following block into that empty file:

```toml
[KDEConnect]
title=KDE Connect
description=KDE Connect enables desktop integration with mobile devices.
ports=1714:1764/udp|1714:1764/tcp
```

## Step 3: Tell UFW to "Allow" the App
Now that the profile exists, tell UFW to refresh its list and allow the app by name:

```bash
sudo ufw app update KDEConnect
sudo ufw allow KDEConnect
```
