# Docker Compose

>Follow this guide to setup Docker Compose to run Activiti Cloud on your local computer in Docker VM



/![DJ Events](/public/images/video1512268814_wrUjMdLr.gif 'DJ Events')





## Hardware Setup
You will need to allocate at least 4 CPU cores and 8 Gb of RAM for your Docker VM machine

## Software Setup
Before you start, the following packages must be installed:
Install Docker for Desktop or Docker Toolbox for your OS
Install Docker-compose if you use Docker for Desktop.
Install GNU Make. For Linux and Mac it is usually installed already, for Windows use Chocolatey GNU Make to install Make.
Install Git Bash Terminal . For Linux and Maс it is usually pre-installed. If you use Docker for Desktop on Windows, use Chocolatey Git Install to install Git Bash Terminal.


## Clone Activiti Cloud Examples
Open Bash command line terminal and run these commands to clone [https://github.com/Activiti/activiti-cloud-examples](https://github.com/Activiti/activiti-cloud-examples) into your local environment:

```
git clone https://github.com/Activiti/activiti-cloud-examples
cd activiti-cloud-examples/docker-compose
```

## Configure Your Environment
You need to edit ```.env``` file to configure DOCKER_IP property based on your OS and Docker VM type.
Use your local computer IP address for Docker for Desktop on Linux, Mac or Windows
Use ```docker-machine ip``` command if you use Docker Toolbox
Don't use 127.0.0.1 or localhost


## How To Run Activity Cloud
### Start Modeler
```make modeler```
After starting Modeler, wait for the containers to start. You can check the status by running ```make ps``` and ```make logs``` command to make sure that the containers are ready.
To access modeler please open the url in your browser:

```
http://$DOCKER_IP/modeling
```





