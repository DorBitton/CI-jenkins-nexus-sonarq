## Continuous Integration using Jenkins, Nexus, Sonarqube &amp; Slack.

In this project we will be using Vagrant to set up multiple VM's to run our own test lab.
Vagrant will set up 3 machines:
- Jenkins server: Jenkins will be used for building the pipeline
- Nexus server: Nexus will be used to download dependencies and building the Artifact
- SonarQube server: SonarQube will test the code and provide us Quality Gates to allow or deny the build.

Other tools;
- Github
- Slacks: Using as a notification system.(Can be replaced with Microsoft teams, emails, etc..

Our workflow:

 <img src="https://i.ibb.co/xmM4vzG/Screenshot-from-2023-01-29-05-46-09.png" alt="Terminal">
 
