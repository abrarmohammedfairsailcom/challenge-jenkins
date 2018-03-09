# Goal

Goal is to install Jenkins Master in Tomcat. This Jenkins master will be used for configuration only. Build, CI and CD will be performed by Jenkins slaves.

# Prerequisites

Java must be installed in the OS to run Jenkins. Since Ansible is used to complete this challenge so install Ansible in workstation and install java in the remote machines, You can also find Ansible java installation role [here] (https://github.com/shudarshon/ansible_role/roles).

# Procedure

Change `hosts` and `play.yml` file accordingly. Then run `ansible-playbook -i hosts play.yml`.

# Test

To check application status go to http://SERVER_IP:8080. It should work on both ubuntu & centos.

# Issue

If you find any issue then create it in the GitHub repo. For any suggestion, information or any help mail me at sdrsn.chaki@gmail.com. You can get me on my blog [here](www.shudarshon.com).
