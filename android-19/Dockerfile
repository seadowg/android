# Pull base image
FROM seadowg/android-sdk:build-tools-23.0.3

# Install Android APIs
RUN \
  echo y | /usr/local/android-sdk/tools/android update sdk --filter android-19 --no-ui --force -a && \
  echo y | /usr/local/android-sdk/tools/android update sdk --filter extra-android-support --no-ui --force -a && \
  echo y | /usr/local/android-sdk/tools/android update sdk --filter extra-android-m2repository --no-ui --force -a

# Setup ANDROID_HOME
ENV ANDROID_HOME /usr/local/android-sdk
