# Etapa 1: Dependencias
FROM eclipse-temurin:17-jdk AS dependencies
WORKDIR /app
COPY pom.xml mvnw ./
COPY .mvn ./.mvn
RUN ./mvnw dependency:go-offline -B

# Etapa 2: Tests
FROM eclipse-temurin:17-jdk AS test
WORKDIR /app
COPY . .
COPY --from=dependencies /root/.m2 /root/.m2
RUN ./mvnw test -B

# Etapa 3: Compilación
FROM eclipse-temurin:17-jdk AS compile
WORKDIR /app
COPY --from=test /app /app
COPY --from=dependencies /root/.m2 /root/.m2
RUN ./mvnw clean package -DskipTests

# Etapa 4: Producción
FROM eclipse-temurin:17-jre AS prod
WORKDIR /app
COPY --from=compile /app/target/*.jar /app.jar
EXPOSE 8080
CMD ["java", "-jar", "/app.jar"]
