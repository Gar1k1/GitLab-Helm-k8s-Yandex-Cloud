FROM eclipse-temurin:17-jdk-jammy as builder

WORKDIR /app

# Копируем pom.xml и запускаем сборку зависимостей
COPY pom.xml .
RUN mvn dependency:go-offline

# Копируем исходный код и собираем проект
COPY src ./src
RUN mvn package -DskipTests

# Запускаем приложение
CMD ["java", "-jar", "target/gateway-1.0-SNAPSHOT.jar"]