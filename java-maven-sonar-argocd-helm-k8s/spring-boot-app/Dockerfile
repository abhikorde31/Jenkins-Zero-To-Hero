# You can change this base image to anything else
# But make sure to use the correct version of Java
FROM adoptopenjdk/openjdk11:alpine-jre

# Install Maven
RUN apk add --no-cache maven

# Simply the artifact path
ARG artifact=target/spring-boot-web.jar

WORKDIR /opt/app

COPY ${artifact} app.jar

# ✅ Keep container running after app starts (important for Jenkins)
CMD ["sh", "-c", "java -jar app.jar & tail -f /dev/null"]
