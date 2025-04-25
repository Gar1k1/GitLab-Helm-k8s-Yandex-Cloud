# Используем базовый образ
FROM eclipse-temurin:21-jdk-jammy AS builder

# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем pom.xml для установки зависимостей (если нужно)
COPY pom.xml ./

# Копируем скомпилированный артефакт из папки target
COPY target/your-artifact.jar ./your-app.jar

# Запуск приложения
CMD ["java", "-jar", "./your-app.jar"]
