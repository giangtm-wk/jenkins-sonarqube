## Run docker container
```bash
docker-compose up -d
```

## Check Jenkins version
```bash
docker exec -it jenkins cat /var/jenkins_home/config.xml | grep '<version>'
```

## Check SonarQube version
```bash
docker logs sonarqube | grep "SonarQube version"
```

## Stop and Restart container 
```bash
docker-compose down
docker-compose up -d
```