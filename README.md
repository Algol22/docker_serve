![1x](https://user-images.githubusercontent.com/47631892/147390244-ecaad7d3-061b-427f-8ac3-ca3ce842f4db.png)
![2x](https://user-images.githubusercontent.com/47631892/147390245-ac310681-9e4d-4421-93a2-28d1bd00ad83.png)



# docker_serve
Docker_serve_upload

Commands:
1. Create 'Dockerfile' in the root folder:
2. Run MVN package

#base docker image
FROM openjdk:11
LABEL maintainer="andrey.net"
ADD target/docker-0.0.1-SNAPSHOT.jar springboot-docker-demo.jar #file created under MVN package
ENTRYPOINT ["java", "-jar", "springboot-docker-demo.jar"]
3. Build
docker build -t springboot-docker:latest .

4. Docker images
docker images

5. Run
docker run -p 8080:8080 springboot-docker


