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


## Github

We will clone a repository and set it as the working repository. Can replace branch name + links to any repository.

Connect your device to github account:

Open terminal:
```
ssh-keygen

```
This created a public and private key, copy the public key to your github account: account -> settings -> ssh and gpg keys -> new ssh key -> create key and post public key. 

Run:
``` 
ssh -T git@github.com
```
Now create a folder for the repository, and now the migration part:

```
git clone -b ci-jenkins https://github.com/DorBitton/vprociproject.git (this is the url of the repository you wish to clone)

cd *foldername

git remote set-url origin git@github.com:DorBitton/vprociproject.git (this is the url of the repository you wish to clone into)

git branch -c main

git checkout main

git checkout ci-jenkins

git push --all origin

git config --global user.email "youremail@example.com"

git config --global user.name "yourUserName"
```
It should be in sync now and we are able to push code into github. 
