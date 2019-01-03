FROM java:latest
WORKDIR /
ADD ../build/libs/kafka-data-gen.jar kafka-data-gen.jar
CMD ["java", "-jar", "kafka-data-gen.jar", "-message-count", "1000000", "-message-size", "256", "-output-stdout", "true", "-eps", "1000"]
