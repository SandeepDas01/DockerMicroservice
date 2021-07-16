FROM maven as build
MAINTAINER sandeepdas8080@gmail.com


WORKDIR /app
COPY . .
RUN mvn install

#jdk
FROM openjdk:11.0.10-jre
WORKDIR /app


#From build to copy to this app
COPY --from=build /app/target/zuul-0.0.1-SNAPSHOT.jar /app 
EXPOSE 9999

#java -jar artifact name
CMD ["java", "-jar", "zuul-0.0.1-SNAPSHOT.jar"] 