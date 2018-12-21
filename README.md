# edgeGW
Docker Form Factor for EdgeGW - BROADCOM API Gateway v9.4

a. Add you license file to this location and run the following commands to spin up the gateway
  1. export SSG_LICENSE_ENV=$(cat ./license.xml | gzip | base64 --wrap=0)
  2. docker-compose --project-name edgeGW up -d --build 
  
  
b. For following up the logs:
  1. docker-compose --project-name edgeGW logs --follow 


c. To STOP and remove the container:
  1. docker-compose --project-name edgeGW down -v


d. For healthcheck:
  1. watch docker ps to see all healthy contianers.
  
e. Volume folder is added to presist the changes, so that next time when you start the gateway all your policies/proxies, configurations, plug-ins are sustained. Make sure you have the relevant access for the same. 

f. Extra host is added to accomodate any additional external integrations, like SSO, Portal, AdvAuth or APM.  

g. SSO agent is enabled by default to accomodate Siteminder integration and relevant host information needs to be amended in the yaml. 
