
# OpenVas9 Documentation

## 1: Install Docker
```
# sudo apt-get install
# sudo apt-get upgrade
# sudo apt-get install docker.io
```
Check that docker is active and running with
```
# sudo service docker status
```
If not run
```
# sudo service docker start
```

## 2: Install Container
```
# sudo docker run -d -p 443:443 --name openvas mikesplain/openvas
```
Wait for NVTs to install, check CPU usage to see if they are done

## 3: Open Greenbone Security Assistant Web Interface
Open a web browser and type the following url: ```http://localhost/```

Log in with 
username: ``admin``
password: ``admin``

The interface should look like this:

![Alt text](greenbone.png?raw=true)

## 4: Run a vulnerability scan
Navigate to Scans -> Tasks and use the task wizard with default settings to run a vulnerability scan

See Results:

![Alt text](results.png?raw=true)

## Docker-Compose.yml
```
version: '3.3'
services:
    openvas:
        ports:
            - '443:443'
        container_name: openvas
        image: mikesplain/openvas
```
