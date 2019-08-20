FROM ubuntu

ENV DEBIAN_FRONTEND noninteractive

RUN apt update \
    && apt install -y unzip wget

RUN apt install -y openjdk-8-jdk

ENV ANDROID_HOME /opt/android-sdk
ENV PATH ${PATH}:${ANDROID_HOME}/tools/bin

RUN mkdir -p ${ANDROID_HOME} \
    && cd ${ANDROID_HOME} \
    && wget -q https://dl.google.com/android/repository/sdk-tools-linux-4333796.zip \
    && unzip sdk-tools-linux-4333796.zip \
    && rm sdk-tools-linux-4333796.zip \
    && mkdir ${ANDROID_HOME}/licenses \
    && echo "24333f8a63b6825ea9c5514f83c2829b004d1fee" > ${ANDROID_HOME}/licenses/android-sdk-license
