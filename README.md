## Continuous Integration using Jenkins, Nexus, Sonarqube &amp; Slack.

In this project I will try to demonstrate a production enviroment pipeline for continuous integration using the following:
* Github repositry: Code managment for developers
* Jenkins: For building the pipeline
* Nexus: For building the Artifact
* SonarQube: For code testing
* Slack: Will be used as a notification system for build results

Our workflow:

 <img src="https://i.ibb.co/xmM4vzG/Screenshot-from-2023-01-29-05-46-09.png" alt="Terminal">
 
 
 Developer will make code changes using an IDE that is connected to a Git repository.
 Github stores the code changes. When Github code changes - Jenkins will fetch the changes. (Integration with Github)
 Jenkins will run code tests and will publish the results on SonarQube server. (We can also add Quality gate tests to the code)
 Once code analysis is done, Maven will build the artifact. (why Maven:Using Java code for an example)
