# Ubuntu 20.04 mit OpenJDK 11
FROM ubuntu:20.04

LABEL maintainer="Stefan M. Prechtl"
LABEL description="Ubuntu 20.04 mit OpenJDK 11"

# OpenDJK installieren und aufräumen
RUN apt-get update && \
    apt install -y openjdk-17-jdk && \
    apt clean -y && \
    rm -r /var/cache/apt /var/lib/apt/lists/*

# Umgebungsvariablen setzen
ENV JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
ENV PATH=${PATH}:${JAVA_HOME}/bin

