# Install appium

    ```t
    sudo npm install -g appium --unsafe-perm=true --allow-root
    ```

## Install appium-doctor

    ```t
    sudo npm install -g appium-doctor
    ```

Run appium-doctor to make sure that all the critical dependencies are installed (ignore optional dependencies):

    ```t
    appium-doctor
    ```

**Do not try to install the optional dependencies. Just don't.**

## Install adb

    ```t
    sudo apt-get install -y adb
    ```

Connect Android device and run:

    ```t
    adb devices
    ```

Unauthorized means that you need to acknowledge a prompt on your Android device.
