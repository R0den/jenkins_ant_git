# Sample task answers.
Hi! This is the implementation of Jenkins with Ant and Git. I used VirtualBox instance with Ubuntu Server 14.04. JSudoku game java source code used.

1. Install Jenkins, Ant, Git.
```
# Git and Ant
$ sudo apt-get install git ant -y

# Jenkins
$ wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -
$ sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
$ sudo apt-get update && sudo apt-get install jenkins
```

2. Setup local git repository with JSudoku source code.


Hi! This is the implementation of Jenkins with Ant and Git. I'll try to explain whole process of installation and configuration of Jenkins wich will build Java source using Apache Ant script.
