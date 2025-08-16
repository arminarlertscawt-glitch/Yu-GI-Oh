FROM maven:3.9.2-eclipse-temurin-17
WORKDIR /app
COPY . .
RUN mvn package -DskipTests
CMD ["java", "-jar", "target/telegrambot-fat.jar"]
