# This image is based on Alpine Linux image, which is only a 5MB image, and contains OpenJDK 8.
FROM openjdk:8-jdk-alpine
EXPOSE 8000
ADD microservice-configserver.jar app.jar
RUN sh -c 'touch /app.jar'
RUN echo 'Asia/Shanghai' > /etc/timezone
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar $ENVIRONMENT_VAR"]
