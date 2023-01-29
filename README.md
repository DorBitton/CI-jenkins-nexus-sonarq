## Continuous Integration using Jenkins, Nexus, Sonarqube &amp; Slack.

In this project we will be using Vagrant to set up multiple VM's to run our own test lab.
Vagrant will set up three machines:
- Jenkins server: Jenkins will be used for building the pipeline
- Nexus server: Nexus will be used to download dependencies and building the Artifact
- SonarQube server: SonarQube will test the code and provide us Quality Gates to allow or deny the build.

Other tools;
- Github
- Slacks: Using as a notification system.(Can be replaced with Microsoft teams, emails, etc..

Our workflow:

 <img src="https://i.ibb.co/xmM4vzG/Screenshot-from-2023-01-29-05-46-09.png" alt="Terminal">
 


## Vagrant

In our <a href="https://github.com/DorBitton/CI-jenkins-nexus-sonarq/tree/main/Vagrant%20Files">Vagrant</a>
 folder we can find how to Install Vagrant. After installed, download the Vagrant File and open a Terminal in that location:
```
Vagrant up
```
Will set up our three servers automaticly with static internal IPS. (We might get an error regarding IP range invalid, just adjust the IP accordingly)
