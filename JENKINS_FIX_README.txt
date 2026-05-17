
FIXED PORTS

API Gateway      : 8080
Customers Service: 8081
Visits Service   : 8082
Vets Service     : 8083
Config Server    : 8888
Discovery Server : 8761
Admin Server     : 9090
Zipkin           : 9411
MySQL            : 3306
Jenkins          : 8088
SonarQube        : 9000
Nexus            : 8085

IMPORTANT
- Jenkins moved to 8088 because API Gateway already uses 8080
- Nexus moved to 8085 because 8081 already used by customers-service
- Fixed Dockerfile path and service build contexts
- Compatible with MySQL 8.0
- Ready for Jenkins CI/CD pipeline

RUN COMMANDS

mvn clean package -DskipTests

docker compose up --build -d
