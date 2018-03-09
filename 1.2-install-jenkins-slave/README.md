# Goal

Goal is to install SSH Jenkins slave agents. Jenkins master will trigger build, ci and cd jobs to these slaves over SSH.

# Prerequisites

Java must be installed in the OS to run Jenkins. Since Ansible is used to complete this challenge so install Ansible in workstation and install java in the remote machines, You can also find Ansible java installation role [here] (https://github.com/shudarshon/ansible_role/roles).

# Procedure

Change `hosts` and `play.yml` file accordingly. Then run `ansible-playbook -i hosts play.yml`.

# Test

Check if jenkins user home directory is created at `/var/lib/jenkins` location with jenkins user permission and ssh keys.

# Issue

If you find any issue then create it in the GitHub repo. For any suggestion, information or any help mail me at sdrsn.chaki@gmail.com. You can get me on my blog [here](www.shudarshon.com).
