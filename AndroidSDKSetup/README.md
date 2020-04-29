# Install Android SDKs

1. Download the Linux zip file:

    ```text
    wget <https://dl.google.com/android/repository/sdk-tools-linux-4333796.zip>

    The downloaded file should be in the folder that the wget command was executed.
    ```

2. From the "/home/pi" directory make a directory called "Android":

    ```t
    sudo mkdir Android
    sudo chmod -R 777 Android
    ```

3. Extract the zip file:

    ```t
    unzip sdk-tools-linux-4333796.zip
    ```

4. Move the "tools" folder to the Android folder:

    ```t
    sudo mv tools Android
    ```

5. Now add sdkmanager PATH to .bashrc (sudo nano ~/.bashrc)

    ```bash
    # Android Paths
    export ANDROID_HOME=/home/pi/Android
    export PATH=$ANDROID_HOME/tools:$ANDROID_HOME/tools/bin:$PATH
    ```

6. At this point it is a good idea to reboot the pi.
7. Make another directory ".android" with a file called "repositories.cfg":

    ```t
    sudo mkdir -p .android
    sudo chmod -R 777 .android
    sudo touch ~/.android/repositories.cfg
    ```

8. Install platform-tools:

    ```t
    sdkmanager platform-tools
    ```

9. Install a base set of build-tools:

    ```t
    sdkmanager "build-tools;26.0.0"
    ```

10. Add this line to .bashrc (sudo nano ~/.bashrc)

    ```bash
    export PATH=$ANDROID_HOME/build-tools/26.0.0:$PATH
    ```

11. Useful reference: <https://linoxide.com/linux-how-to/install-android-sdk-manager-ubuntu/>

12. This should be the completion of the Android sdk installation
