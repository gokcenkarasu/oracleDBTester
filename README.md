# Oracle Database Connection Tester in Container

Runnable Container or standalone jar.

docker push gokcenk/oracledbtester:latest

<!-- vscode-markdown-toc -->
* 1. [Summary](#Summary)
* 2. [Java Code - Know-How](#SharedKnow-How)
* 3. [Product Versions](#ProductVersions)
* 4. [PreRequirements](#PreRequirements)
* 5. [How can you run container version](#ODM-OperationalDecisionManager)
	* 5.1. [In Docker](#Importingthedecisionservice)
	* 5.2. [In Kubernetes](#Deployingtheservice)
	* 5.3. [In Openshift](#ExposingtheruleviaRESTAPI)
* 6. [How can you run jar version]

<!-- vscode-markdown-toc-config
	numbering=true
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->


# How can you test oracle database connection in 2 minutes...
* 🧿

***Disclaimer:** If you are planning to open this diagnosing tool to public, It is highly recommended to change the rules implemented inside ODM which combines symptoms and diseases with the help of a health professional before going live.*

##  1. <a name='Summary'></a>Summary

This asset is created to show how to define a workflow inside [IBM BAW](https://www.ibm.com/products/business-automation-workflow) (Business Automation Workflow) including UI designs, service integration, database integration and ODM integration. It also gives information about how to integrate workflow data with [IBM BAI](https://www.ibm.com/support/knowledgecenter/SSYHZ8_19.0.x/com.ibm.dba.bai/topics/con_bai_overview.html) (Business Automation Insights) and generate custom graphics and reports from the data transferred to BAI. 

It can be used by Ministry of Health or healthcare organizations in order to gather symptoms, disease history and physical information from citizens and diagnose if they are infected by COVID-19 or not.  It also helps these organizations to manage inform the citizens and conduct the emergency situations like quarantine / sending ambulance / monitoring the patient during home quarantine if required. 

Required rules to diagnose symptoms are defined inside [IBM ODM](https://www.ibm.com/products/operational-decision-manager) (Operational Decision Manager) to make them easy to change quickly without the need of IT. 
It is very important to provide a flexible and easy to change platform in such situations. Since it is a new epidemic and each day as citizens, we and health organizations are learning a new behaviour of this virus. So, the symptoms and affect on cronical diseases may differ day by day.  
All of the rulesets implemented inside ODM can easily be changed with the light of recommendations of medical boards. 

![](https://raw.githubusercontent.com/DBA-Turkiye/DiagnoseCovid19/master/Documentation/images/Scenario.png)

##  2. <a name='SharedKnow-How'></a>Shared Know-How
 * IBM BAW:
    * Implementing a workflow
    * Implementing user interfaces 
    * Implementing service integrations
    * How to call ODM services
    * Database integration
    * Views
    * Sending E-mail
    * Integrate date to IBM BAI using emitters
* IBM ODM:
    * Implementing a Decision Service on IBM ODM
    * Implement rules using decision tables
    * Implement rules by using if/then/else statements
    * Deploy a decision service. 
    * Test decision service through REST API. 
* IBM BAI:
	* Transfer data from BPM & ODM
	* Creating dashboards from collected data. 
	* Using emitters to collect data. 



