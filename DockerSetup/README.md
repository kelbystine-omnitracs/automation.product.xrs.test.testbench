# Docker Setup

*Taken From <https://pimylifeup.com/raspberry-pi-docker/>*

1. Our first task is to update all our existing packages before we proceed to install Docker.
    We can upgrade all existing packages by running the following two commands on the Raspberry Pi.

    ```t
    sudo apt update
    sudo apt upgrade
    ```

2. With our Raspberry Pi entirely up to date, we can now go ahead and install Docker to the Raspberry Pi.
    Luckily for us, Docker has made this process incredibly quick and straightforward by providing a bash script that installs everything for you.
    You can download and run the official Docker setup script by running the following command.

    ```t
    curl -sSL https://get.docker.com | sh
    ```

    ```text
    This command will pipe the script directly into the command line. Typically it would be best if you didn’t do this; however, Docker is a trusted source. If you are unsure about running this directly without first inspecting it, you can go directly to get.docker.com to view the script.
    This script can take some time to complete as it automatically detects and installs everything it needs to run Docker on the Raspberry Pi.
    ```

## Setting up the Pi user for Docker

1. Once Docker has finished installing to the Pi, there are a couple more things we need to do.
    For another user to be able to interact with Docker, it needs to be added to the docker group.
    So our next step is to add our pi user to the docker group by using the command below.

    ```t
    sudo usermod -aG docker pi
    ```

    ```text
    If we don’t add our pi user to the group, we won’t be able to interact with Docker without running as the root user.
    If you want to learn more about permissions and groups in Linux, check out our file permissions in Linux guide.
    ```

2. Since we made some changes to our pi user, we will now need to log out and log back in for it to take effect.
    You can log out by running the following command in the terminal.

    ```t
    logout
    ```

3. Once you have logged back in, you can verify that the docker group has been successfully added to your user by running the following command.

    ```t
    groups
    ```

    ```text
    This command will list out all the groups that the current user is a part of. If everything worked as it should, the group docker should be listed here.
    ```

## Testing the Docker Installation on Raspberry Pi

1. With Docker now set up on our Raspberry Pi, we should now go ahead and test to make sure it’s working.
    To test if Docker is working, we are going to go ahead and run the following command on our Pi.

    ```t
    docker run hello-world
    ```

    ```text
    This command will tell Docker to download, setup and run a docker container called “hello-world".
    ```

2. If you have successfully installed Docker to your Raspberry Pi, you should see a message with the following text in it.

    ```text
    Hello from Docker!
    ```

    ```text
    This message shows that your installation appears to be working correctly.
    ```
