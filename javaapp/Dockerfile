# FROM eclipse-temurin:21-jdk-alpine

# RUN mkdir /usr/src/
# COPY app/ /usr/src/
# WORKDIR /usr/src/
# RUN javac Main.java

# FROM eclipse-temurin:21-jre-alpine
# COPY --from=0 /usr/src/Main.class .

# CMD ["java", "Main"]

FROM maven:3.8.6-amazoncorretto-17 AS myapp-build
ENV MYAPP_HOME /opt/myapp
WORKDIR $MYAPP_HOME
COPY simple-api/pom.xml .
COPY simple-api/src ./src
RUN mvn -ntp dependency:go-offline
RUN mvn -ntp package -DskipTests

# Run
FROM amazoncorretto:17
ENV MYAPP_HOME /opt/myapp
WORKDIR $MYAPP_HOME
COPY --from=myapp-build $MYAPP_HOME/target/*.jar $MYAPP_HOME/myapp.jar

ENTRYPOINT java -jar myapp.jar