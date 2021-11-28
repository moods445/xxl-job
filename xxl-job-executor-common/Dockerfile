FROM openjdk:8-jdk-slim
MAINTAINER modds

ENV PARAMS=""
ENV TZ=PRC
ARG JAR_FILE

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
ADD target/xxl-job-executor-common-*.jar /app.jar
ENTRYPOINT ["sh","-c","java -jar $JAVA_OPTS /app.jar $PARAMS"]