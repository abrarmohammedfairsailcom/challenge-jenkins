#Prerequisite

* Manage USER API token from Jenkins>Manage Jenkins>Mange Users  
* Make sure unchecking prevent CSRF token security option in Jenkins>Manage Jenkins>Change Global Security  
* Gather PROJECT_NAME from jenkins application url in browser address bar  

#Build project

curl -X POST http://SERVER_IP:8080/job/PROJECT_NAME/build --user USER:USER_API_TOKEN  

#Get project config.xml  

curl http://SERVER_IP:8080/job/PROJECT_NAME/config.xml --user --user USER:USER_API_TOKEN  

#Disable/Enable project

curl -X POST http://SERVER_IP:8080/job/PROJECT_NAME/disable --user --user USER:USER_API_TOKEN  
curl -X POST http://SERVER_IP:8080/job/PROJECT_NAME/enable --user --user USER:USER_API_TOKEN  
