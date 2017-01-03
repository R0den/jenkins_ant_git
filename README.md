# Sample task answers.
Hi! I used VirtualBox instance with Ubuntu Server 14.04. 
JSudoku game java source code used.

- ```jsudoku_build.xml``` - Ant build.xml file with following targets 
 - sub.clear
 - git.getsource
 - checker
 - sub.compile
 - sub.manifest
 - jar <br>
 
 It includes all target related messages for more information about each step and configuration of Git and Checkstyle plugin.
 
- Install Jenkins, Ant, Git.
```
# Git and Ant
$ sudo apt-get install git ant -y

# Jenkins
$ wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -
$ sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
$ sudo apt-get update && sudo apt-get install jenkins
```
- Setup local git repository with JSudoku source code.
```
$ sudo adduser git
#password: git
$ sudo su - git
$ wget https://trello-attachments.s3.amazonaws.com/5865013c9e2c3bcfe9a9407e/5865017550cc1c7ead5c3cf1/52a4610fd1341e93fbe678c4eef0668d/jsudokukadu-jSudoku.tar.gz
$ tar zxf jsudokukadu-jSudoku.tar.gz
$ cd jSudoku
$ git config --global user.email "git@localhost"
$ git config --global user.name "git"
$ git init
$ git add .
$ git commit -m "Initial commit"
 
```

