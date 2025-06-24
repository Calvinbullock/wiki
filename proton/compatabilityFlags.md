# Steam Compatibility Flags

### opendGL fallback
-  `PROTON_USE_WINED3D=1 %command%` set proton to fall back to openGL translation instead of vulken.
    - good for older games / older GPUs with out vulken
    - *Often needed for intel gpus*

### log
- `PROTON_LOG=1 %command%` set steam to create game log file
    - log locations:
        - native  - `/home/johndoe/steam-221410.log` 
        - snap    - `~/snap/steam/common/` 
        - flatpak - `~/.var/app/com.valvesoftware.Steam/`

