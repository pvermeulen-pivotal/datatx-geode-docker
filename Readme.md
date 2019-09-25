# Gemfire Docker Example

## Build and Run Docker Image

```bash
docker build . -t <YOUR_TAG>
docker run -t <YOUR_TAG>
```

## Explanation
This will run a two node one locator geode cluster with a partitioned redundant region created.  You can then use gfsh to access it.

## References

- How to run Apache Geode with docker: https://cwiki.apache.org/confluence/display/GEODE/How+to+use+Geode+on+Docker

- Gemfire Docker Repo: https://github.com/GSSJacky/gemfire-docker/blob/master/Dockerfile

- Docker Geode: https://github.com/markito/geode-docker

docker build -t "geode_1_6_0:latest" .   
docker run --name geode -d -p 8080:8080 -p 10334:10334 -p 40404:40404 -p 40405:40405 -p 1099:1099 -p 7070:7070 geode_1_6_0:latest
docker exec -it geode /bin/bash 

docker save geode_1_6_0:latest > geode-1.6.0.tar"# datatx-geode-docker" 
