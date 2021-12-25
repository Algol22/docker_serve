![1x](https://user-images.githubusercontent.com/47631892/147390244-ecaad7d3-061b-427f-8ac3-ca3ce842f4db.png)
![2x](https://user-images.githubusercontent.com/47631892/147390245-ac310681-9e4d-4421-93a2-28d1bd00ad83.png)



# docker_serve <br/>
Docker_serve_upload<br/>

Commands:<br/>
1. Create 'Dockerfile' in the root folder:<br/>
2. Run MVN package<br/>
<br/>
#base docker image<br/>
FROM openjdk:11<br/>
LABEL maintainer="andrey.net"<br/>
ADD target/docker-0.0.1-SNAPSHOT.jar springboot-docker-demo.jar #file created under MVN package<br/>
ENTRYPOINT ["java", "-jar", "springboot-docker-demo.jar"]<br/><br/>

3. Build<br/>
docker build -t springboot-docker:latest .<br/>

4. Docker images<br/>
docker images<br/>

5. Run<br/>
docker run -p 8080:8080 springboot-docker<br/>

6. Connect to server:<br/>
ssh-keygen<br/>
//copy-paste and write secret word. Then build docker image and run it again via command line within the server<br/>

The end<br/>
***<br/>


