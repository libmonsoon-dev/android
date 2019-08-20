FROM ubuntu

ENV DEBIAN_FRONTEND noninteractive

RUN apt update \
    && apt install -y unzip wget

ENV ANDROID_NDK_HOME /opt/ndk
ENV PATH ${ANDROID_NDK_HOME}/toolchains/llvm/prebuilt/linux-x86_64/bin/:${PATH}

RUN wget -q https://dl.google.com/android/repository/android-ndk-r20-linux-x86_64.zip \
    && unzip android-ndk-r20-linux-x86_64.zip \
    && mv android-ndk-r20 ${ANDROID_NDK_HOME} \
    && rm android-ndk-r20-linux-x86_64.zip
