# MS17-010-docker
Docker env supporting MS17-010 exploits

DISCLAIMER:
I don't know docker very well. So if you find yourself pulling your hair out over my usage of docker: I don't care.

After a long time troubleshooting errors from MS17-010 exploit scripts, I cobbled together a docker environment that can support these exploits out of the box. **YOU WILL NOT FIND ANY EXPLOIT CODE IN THIS REPO, NERD**

The dockerfile was built on top of an existing one for `python2` located here:  
https://github.com/Docker-Hub-frolvlad/docker-alpine-python2  

If you came here looking for the exploits themselves I recommend the following:  
https://github.com/worawit/MS17-010  
https://www.exploit-db.com/exploits/42315 or the like  

A brief set of usage instructions is as follows:
This will create a container with your exploit code in `/src/`
```
sudo docker build - < Dockerfile
sudo docker images
sudo docker run -v "/path/to/exploit/code:/src/" -it --name [NEW CONTAINER NAME] [IMAGE ID]
```
