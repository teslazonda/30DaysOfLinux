# Day 2: Linux as a virtualization guest

### LPIC-1 Objective 102.6

### Virtual machines

It is possible to run multiple VMs on a single Hypervisor, or server

### Lab - Running CentOS on Debian with Docker

Downloaded and installed docker.

Ran `sudo docker run -it centos bash`

Ran lastest centos terminal from within the Debian virtual terminal.

#### Docker commands

List all containers `sudo docker ps -a`

Start docker image `sudo docker start <CONTAINER ID>`

Attach docker image to terminal (jump into) `sudo docker attach <CONTAINER ID>`

Delete docker image `sudo docker rm <CONTAINER ID>`


