# About

This project automates the docker image creation process of SonarQube server with slack plugin enabled using Jenkins pipeline.

# Requirements

Make sure following things are prepared in the system,

* make
* docker with sudoer user (i.e. ubuntu) group membership
* docker hub account

# Usage

Apply following command to run the docker image

```shell
docker run -d --name sonarqube \
    -p 9000:9000 -p 9092:9092 \
    -e SONARQUBE_JDBC_USERNAME=sonar \
    -e SONARQUBE_JDBC_PASSWORD=sonar \
    -e SONARQUBE_JDBC_URL=jdbc:postgresql://localhost/sonar \
    sonarqube
```

Next, browse to 127.0.0.1:9000 to view the sonarqube application.

# Credit

* Sonarqube server source origin can be found [https://github.com/SonarSource/docker-sonarqube](here).
* Sonar Slack plugin source origin can be found [https://github.com/kogitant/sonar-slack-notifier-plugin](here).
