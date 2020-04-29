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

The recommended order of setup for the test bench:

1. RaspberryPiSetup
2. JavaSetup
3. AndroidSDKSetup
4. NodeJsSetup
5. AppiumSetup
6. DockerSetup
7. DockerImageSetup
