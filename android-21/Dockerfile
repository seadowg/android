# Pull base image
FROM seadowg/android-sdk

# Install Android APIs
RUN \
  echo y | /usr/local/android-sdk/tools/android update sdk --filter android-21 --no-ui --force -a && \
  echo y | /usr/local/android-sdk/tools/android update sdk --filter extra-android-support --no-ui --force -a && \
  echo y | /usr/local/android-sdk/tools/android update sdk --filter extra-android-m2repository --no-ui --force -a
  
