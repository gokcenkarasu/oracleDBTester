# Oracle Database Connection Tester in Container * 🧿

Runnable container or standalone.

<!-- vscode-markdown-toc -->

* 1. [Summary](#Summary)
* 2. [Java Code](#JavaCode)
* 3. [Product Versions](#ProductVersions)
* 4. [PreRequirements](#PreRequirements)
* 5. [How can you run container version](#RunContainer)
	* 5.1. [In Docker](#InDocker)
	* 5.2. [In Kubernetes](#InKubernetes)
	* 5.3. [In Openshift](#InOpenshift)
* 6. [How can you run jar version](#RunJarVerison)

<!-- vscode-markdown-toc-config
	numbering=true
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->


# How to test oracle database connection in 2 minutes...


***Disclaimer:** If you are planning to use this standalone jar version please check your java version in your enviorment..*

##  1. <a name='Summary'></a>Summary

This asset is created to show how to test oracle database with in 2 minutes. 

Sometimes deployment processes take long time so it is long time to take results sucsess or fail.For example some deployment with using OpenShift operators take 30minutes to complete it. They we need to check pre-requirments before the deployment processes.

This asssets help to test oracle db connection on continarized systems. 

There are 2 different option to use this tester. 
	
	**** Fist one is contianer base system. 
	**** Second one is Jar base system. 
	
Both of them are using the same java codes that you can find details below. 

##  2. <a name='JavaCode'></a>Java Code

* I developed Javacode with 1.8 JDK in Eclipse development enviorment. 
 	There are 3 Classes to run this jar program. 
	
	**** 1- ConnectionInfo = This is static abstraction class to use collecting data from getting user.
	**** 2- ConnectionOracle = This includes runnable method and is using to get some information from user. it has time units sleep method to wait thread until wait to runnig containers.
	**** 3- OracleConTest = This is main method which include all conenctions methods.	
	
	
	There are 3 diffrent approches tester to connection test
		1. It will generate URL string which it will get parameters from you
		2. It will generate URL string without Username and Password
		3. It will generate URL string and properties

If you want to selet once, the program execute only it, if you enter the "ALL" keyword, the program executes all of them to test it. 

 
##  3. <a name='ProductVersions'></a>Product Versions
	
	This is 1.3 version of program. 
	
	I used Java 1.8 so If you are planning to use this standalone jar version please check your java version in your enviorment. Also want to use container version of program , you have to at least on of Docker, Podman, Kubernetes or Openshift platforms.  

##  4. <a name='PreRequirements'></a>Pre-Requirments

	For Jar version;
		1.8 Java JRE, Oracle Databese version 19x 
	For Contanirazed version;
		

##  5. <a name='RunContainer'></a>How can you run container version?

###  5.1. <a name='InDocker'></a>In Docker

 docker run -it --rm oracledbtester

###  5.2. <a name='InKubernetes'></a>In Kubernetes

 kubectl run orcl --image=gokcenk/oracledbtester -it --rm    

###  5.2. <a name='InOpenshift'></a>In Openshift

 kubectl run orcl --image=gokcenk/oracledbtester -it --rm    

##  6. <a name='RunJarVerison'></a>How can you run container version?

java -jar OracleTestConnection.jar

