## spring-boot-app
 
This is a simple sprint boot based Java application that can be built using Maven. 

## Execute the application locally and access it using your browser

Checkout the repo and move to the directory

```
git clone https://github.com/charitha-allu/sprint-boot-app
```

Execute the Maven targets to generate the artifacts

```
brew install maven
```
## for windows
```
mvn clean package
```

The above maven target stores the artifacts to the `target` directory. You can either execute the artifact on your local machine
(or) run it as a Docker container.

## Execute locally and access the application on http://localhost:8080

```
java -jar target/spring-boot-web.jar
```

## The Docker way

Build the Docker Image

```
docker build -t ultimate-cicd-pipeline:v1 .
```

```
docker run -d -p 8010:8080 -t ultimate-cicd-pipeline:v1
```

Access the application on `http://<ip-address>:8010`


## Next Steps

## Configure a Sonar Server locally

```
apt install unzip
adduser sonarqube
wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.4.0.54424.zip
unzip *
chmod -R 755 /home/sonarqube/sonarqube-9.4.0.54424
chown -R sonarqube:sonarqube /home/sonarqube/sonarqube-9.4.0.54424
cd sonarqube-9.4.0.54424/bin/linux-x86-64/
./sonar.sh start
```

Now you can access the `SonarQube Server` on `http://<ip-address>:9000` 
