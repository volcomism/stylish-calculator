docker run -p 8080:8080 jenkins
This will store the workspace in /var/jenkins_home. All Jenkins data lives in there - including plugins and configuration. You will probably want to make that a persistent volume:

docker run --name myjenkins -p 8080:8080 -v /var/jenkins_home jenkins
The volume for the “myjenkins” named container will then be persistent.
