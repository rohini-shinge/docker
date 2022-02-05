**Docker**

**Recommendation 1**

If you are using Windows, make sure that you use PowerShell instead of Command Prompt.

**Recommendation 2**

If you are using Window 10 and are using docker toolbox

=> Use 192.168.99.100 instead of localhost.

Note: If 192.168.99.100 does not work, you can find the IP by using the command docker-machine ip

**Reason**=>In Window 10 when using docker toolbox, docker is configured to use the default machine with IP 192.168.99.100

=>Docker Registry : https://hub.docker.com

=>Running Version of Image : Container

**-- General Commands --**

1. docker run 'Repository:Tag'
2. docker run -p {host-port}:{container-port} -d 'Repository:Tag' => Running container in detached mode (-d)
3. docker logs -f 'id' => Tailing Logs
4. docker container ls => Shows running containers
5. docker container ls -a => Shows all the containers irrespective of thier status
6. docker images => Shows only pulled images on local
7. docker container stop 'id' => To stop the running container
8. docker pull mysql
9. docker search mysql
10. docker image history 'imageId'
11. docker image inspect 'imageId'
12. docker image remove 'imageId' => Only remove from local machine
13. docker container pause 'Id'
14. docker container unpause 'Id'
15. docker container stop 'Id' => Stop gracefully
16. docker container kill 'Id' => Immediately terminate the process
17. docker stats
17. docker events
18. docker top 'Id'
19. docker run -m 512m --cpu quota 50000
20. docker system df
---
