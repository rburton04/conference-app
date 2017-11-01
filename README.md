# Open Space Software Development 1025 10/27/2017

* Hashtags: #osswdev & #javaland
* Introduction: https://www.codecentric.de/2015/03/18/javaland-openspace-software-development/

## Application Links

| Environment         | Link          | 
| ------------------- |:-------------:|
| Production | currently unavailable |
| Staging    | currently unavailable | 
| Test       | currently unavailable |


## Infrastructure Links

* Continuous Delivery Build Pipeline **http://osswdev.codecentric.de/jenkins/view/Pipeline/**
* SonarQube SQM **http://osswdev.codecentric.de/sonarqube/dashboard/index/1**
* Artifact Repository **http://osswdev.codecentric.de/artifactory**
* Spring Boot Admin Client **http://osswdev.codecentric.de/adminclient**
* Amazon EC2 Dashboard **http://osswdev.codecentric.de/jenkins/view/Deployment%20Dashboard/**

## Developer Quickstart

```
cd monitoring
mvn clean install 
java -jar target/monitoring-1.0.0.jar

cd app
mvn clean install
java -jar target/conference-app-3.0.0.war
```

### Open WebApp
http://localhost:8080

### Open Monitoring App
http://localhost:8888
