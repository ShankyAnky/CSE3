# Astronomer Setup

### 1. Install Astronomer CLI
```
Install CLI : curl -sSL https://install.astronomer.io | sudo bash
```
### 2.  To Initialize Basic Setup
```
astro dev init
```
 ### 3.  To Start Local Development on Machine  
``` 
astro dev start
```
* It will Spin up 3 docker instances
	i.  Postgres
    ii.  Web Server
    iii.  Scheduler
### 4. To Stop Local Containers
```
astro dev stop
```
### 5. Login to Astronomer Cloud
   astro auth login <base_domain_url>
   Example: astro auth login gcp0001.us-east4.astronomer.io
### 6.  Get Workspace List
```
Get Workspace List
```
### 7. To Switch Workspace
```
astro workspace switch [UUID]
```
### 8. Get Deployment List
```
astro deployment list
```
### 9. To Create Deployment
```
astro deployment create <deployment-name> --executor=celery
```
### 10. To Delete Deployment
```
astro deployment delete <deployment-name> --workspace-id=<workspace_id>
```
### 11. To Update Deployment
```
astro deployment update <deployment-name> -workspace-id=<workspace_id>
```
### 12. To Stream Logs from Deployment
* Get Logs
```
astro deployment logs webserver/scheduler/worker <deployment-id> -f
```
* Get last 5min Logs 
```
astro deployment logs webserver/scheduler/worker <deployment-id> --since 5m
``` 
* Get last 25min Logs
```
astro deployment logs webserver/scheduler/worker <deployment-id> --since 25m
```
