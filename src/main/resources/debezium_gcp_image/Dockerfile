FROM debezium/connect:latest

# Create a libs directory if needed
#RUN mkdir -p /kafka/libs

# Add your custom JAR (Google Auth JAR for OAuthBearer in this case)
ADD https://repo1.maven.org/maven2/com/google/cloud/hosted/kafka/managed-kafka-auth-login-handler/1.0.1/managed-kafka-auth-login-handler-1.0.1.jar /kafka/libs/
