# brcm-backup

## What is this ?

This is a backup of the `/lib/firmware/brcm` folder I had on my RockPro64 while it was running Manjaro.
The Wifi was actually working and since I'm very lazy and don't want to waste my time I decided to make a backup of it before switching to another distro.

## How to use it ?

**I only tested this with the RockPro64 running on Fedora !**

1. Make a backup of your `/lib/firmware/brcm` folder just in case (including the symbolic links !)

    ```sh
    cp -av /lib/firmware/brcm/ $HOME
    ```

2. Delete the content of your `lib/firmware/brcm` folder

   ```sh
   sudo rm -rf /lib/firmware/brcm/*
   ```

3. Copy the content of the `files` folder to your `/lib/firmware/brcm` one

   ```sh
   sudo cp -av files/* /lib/firmware/brcm/
   ```

4. Reboot and the Wifi should be working
