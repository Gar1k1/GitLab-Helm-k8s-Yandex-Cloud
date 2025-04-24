# Этап сборки
FROM eclipse-temurin:21-jdk-jammy AS builder

WORKDIR /app

COPY pom.xml ./
COPY src ./src

RUN ./mvnw package -DskipTests

# Этап продакшн
FROM eclipse-temurin:21-jre-jammy

WORKDIR /app

COPY --from=builder /app/target/*.jar app.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "app.jar"]
