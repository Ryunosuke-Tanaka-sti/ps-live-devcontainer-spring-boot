FROM eclipse-temurin:21-jdk-alpine
WORKDIR /app

RUN addgroup spring && adduser  --ingroup spring --disabled-password spring
RUN chown spring:spring ./

RUN mkdir target && chown spring:spring target

COPY --chown=spring:spring ./app/.mvn .mvn
COPY --chown=spring:spring ./app/mvnw ./app/pom.xml ./

USER spring:spring

RUN ./mvnw dependency:go-offline

COPY --chown=spring:spring ./app/src ./src

CMD ["./mvnw", "spring-boot:run"]
