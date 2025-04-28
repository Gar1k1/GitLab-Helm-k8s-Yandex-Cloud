FROM eclipse-temurin:21-jdk-jammy AS builder

WORKDIR /app

COPY pom.xml ./

COPY target/gateway-1.0-SNAPSHOT.jar ./your-app.jar

CMD ["java", "-jar", "./your-app.jar"]
