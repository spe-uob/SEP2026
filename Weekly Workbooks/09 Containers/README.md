# Containers
This week we will learn about containers, an extremely successful virtualisation technique that is key to the deployment of your application. 

### Task 1: Introduction to Containers 
<table><tr><td> <h3>What are Containers?</h3>
<p></p>
Containers are packages of software that have everything someone needs to run your system in the cloud - code, libraries, system tools, configuration files and anything else needed.
<p></p>
They're created to enable anyone to be able to run and deploy your system from anywhere, making it portable and not reliant on specific operating systems.  
<p></p>
 They are resource-efficient can be used in different ways - you may have your whole software system in one container, or divided between a number of different containers. 
 <p></p>
 <p></p>
</tr></table>

**Please watch these two short videos:**

* an [introduction to containers](https://uob.sharepoint.com/:v:/t/UnitTeams-COMS20006-2021-22-TB-4-A/EfaHnCJKChNf6G-WRrzsZ_YBWNdKPljaOxW7rARLVC48UQ?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=Dpx318)  to
find out the main concepts
*  [a demonstration](https://uob.sharepoint.com/:v:/t/UnitTeams-COMS20006-2021-22-TB-4-A/EaBpY4vgJr1TjzEbrNz-o0YBFHV9E4hICB3k1hRliK1alw?e=ueZEj0&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D) how a Spring application can be dockerised.

These are focused on Spring web applications, but if you are not making your product with Spring, you should still watch them to learn the key concepts.  

#
### Task 2: Install Docker

We recommend you use [Docker](https://www.docker.com/) for containerisation. 

They have great documentation - [start here](https://docs.docker.com/get-started/get-docker/) to install the client designed for your system, and if you need any guides, advice or other information, you can probably find it on [DockerDocs](https://docs.docker.com/).

# 
### Task 3: Run Hello World

With the docker client working on your system you can now take the first steps: 

* enter `docker run hello-world`. 
* If everything goes to plan, you should see a message on the terminal. 
* A call to `docker ps` should not show anything as the container exits immediately.
* However, you can run `docker images` to find the name of the image and then call `docker inspect <ref>` with the name of the image to see some metadata.  

# 
### Task 4: Dockerise a Spring Boot App

The final step is to dockerise a Spring Boot app. 

If your team is working on a Spring Boot app, now should be the moment to put that into a container. If not, you might want to dockerise the example from the practical introduction video

The code can be found on github under [https://github.com/spe-uob/spring-hello-world](https://github.com/spe-uob/spring-hello-world).

Recall the steps we took in the practical video and you should have it running in no time:
* build the app jar with `mvn package`
* find the path to the jar from the target folder
* check the base image in the Dockerfile matches your local Java version
* run `docker build` and finally `docker run`.

See the video for the full commands.  

# 
## Docker and React
[Murray Groves](https://github.com/MurrayGroves) has written a great [guide to Docker, React and Reverse Proxies](https://github.com/spe-uob/knowledge-hub/blob/main/React%20-%20Docker%20and%20Reverse%20Proxies%20for%20Development%20&%20Production.md) for the [SEP Knowledge Hub](https://github.com/spe-uob/knowledge-hub/), which we recommend if you're using React. 



