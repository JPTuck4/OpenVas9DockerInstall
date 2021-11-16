
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

## 4: 
Create a new target (under Configuration) as shown
![Alt text](newtarget.png?raw=true)

Create a new task (under Scans -> Tasks) as shown
![Alt text](newtask.png?raw=true)
