# Sample task answers.
I used VirtualBox instance with Ubuntu Server 14.04. 
JSudoku game java source code used.

- Install Jenkins, Ant, Git.
```
$ sudo apt-get install git ant -y
$ wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -
$ sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
$ sudo apt-get update && sudo apt-get install jenkins
```

- Setup local git repository with JSudoku source code.
```
$ sudo adduser git
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

- Create Ant build.xml <br>
```jsudoku_build.xml``` - Ant build.xml file with following targets 
 - sub.clear
 - git.getsource
 - checker
 - sub.compile
 - sub.manifest
 - jar <br>
 
 It includes all target related messages for more information about each step and configuration of Git and Checkstyle plugin.

- Installation of Checkstyle for Ant
```
$ sudo su - jenkins
$ wget https://sourceforge.net/projects/checkstyle/files/checkstyle/7.4/checkstyle-7.4-bin.zip/download
$ unzip downoad
$ cd checkstyle-7.4
$ cp checkstyle-7.4-all.jar docs && cd docs
$ unzip checkstyle-7.4-all.jar
```

- Create Jenkins Project 
 - ![alt tag](https://github.com/R0den/jenkins_ant_git/blob/master/installed_plugins.PNG) <br>
 - ![alt tag](https://github.com/R0den/jenkins_ant_git/blob/master/Creating_project.PNG)
 - ![alt tag](https://github.com/R0den/jenkins_ant_git/blob/master/console_output_build.PNG)
 - ![alt tag](https://github.com/R0den/jenkins_ant_git/blob/master/console_output2_build.PNG)
 - ![alt tag](https://github.com/R0den/jenkins_ant_git/blob/master/checkstyle_result.PNG)
 
- External files
 - Checkstyle - https://sourceforge.net/projects/checkstyle/files/checkstyle/7.4/checkstyle-7.4-bin.zip/download
 - JSudoku - http://jsudokukadu.cvs.sourceforge.net/

- Sources <br>
https://www.mkyong.com/ant/ant-how-to-create-a-java-project/ <br>
http://www.javaworld.com/article/2076208/java-app-dev/automate-your-build-process-using-java-and-ant.html <br>
http://leshcatlabs.net/2015/09/27/into-cicd-jenkins-ant-git-and-checkstyle/ <br>
http://checkstyle.sourceforge.net/anttask.html <br>
https://github.com/sevntu-checkstyle/checkstyle-samples/blob/master/ant-project/build.xml <br>
https://ant.apache.org/manual/tutorial-HelloWorldWithAnt.html <br>
