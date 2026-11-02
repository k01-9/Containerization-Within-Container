# Containerization Within Container

![](images/docker-in-docker.png)

In this Project I have used the concepts of Docker which I learned during the Training <a href="https://www.linkedin.com/posts/abhinavdubey26_docker-expertise-activity-6675343126288244737-TgyB"><b>Expertise in Docker</b></a> under the guidance of <b>World Record Holder Vimal Daga</b> sir. I have used these concepts to create an <b>Automated WebSite Deployment</b> as I have created in the <a href="https://github.com/Abhinav-26/DevOps-Integration/tree/master/DevOps%20Project-2">Previous Project</a>.

# How it is Different?
This Project, and the Project which I made in previous repository performs the same tasks but with a different approach. The advantage of using this apprach is that we can easily ship this complete project to where ever we want to run it. I have created a Jenkins-image using DOCKERFILE so that all my work will be saved into this and it won't effect my project. Also I have uploaded this jenkins-image to my <a href="https://hub.docker.com/u/alex43">DockerHub</a> profile.<br>

## Security and compatibility warnings

> **Do not run the example container on a personal laptop, shared server, or production machine without understanding the risks.** The command below mounts the host root filesystem at `/host` and the host Docker socket at `/var/run/docker.sock`. A process able to use that socket can effectively control the host's Docker daemon and may gain host-level access. These mounts are **not required to view the source**, and they must never be used for untrusted workloads.
>
> The image and Dockerfile are from an older Jenkins/CentOS workflow. The unversioned `FROM centos` base and older Jenkins repository instructions may no longer build on modern platforms. The example image is third-party and its current contents have not been verified. Evaluate the image and update the Dockerfile before attempting deployment.

For safer experimentation, prefer an isolated disposable virtual machine, a dedicated Docker daemon with narrowly scoped permissions, and a current supported Jenkins image. Do not expose the Jenkins port to a public network without authentication and TLS.

# How to Launch this Project?
**Historical example for trusted, isolated labs only; not a recommended production command.** Docker must be installed, and the additional security considerations above must be addressed. Run the Following commands in your terminal to launch this project.<br>
1. <code>docker pull alex43/jenkins-os:v1.0</code><br><br>
2. <code>docker run -dit -p 1234:8080 -v /:/host -v /var/run/docker.sock:/var/run/docker.sock --name automation_project alex43/jenkins-os:v1.0</code><br><br>
3. <code>Your_IP:1234</code>, Enter your Ip with port specified in browser after running container successfully.

For more details about this Project you can see this <a href="https://www.linkedin.com/posts/abhinavd26_containerization-within-container-activity-6671002631571431424-HclV">LinkedIn Post</a> where I have mentioned all the details regarding this Project and written a well documented article for using this concept of Docker-within-docker.<br>
For any query feel free to dm in my LinkedIn Handle.
