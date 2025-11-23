#PROD
FROM eclipse-temurin:21-jre-alpine

WORKDIR /app

COPY target/*.jar app.jar

#QA
ENV PORT=8099
ENV JAVA_OPTS="-Xmx300m -Xms128m -XX:MaxMetaspaceSize=128m -XX:+UseG1GC"

EXPOSE 8099

##PROD
#ENTRYPOINT ["java", "-jar", "app.jar"]

#QA
ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -jar app.jar"]
