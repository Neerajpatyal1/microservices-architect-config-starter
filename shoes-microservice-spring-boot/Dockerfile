FROM maven  as build
WORDIR /app
COPY  . .
RUN mvn install 

FROM  openjdk:11.0.10-jre
WORDIR /app
COPY --from=build  /app/shoes-0.0.1-SNAPSHOT.jar /app
EXPOSE 1002
CMD [ "java","-jar","shoes-0.0.1-SNAPSHOT.jar"]