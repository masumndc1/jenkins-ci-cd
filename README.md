# jenkins-ci-cd

## Install jenkins. Keep jenkins service enabled and keep running.
1. Run "ansible-playbook -i inventory/hosts jenkins_install.yml"

## Install lxd and setup couple of lxd container used as to be container
1. Run "ansible-playbook -i inventory/hosts lxd_install.yml"

## Bootstrap lxd
1. Run "lxd init" and complete steps

## Download lxd image and run container
1. Run "ansible-playbook -i inventory/hosts lxd_container.yml"
