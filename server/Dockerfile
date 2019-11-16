FROM ubuntu:18.04

#install
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y git
RUN apt-get install -y maven

RUN git clone https://github.com/Karasuma1412/clientserverexample.git
WORKDIR clientserverexample
RUN mvn package
WORKDIR server
CMD ["java","-jar","target/server-0.0.1-SNAPSHOT.jar"]
