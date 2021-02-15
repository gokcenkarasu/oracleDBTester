
# Oracle Database Connection Tester in Container 

<!-- vscode-markdown-toc -->

* 1. 1
* 2. List item


* 1. [Summary](#Summary)
* 2. [Java Code](#JavaCode)
* 3. [Product Versions](#ProductVersions)
* 4. [PreRequirements](#PreRequirements)
* 5. [How to run container version](#RunContainer)
	* 5.1. [In Docker](#InDocker)
	* 5.2. [In Kubernetes](#InKubernetes)
	* 5.3. [In Openshift](#InOpenshift)
* 6. [How to run jar version](#RunJarVerison)

<!-- vscode-markdown-toc-config numbering=true autoSave=true /vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->


# How to test oracle database connection in 2 minutes

> **Disclaimer:** If you are planning to use this standalone jar version please check your java version in your environment*

##  1. <a name='Summary'></a>Summary

This asset is created to show how to test oracle database in 2 minutes. There are two different options you can select: 
Runnable container version or standalone jar version.

Sometimes deployment processes take long time so it is time consuming to get sucsess or fail results. For example some deployments by using OpenShift operators take 30 minutes to complete. We need to check pre-requirements before the deployment processes.

This assset helps to test oracle db connection on containerized systems. 

There are 2 different options to use this tester:
	
> * Fist one is contianer base system. 
> * Second one is Jar base system. 
	
Both of them are using the same java codes of which you can find the details below. 

##  2. <a name='JavaCode'></a>Java Code

*  I developed Javacode with 1.8 JDK in Eclipse development environment. 
 	
	There are 3 Classes to run this jar program. 
	
	** 1- ConnectionInfo = This is static abstraction class to use collecting data from getting user. 
	
	** 2- ConnectionOracle = This includes runnable method and is using to get some information from user. it has time units sleep method to wait thread until wait to runnig containers. `TimeUnit.SECONDS.sleep(8);`
	
	** 3- OracleConTest = This is main method which include all conenctions methods.
	
> 		There are 3 different approaches for connection test:
>		1. It will generate URL string which it will get parameters from you
>		2. It will generate URL string without Username and Password
>		3. It will generate URL string and properties

If you select one of those options, the program executes only the selected one, if you enter "ALL" keyword, the program executes all of them to test it. 

 
##  3. <a name='ProductVersions'></a>Product Versions
	
This is 1.3 version of the program. 
	
I used Java 1.8 so If you are planning to use this standalone jar version please check your java version in your environment. Also if you want to use container version of the program, you need to have to at least one of these platforms: Docker, Podman, Kubernetes or Openshift.  

##  4. <a name='PreRequirements'></a>Pre-Requirments
<br/>
	For Jar version; 
		1.8 Java JRE, Oracle Databese version 19x
	For Contanirazed version;
		Openshift 3.x or newer versions, Docker 17.x or newer versions, Kubernetes 1.x or newer versions.
<br/>

##  5. <a name='RunContainer'></a>How to run container version?

I used IBM JAVA container as a base of this program.

[Oracle Test Connection Docker Hub](https://hub.docker.com/repository/docker/gokcenk/oracledbtester)

> `docker pull gokcenk/oracletestconnection`

###  5.1. <a name='InDocker'></a>In Docker

>  `docker run -it --rm oracledbtester`

###  5.2. <a name='InKubernetes'></a>In Kubernetes

> `kubectl run orcl --image=gokcenk/oracledbtester -it --rm`    

###  5.2. <a name='InOpenshift'></a>In Openshift

> `kubectl run orcl --image=gokcenk/oracledbtester -it --rm`    

##  6. <a name='RunJarVerison'></a>How to run container version?

 > `java -jar OracleTestConnection.jar`


🧿
