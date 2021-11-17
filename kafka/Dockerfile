# Kafka 3.0.0
FROM esempe/openjre11

LABEL maintainer="Stefan M. Prechtl"
LABEL description="Kafka 3.0.0"

RUN apt-get update && \
    apt install -y curl
RUN curl -L -O https://dlcdn.apache.org/kafka/3.0.0/kafka_2.13-3.0.0.tgz
RUN tar -zxf kafka_2.13-3.0.0.tgz -C /opt
RUN rm kafka_2.13-3.0.0.tgz

# Initialisierung wegen Modus mit "kraft"
RUN /opt/kafka_2.13-3.0.0/bin/kafka-storage.sh format -t xtzWWN4bTjitpL3kfd9s5g -c /opt/kafka_2.13-3.0.0/config/kraft/server.properties

# Server mit "kraft"-Config starten
ENTRYPOINT /opt/kafka_2.13-3.0.0/bin/kafka-server-start.sh /opt/kafka_2.13-3.0.0/config/kraft/server.properties
# Standardport freigeben
EXPOSE 9092