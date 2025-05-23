# Use official OpenJDK 17 runtime image as base
FROM openjdk:17-jdk-alpine

# Set working directory inside the container
WORKDIR /app

# Copy the built jar file into the container
COPY target/insure-me-1.0.jar insure-me.jar

# Expose port 8081 (as your app runs on 8081)
EXPOSE 8081

# Run the jar file
ENTRYPOINT ["java", "-jar", "insure-me.jar"]
