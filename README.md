# AzureCloud-
## ELK Deployment 
This repository contains files to deploy an ELK stack generated on an Azure Cloud enviroment to launch a logged and monitored instance to the DVWA.   
Below is a an image representation of the network created. 

[![](https://i.imgur.com/hYJZjCAm.jpg)](https://i.imgur.com/hYJZjCA.png)



## Description  
This network is designed give a load balanced web server exposure to the DVWA, 
inside a private network while being monitored by an ELK server. 
 
* The jump box protects private network from public access
* The load balancer offers an efficient distrubition of traffic, DOS prevention 
* The ELK server logs and monitors the virtual machine for any changes 
* Filebeat ships the logs to elasticsearch to be indexed to be visualized by kibana


## Firewall Modifications 
Port modification request depicted below

[![](https://i.imgur.com/e7uTkvNm.jpg)](https://i.imgur.com/e7uTkvN.png)

## Access Policies

Host uses SSH to gain access Jump server using public IPs. The Jump server accesses the Web server with internal IPs. Web server is set up to connect to ELK. Web server is configured on
backend pool of public load balancer to interact with DVWA containerized instance. Filebeat installed on Web server pushes logs to Elk server where an ELK stack has been deployed to monitor web server. Access policies ballows SSH service from host to Jumpbox, 

