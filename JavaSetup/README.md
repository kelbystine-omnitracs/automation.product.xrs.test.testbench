# Install java 1.8

Unlike vanilla Debian Buster, the raspberry pi supports java jdk 1.8.

1. Install jdk 8 and verify installation:

    ```t
    sudo apt-get update
    sudo apt install openjdk-8-jdk
    java -version
    ```

2. Edit the .bashrc file to set JAVA_HOME and PATH:

    ```t
    sudo nano ~/.bashrc
    ```

3. Add these lines to the end of the file. CTRL-X then respond with 'Y' to write the changes:

    ```bash
    # JAVA_HOME Path
    export JAVA_HOME="/usr/lib/jvm/java-8-openjdk-armhf"
    export PATH=$JAVA_HOME/bin:$PATH
    ```
