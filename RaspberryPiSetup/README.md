# Prepare Raspberry Pi SD Card and install/update Raspbian

1. Get the appropriate SD Card Image  <https://www.raspberrypi.org/downloads/>
2. Get Raspbian Buster with desktop  <https://www.raspberrypi.org/downloads/raspbian/>
3. Setup should be for United States setup (keyboard, localization, etc ...)
4. Connect to the OT_ENGR WiFi network.
5. Enable SSH and VNC
6. Name the pi ***pitestbench#*** (where # is the number of the bench) and set the password to ***yadayadayada***
7. Update the packages:

    ```t
    sudo apt-get update
    ```

8. Upgrade the packages:

   ```t
   sudo apt-get upgrade
   ```
