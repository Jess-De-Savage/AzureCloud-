# ELK Server Deployment-
## Using Azure
This repository documents the deployment of an ELK stack server generated on an Azure Cloud enviroment to launch a logged and monitored instance of the DVWA. 

Below is a an image representation of the network created. 

![](https://i.imgur.com/es466SV.png)

The intention of the project is to deploy a lab environment to test vulnerabilities in a containerized instance of the **damn vulnerable web application** with docker on a web server. A jumpbox server is utilized as a gateway to the network by host through SSH tunneling. The use of a load balancer provides a public IP for the web server. The benefits are increased privacy of the network, increased availibility and health monitoring of backend pool. Filebeat pushes web server logs to the Elk machine. Logstash aggregates logs, Elasticsearch indexes and analyzes and Kibana visualizes data to offer insights on changes in performance and fidelity of logs. 

## Description  
This network is designed give a load balanced web server exposure to the DVWA, 
inside a private network while being monitored by an ELK server.
 
* The jump box protects private network from public access
* The load balancer offers an efficient distribution of traffic, public IP, DoS protection
* The ELK server logs and monitors the virtual machine for any changes 
* Web server logs are shipped to ELK server, analyzed and indexed by elasticsearch then visualized with kibana 


## Firewall Modifications 
*Request for Firewall modfications depicted below*

[![](https://i.imgur.com/e7uTkvNm.jpg)](https://i.imgur.com/e7uTkvN.png)


## Documentation

[DVWA](https://hub.docker.com/r/vulnerables/web-dvwa)

[sebp/ELK](https://hub.docker.com/r/sebp/elk/)

[Filebeat](https://www.elastic.co/downloads/beats/filebeat)


# Topology Description 

|Name |Function |IP Address |OS |
| ---- | ---- | ---- | ---- |
| Jumpbox | Gateway | 13.82.169.177 | Ubuntu 18.04 |
| Web Server | DVWA  | 10.0.0.5 | Ubuntu 18.04 |
| Elk Server | ELK Stack | 10.1.0.4 | Ubuntu 18.04 |


##### Access Policies

