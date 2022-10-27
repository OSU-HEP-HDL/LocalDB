# LocalDB Build EnV
This repository is a virtual environment for builing the LocalDB application. 


## Dependencies
You will need to install Vagrant and Ansible

* Mac OS
```
  brew install vagrant ansible
```

# To get started these are some basic Vagrant Commands
```
vagrant up # this command will start the virtual machine
vagrant ssh # this will allow you to log into the machine. Your files will be avalaible at /vagrant
vagrant provision # this will allow you to re-provision the machine if you need to make changes to the ansible file
vagrant halt # this will turn the machine off 
vagrant destroy # this will delete the machine 
```

You can also use a docker envrionment
```
vagrant up --provider docker
```
When you execute 
Ansible is used to configure the environment. 


Make sure you remove the line pymongo==3.12.1 from the requirements-pip.txt and replace it with pymongo. You may have to verifty that pymongo version 3.12.1 is installed. pymongo 4 will not work  