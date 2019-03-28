FROM openjdk:8-jdk-alpine
VOLUME /tmp
ADD leaf.jar app/app.jar
ADD lib/ app/lib/
RUN sh -c 'touch app/app.jar'
ENV JAVA_OPTS=""
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app/app.jar" ]