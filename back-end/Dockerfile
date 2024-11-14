#           NOT TESTED YET
FROM eclipse-temurin:17-jdk-alpine AS build
LABEL authors="XIONdevel, Anya-ctrl"
WORKDIR /app
# Copy the source code
COPY . /app
# Build the Spring Boot application
RUN ./mvnw clean package -DskipTests
# Stage 2: Run the application
FROM eclipse-temurin:17-jre-alpine
# Set the working directory
WORKDIR /app
# Copy the built jar file
COPY --from=build /app/target/*.jar app.jar
# Expose the port Spring Boot runs on
EXPOSE 8080
# Run the Spring Boot application
CMD ["java", "-jar", "app.jar"]