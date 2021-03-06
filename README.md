# jenkins-ci-cd

## Edit host_vars/yml.files and set variables.

## Install sudo, create user and place user authkey and give that
## user sudo right.
1. Run "ansible-playbook -i inventory/hosts user.yml --ask-become-pass"

## Install some common packages
1. Run "ansible-playbook -i inventory/hosts common_packages.yml"

## Install ansible on node.
1. Run "scp ansible_playbook.py user@host:/tmp"

## Install jenkins. Keep jenkins service enabled and keep running.
1. Run "ansible-playbook -i inventory/hosts jenkins_install.yml"

## Install lxd and setup couple of lxd container used as to be container
1. Run "ansible-playbook -i inventory/hosts lxd_install.yml"

## Bootstrap lxd
1. Run "lxd init" and complete steps

## Install packer in jenkins host
1. Run "ansible-playbook -i inventory/hosts packer_install.yml"

## Download packer-template from git in jenkins host and follow steps.
1. Run "git clone https://github.com/masumndc1/packer-template.git"

## Initial jenkins
1. Browse http://<jenkins_server_ip>:8080 and follow steps.
Initial password will be in here "/var/lib/jenkins/secrets/initialAdminPassword"

![Jenkins_initialization](/pics/Jenkins_initialiazion.png)

## Note:
You might need to install git and openjdk-8-jdk on lxd nodes.
