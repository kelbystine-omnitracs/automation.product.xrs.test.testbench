FROM selenium/node-base:local
LABEL authors=kstine@omnitracs.com

USER root

#============================================
# Google Chromium
# Needed for arm based architecture
#============================================
# Commented out: future use
# can specify versions by CHROMIUM_VERSION;
#  e.g. google-chrome-stable=53.0.2785.101-1
#       google-chrome-beta=53.0.2785.92-1
#       google-chrome-unstable=54.0.2840.14-1
#       latest (equivalent to google-chrome-stable)
#       google-chrome-beta  (pull latest beta)
#============================================
# ARG CHROMIUM_VERSION="google-chrome-stable"
RUN wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add - \
  && apt-get update -qqy \
  && apt-get -qqy install \
    chromium-browser

#=================================
# Chrome Launch Script Wrapper
#=================================
COPY wrap_chrome_binary /opt/bin/wrap_chromium_binary
RUN /opt/bin/wrap_chromium_binary

#============================================
# Chromium webdriver
#============================================
# Commented out: future use
# can specify versions by CHROMIUM_DRIVER_VERSION
# Latest released version will be used by default
#============================================
# ARG CHROMIUM_DRIVER_VERSION
RUN apt-get -qqy install chromium-chromedriver

USER seluser

COPY generate_config /opt/bin/generate_config

# Generating a default config during build time
RUN /opt/bin/generate_config > /opt/selenium/config.json
