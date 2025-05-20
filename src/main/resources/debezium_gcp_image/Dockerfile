FROM quay.io/debezium/connect:latest

# Switch to root to create directories and copy files
USER root

# Create a directory for Google OAuth JARs
RUN mkdir -p /opt/kafka/libs/gcp

# Copy JARs into the container
COPY libs/*.jar /opt/kafka/libs/gcp/

# Fix permissions so the default user can access the jars
RUN chown -R 1000:1000 /opt/kafka/libs/gcp

# Switch back to the default user
USER 1000

# Add them to the Kafka classpath
ENV CLASSPATH="/opt/kafka/libs/gcp/*"
