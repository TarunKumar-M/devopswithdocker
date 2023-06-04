# We need Java 8. Choosing openjdk:8 from Docker Hub
FROM openjdk:8

EXPOSE 8080

WORKDIR /usr/src/app

# Copy the project
COPY . .

# Build the project
RUN ./mvnw package

# Command to run the application
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
