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
