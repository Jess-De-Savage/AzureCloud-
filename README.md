# AzureCloud-
## ELK Deployment 
This repository documents the deployment of an ELK stack server generated on an Azure Cloud enviroment to launch a logged and monitored instance of the DVWA. 

Below is a an image representation of the network created. 

![](https://i.imgur.com/bXvM6NG.png)

The intention of the project is to deploy a lab environment to test vulnerabilities of a containerized instance of the "damn vulnerable web app" on a web server. A jumpbox server is used as a gateway to the network through an SSH tunnel to host. Use of a load balancer provides public internet access for the web server. This provides increased isolation of the network, increased availibility (especially if scaled) and monitoring the health of backend server. Filebeat installed on Web server pushes logs to Elk server. ELK server aggregate logs, indexes/analyzes and visualizes data to offer insights on changes in performance and fidelity of logs. 

## Description  
This network is designed give a load balanced web server exposure to the DVWA, 
inside a private network while being monitored by an ELK server. 
 
* The jump box protects private network from public access
* The load balancer offers an efficient distribution of traffic, public IP, DoS protection
* The ELK server logs and monitors the virtual machine for any changes 
* Web server logs are pushed to ELK server, analyzed and indexed by elasticsearch then visualized by kibana


## Firewall Modifications 
*Request for Firewall modfications depicted below*

[![](https://i.imgur.com/e7uTkvNm.jpg)](https://i.imgur.com/e7uTkvN.png)


## Documentation
[filebeat.yml]()

[DVWA]()

[ELK/sebp]()



# Topology Description 

|Name |Function |IP Address |OS |
| ---- | ---- | ---- | ---- |
| Jumpbox | Gateway | 13.82.169.177 | Ubuntu 18.04 |
| Web Server | DVWA  | 10.0.0.5 | Ubuntu 18.04 |
| Elk Server | ELK Stack | 10.1.0.4 | Ubuntu 18.04 |


##### Access Policies

