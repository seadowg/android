# Pull base image.
FROM java:openjdk-7-jdk

# Install Android
RUN \
  wget http://dl.google.com/android/android-sdk_r24.0.2-linux.tgz && \
  tar -xzvf android-sdk_r24.0.2-linux.tgz && \
  rm android-sdk_r24.0.2-linux.tgz && \
  mv android-sdk-linux /usr/local/android-sdk

# Install Android Tools
RUN \
  echo y | /usr/local/android-sdk/tools/android update sdk --filter platform-tools --no-ui --force -a && \
  echo y | /usr/local/android-sdk/tools/android update sdk --filter build-tools-21.1.2 --no-ui --force -a

# Install Android APIs
RUN echo y | /usr/local/android-sdk/tools/android update sdk --filter android-19 --no-ui --force -a
RUN echo y | /usr/local/android-sdk/tools/android update sdk --filter extra-android-support --no-ui --force -a
RUN echo y | /usr/local/android-sdk/tools/android update sdk --filter extra-android-m2repository --no-ui --force -a

# Define working directory.
WORKDIR /data

# Setup ANDROID_HOME
ENV ANDROID_HOME /usr/local/android-sdk
