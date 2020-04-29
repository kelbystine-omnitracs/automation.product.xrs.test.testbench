# automation.product.xrs.test.testbench

Assets for setting up a XRS test automation test bench

The folder docker-selenium-pi contains the dockerfiles for building the images on a raspberry pi.
Many of the copied folders will be updated for future use. (firefox, hubs, grids, etc ...)
Since it is copied from <https://github.com/SeleniumHQ/docker-selenium> the folder will contain quite a few extra files.

***Ignore them, and do not remove the files.***

The most important folders are:
BasePi
NodeBasePi
NodeChromium
StandaloneChromium

Build Standalone Chromium Container

1. Build a Selenium/Base image
    ( /docker-selenium-pi/BasePi $ docker build . -t selenium/base:local )
2. Build a Selenium/NodeBase image from selenium/base:local image
    ( /docker-selenium-pi/NodeBasePi $ docker build . -t selenium/node-base:local )
3. Build a Selenium/ChromiumNode image from selenium/node-chromium:local image
    ( /docker-selenium-pi/NodeChromium $ docker build . -t selenium/node-chromium:local )
4. Build a Standalone/Chromium image from selenium/node-chromium:local image
    ( /docker-selenium-pi/StandaloneChromium $ docker build . -t selenium/node-chromium:local )

The command to run a container from the image:

    docker run -d --name pi-chromium-server -p 4444:4444 --shm-size=2g selenium/standalone-chromium:local
