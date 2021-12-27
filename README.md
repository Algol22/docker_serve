<b>Rest controller built on Ubuntu server using Docker</b>

![1x](https://user-images.githubusercontent.com/47631892/147390244-ecaad7d3-061b-427f-8ac3-ca3ce842f4db.png)
![2x](https://user-images.githubusercontent.com/47631892/147390245-ac310681-9e4d-4421-93a2-28d1bd00ad83.png)



# docker image built on Ubuntu server<br/>
<b>Docker_serve_upload</b><br/>

Commands:<br/>
<b>1. Create 'Dockerfile' in the root folder:</b><br/>
<b>2. Run MVN package</b><br/>
<br/>

#base docker image<br/>
FROM openjdk:11<br/>
LABEL maintainer="andrey.net"<br/>
ADD target/docker-0.0.1-SNAPSHOT.jar springboot-docker-demo.jar #file created under MVN package<br/>
ENTRYPOINT ["java", "-jar", "springboot-docker-demo.jar"]<br/><br/>


<b>3. Build</b><br/>
<code>docker build -t springboot-docker:latest .</code><br/>

<b>4. Docker images</b><br/>
<code>docker images</code><br/>

<b>5. Run</b><br/>
<code>docker run -p 8080:8080 springboot-docker</code><br/>

<b>6. Connect to server:</b><br/>
<code>ssh-keygen</code><br/>
//copy-paste and write secret word. Then build docker image and run it again via command line within the server<br/>

**run in browser:<br/>
<code>ServerIP:8080/welcome</code><br/>

The end<br/>
***<br/>


