FROM ubuntu:18.04

#install
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y git
RUN apt-get install -y maven

RUN git clone https://github.com/Karasuma1412/clientserverexample.git
WORKDIR clientserverexample
RUN mvn package
WORKDIR client
RUN sed -i "s|http://localhost:8080|http://server-service:8080|g" conf/url.json
#RUN echo test >> conf/url.json
CMD ["java","-jar","target/client-1.0-SNAPSHOT-jar-with-dependencies.jar"]
