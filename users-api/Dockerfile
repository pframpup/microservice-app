FROM openjdk:8

WORKDIR /usersapp
COPY . .

RUN ./mvnw clean install
CMD java -jar target/users-api-0.0.1-SNAPSHOT.jar