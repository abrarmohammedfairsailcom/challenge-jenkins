build-slack-sonar-app:
	cd /var/lib/jenkins/workspace/$JENKINS_PROJECT_NAME/ &&  \
	rm -rf sonar-slack-notifier-plugin && \
	git clone https://github.com/kogitant/sonar-slack-notifier-plugin.git && \
	cd /var/lib/jenkins/workspace/$JENKINS_PROJECT_NAME/sonar-slack-notifier-plugin && `which mvn` clean package
	cp /var/lib/jenkins/workspace/$JENKINS_PROJECT_NAME/sonar-slack-notifier-plugin/target/*.jar /var/lib/jenkins/workspace/$JENKINS_PROJECT_NAME/7.1-alpine/

build-sonar-alpine-app:
	`which docker` docker --username=$USER_NAME --password=$PASSWORD https://hub.docker.com/
	`which docker` build -t $USER_NAME/sonar-alpine /var/lib/jenkins/workspace/$JENKINS_PROJECT_NAME/7.1-alpine/
	`which docker` push $USER_NAME/sonar-alpine

prune:
	`which docker` system prune -af
