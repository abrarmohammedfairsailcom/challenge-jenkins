# Essential Commands

#list all jobs  
jcli list-jobs  

#list all plugins  
jcli list-plugins

#install plugin  
jcli install-plugin https://updates.jenkins.io/latest/ldap.hpi -deploy -restart --username USERNAME --password PASSWORD #get the download url from plugin page archive download portion  

#build specific job  
jcli build JOB_NAME  

#build job with verbose  
jcli build JOB_NAME -s -v --user USERNAME --password-file  /var/lib/jenkins/credential  

#build by checking SCM changes  
jcli build JOB_NAME -c  

#get last n line build status of any job by build number  
jcli console JOB_NAME BUILD_NUMBER -n N  

#tail any build number of an ongoing job  
jcli console JOB_NAME BUILD_NUMBER -f  

#check Jenkinsfile syntax  
jcli declarative-linter --username USERNAME --password-file /var/lib/jenkins/credential < ~/code/Jenkins/Jenkinsfile  

#get job configuration as xml file  
jcli get-job JOB_NAME   #save the output as xml file  

#create job  
jcli create-job JOB_NAME --username USERNAME --password PASSWORD < job.xml    #job configuration as xml file  

#get user information  
jcli who-am-i  

#reload configuration  
jcli reload-configuration  

#safely reboot jenkins  
jcli safe-restart  

#safely shutdown jenkins  
jcli safe-shutdown  
