**Docker**

---

## Images

- https://hub.docker.com/u/in28min
- Currency Exchange Service 
	- in28min/mmv2-currency-exchange-service:0.0.1-SNAPSHOT
- Currency Conversion Service
	- in28min/mmv2-currency-conversion-service:0.0.1-SNAPSHOT
- Eureka
	- in28min/mmv2-naming-server:0.0.1-SNAPSHOT
- API GATEWAY
	- in28min/mmv2-api-gateway:0.0.1-SNAPSHOT

## URLS

#### Currency Exchange Service
- http://localhost:8000/currency-exchange/from/USD/to/INR

#### Currency Conversion Service
- http://localhost:8100/currency-conversion/from/USD/to/INR/quantity/10
- http://localhost:8100/currency-conversion-feign/from/USD/to/INR/quantity/10

#### Eureka
- http://localhost:8761/

#### Zipkin
- http://localhost:9411/

#### API GATEWAY
- http://localhost:8765/currency-exchange/from/USD/to/INR
- http://localhost:8765/currency-conversion/from/USD/to/INR/quantity/10
- http://localhost:8765/currency-conversion-feign/from/USD/to/INR/quantity/10
- http://localhost:8765/currency-conversion-new/from/USD/to/INR/quantity/10

#### Commands
```
docker run -p 9411:9411 openzipkin/zipkin:2.23
docker push docker.io/in28min/mmv2-currency-exchange-service:0.0.1-SNAPSHOT
docker-compose --version
docker-compose up
docker push in28min/mmv2-naming-server:0.0.1-SNAPSHOT
docker push in28min/mmv2-currency-conversion-service:0.0.1-SNAPSHOT
docker push in28min/mmv2-api-gateway:0.0.1-SNAPSHOT
watch -n 0.1 curl http://localhost:8000/sample-api
```
---

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
```
docker run 'Repository:Tag'
docker run -p {host-port}:{container-port} -d 'Repository:Tag' => Running container in detached mode (-d)
docker logs -f 'id' => Tailing Logs
docker container ls => Shows running containers
docker container ls -a => Shows all the containers irrespective of thier status
docker images => Shows only pulled images on local
docker container stop 'id' => To stop the running container
docker pull mysql
docker search mysql
docker image history 'imageId'
docker image inspect 'imageId'
docker image remove 'imageId' => Only remove from local machine
docker container pause 'Id'
docker container unpause 'Id'
docker container stop 'Id' => Stop gracefully
docker container kill 'Id' => Immediately terminate the process
docker stats
docker events
docker top 'Id'
docker run -m 512m --cpu quota 50000
docker system df
```
---
