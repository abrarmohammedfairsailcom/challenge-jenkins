# Prerequisite

* Running Jenkins Instance
* Java installed in local workstation (we will download jekins cli jar in local
  workstation)
* SSH public key of user

# Download Jenkins CLI jar

* Add SSH public key of user in Jenkins Dashboard > Manage User > Add SSH
  public key

* wget -P ~/.jenkins http://SERVER_IP:8080/jnlpJars/jenkins-cli.jar

# Run Jenkins CLI

* Add an alias in ~/.bashrc --> alias jcli="java -jar ~/.jenkins/jenkins-cli.jar"

* Next, use `source ~/.bashrc` command to restart the settings.

* Run, `jcli -s http://SERVER_IP:8080 help`

* Optionally, you can export JENKINS_URL=http://SERVER_IP:8080 ti use jenkins
  cli without server url parameter.

