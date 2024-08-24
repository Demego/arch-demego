# ArchTitus Installer Script
[![GitHub Super-Linter](https://github.com/ChrisTitusTech/ArchTitus/workflows/Lint%20Code%20Base/badge.svg)](https://github.com/marketplace/actions/super-linter)

```
pacman -Sy git
git clone https://github.com/ChrisTitusTech/ArchTitus
cd ArchTitus
./archtitus.sh
```
### No Wifi

You can check if the WiFi is blocked by running `rfkill list`.
If it says **Soft blocked: yes**, then run `rfkill unblock wifi`

After unblocking the WiFi, you can connect to it. Go through these 5 steps:

#1: Run `iwctl`

#2: Run `device list`, and find your device name.

#3: Run `station [device name] scan`

#4: Run `station [device name] get-networks`

#5: Find your network, and run `station [device name] connect [network name]`, enter your password and run `exit`. You can test if you have internet connection by running `ping google.com`, and then Press Ctrl and C to stop the ping test.
