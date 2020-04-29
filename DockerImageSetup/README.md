# Build Standalone Chromium Container

1. Build a Selenium/Base image:

    ```t
    cd ~/docker-selenium-pi/BasePi
    docker build . -t selenium/base:local
    ```

2. Build a Selenium/NodeBase image from selenium/base:local image:

    ```t
    cd ~/docker-selenium-pi/NodeBasePi
    docker build . -t selenium/node-base:local
    ```

3. Build a Selenium/ChromiumNode image from selenium/node-chromium:local image:

    ```t
    cd ~/docker-selenium-pi/NodeChromium
    docker build . -t selenium/node-chromium:local
    ```

4. Build a Standalone/Chromium image from selenium/node-chromium:local image:

    ```t
    cd ~/docker-selenium-pi/StandaloneChromium
    docker build . -t elenium/node-chromium:local
    ```

**The command to run a container from the image:**

```t
docker run -d --name pi-chromium-server -p 4444:4444 --shm-size=2g selenium/standalone-chromium:local
```
