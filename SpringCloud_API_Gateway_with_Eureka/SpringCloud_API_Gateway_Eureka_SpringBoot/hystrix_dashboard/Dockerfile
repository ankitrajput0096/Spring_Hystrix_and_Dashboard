 
# Base Image ubuntu
FROM ubuntu:18.04

# Installing dependencies
RUN apt-get update
RUN apt-get install -y openjdk-8-jdk maven 

# coping the required application files
COPY . /spring_boot_hystrix_dashboard
WORKDIR /spring_boot_hystrix_dashboard/hystrix-turbine

# building the spring boot app
RUN mvn clean install

WORKDIR /spring_boot_hystrix_dashboard/hystrix-turbine/target

# running the spring boot app
CMD ["java", "-jar", "hystrix-turbine-1.0.0-SNAPSHOT.jar"]
