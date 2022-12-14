A simple, practical and straightforward guide to getting started using git and github. A sample use case for **AEENI DevHunt edition 1**.



# 1. Setup

> Note: command-line snippets should be run or executed without the $ sign on your favorite terminal/shell (cmd, bash, powershell...)

## 1.1 Installation
[Download and Install git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) on your OS.
If you are on windows, you may want to choose Git Bash to use bash shell features.

You can check if the installation was successful by running:

```execute
$ git --version
```

## 1.2 Create a GitHub account
In order to use Git with GitHub, you need first to [create a GitHub account](https://github.com/join)

## 1.3 Configuration
### 1.2.1 Name and Email

For new git users only, let git know your username and email.
Open a terminal and excecute:

```execute
$ git config --global user.name "YourUsername"

$ git config --global user.email "your_email@whatever.com"
```

### 1.2.2 Line ending preferences

Collaborators using different OS's need to use the same preference for line ending to prevent conflicts:

For Unix/Mac users:

```execute
$ git config --global core.autocrlf input

$ git config --global core.safecrlf true
```

And for Windows users:

```execute
$ git config --global core.autocrlf true

$ git config --global core.safecrlf true
```

### 1.2.3 Default initial branch name

Use `main` instead of `master` as the default initial branch name to follow the new convention.

```execute
$ git config --global init.defaultBranch main
```

# 2. Authentication
When you connect to a GitHub repository from Git, you will need to authenticate with GitHub using either HTTPS or SSH.

## 2.1 Connecting over HTTPS (recommended)
You can authenticate manually or use a credential helper to automate and facilitate authentications.

### 2.1.1 Authenticating manually
1. [Create your Personnal Access Token (PAT)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)
2. When git asks for your GitHub username and password, use your created PAT as your password.

### 2.1.2 Authenticating via a credential helper (caching)
Caching credentials will facilitate your authentications to GitHub by remembering (or caching) your credentials. You can use GitHub CLI, GCM, or other credential managers.

#### 2.1.2.a GitHub CLI
1. [Install GiHub CLI](https://github.com/cli/cli#installation) on your OS. 
   Alternatively,  instead of using package managers, you can directly install its [binaries](https://github.com/cli/cli/releases/tag/v2.14.3) : .msi for Windows, .deb, .rpm ... for other platforms.
   
2. In the command line, execute:
   
```execute
   $ gh auth login
```

3. , then follow the prompts.

-   When prompted for your preferred protocol for Git operations, select `HTTPS`.
-   When asked if you would like to authenticate to Git with your GitHub credentials, enter `Y`.
  
  <img src="./img/GitHub CLI.png"/>
![[GitHub CLI.png]]


# 3. Teams and repositories
## 3.1 Join the organization
After registering the team to participate to DevHunt, all team members will receive an email invitation allowing them to join the [AEENI-UF organization](https://github.com/AEENI-UF). 

<img src="./img/Email invitation.png"/>
![[Email invitation.png]]

Click the join button and you will be redirected to github:

<img src="./img/GitHub invitation.png"/>
![[GitHub invitation.png]]

Once joined, you will be able to see and create repositories on the organization. You will  also be able to join or create teams and subteams.

<img src="./img/AEENI-UF.png"/>
![[AEENI-UF.png]]


## 3.2 Team leader tasks

For now, the **team leader** should :
1. [Create a visible subteam](https://github.com/orgs/AEENI-UF/new-team)  inside the organization for your team, under the `devhunt-edition-1-teams` (the parent team):

<img src="./img/New team.png"/>
![[New team.png]]

Then, it will be pending until approved to become a child of the `devhunt-edition-1-teams` :

<img src="./img/Pending team.png"/>
![[Pending team.png]]

2. [Create a repository](https://github.com/organizations/AEENI-UF/repositories/new) for your project. Use the prefix `devhunt-edition-1-` before your repos name.  It should have a README.md file that describes how to install and use your project.
   
   > Eg:  devhunt-edition-1-cocotte-minute
   
   <img src="./img/New Repository.png"/>
![[New Repository.png]]

3. Go to your team's page at `https://github.com/orgs/AEENI-UF/teams/YOURTEAMNAME/repositories`,  and add your repository
   > eg: https://github.com/orgs/AEENI-UF/teams/cocotte-minute/repositories

<img src="./img/Team repo.png"/>
![[Team repo.png]]

Click the Add repository button and enter the name of the repository you created earlier.
> eg: AEENI-UF/devhunt-edition-1-cocotte-minute

<img src="./img/Add repo to team.png"/>
![[Add repo to team.png]]

Then you should now see it in your team's repos

<img src="./img/Repo added to team.png"/>
![[Repo added to team.png]]

4. Add Write permission to the repo for the team

<img src="./img/Add write permission to repo.png"/>
![[Add write permission to repo.png]]

Now, your team's repository is ready. You can visit the repo by clicking the link of the repo, or go directly to the link `https://github.com/AEENI-UF/devhunt-edition-1-YOURREPONAME`

5. Add each team members to the created team. Follow the link `https://github.com/orgs/AEENI-UF/teams/YOURTEAMNAME/members?add=true`
   >eg: https://github.com/orgs/AEENI-UF/teams/cocotte-minute/members?add=true

<img src="./img/Add team members.png"/>
 ![[Add team members.png]]

## 3.3 Using the repository

### 3.3.1 Get the link to the repository

Go to your repository and copy the HTTPS url to your repo

<img src="./img/Https link.png"/>
![[Https link.png]]

### 3.3.2 Cloning into a local repository

Each collaborators (team members) should now clone the repository into their local machines and work with their local copy.

Change to a directory where you would like to put the local copy:

```execute
$ cd /path/to/myprojects
```

Clone the repository using the SSH url copied earlier:

```execute
$ git clone https://github.com/AEENI-UF/devhunt-edition-1-YOURREPONAME.git
```

> eg: git clone https://github.com/AEENI-UF/devhunt-edition-1-cocotte-minute.git

<img src="./img/Git clone.png"/>
![[Git clone.png]]

A new folder containing the project will be created, it is called the `working directory` . Change directory to that folder:

```execute
$ cd devhunt-edition-1-YOURREPONAME
```

> eg: cd devhunt-edition-1-cocotte-minute

If you list its content, there should exist one folder `.git` and a `README.md` file.

<img src="./img/List first.png"/>
![[List first.png]]


### 3.3.3 Open the project in your IDE
You can open the project in your IDE or source code editor. (VSCode, Atom, Eclipse,...) 

## 3.4 Developing the project

It's time to develop our project. Each time we finish a functionnality in our project, we should upload (push) the modifications to our remote repository so that the other collaborators can download (pull) them. 

3.4.1 The git workflow

The workflow: we have to repeat the following actions each time we want to update our project:

1.  Create or modify files (css, html, js, py, java, img, ....)
2.  Add modifications into the staging area.
3. ...


<img src="./img/Git workflow.png"/>
![[Git workflow.png]]
***Source: https://en.wikibooks.org/wiki/File:Git_data_flow.png

Anywhere in the workflow, you can always check the status of your files using:

```execute
$ git status
```

- **Working directory or working tree:** This is where your files reside and where you can edit and develop your project. When you have done editing some files, you need first to add or prepare them to the *staging area*. 
  You can add them either once together or specifically.

To add them once for all, execute the following inside the root folder of your project:

```execute
$ git add .  
```

To add them specifically, list your edited files after the add command.

Example:
```execute
$ git add yourFile1.txt yourFile2.css
```

- **Staging area or index:** This is a location containing your prepared files. `.git/index` contains paths and `.git/objects` contains file contents. You should always use git commands to add or remove files from there, and not manually.
  When you have finished adding the files you want to prepare, you can commit them to the *local repository* with a description (message, reason or comment) of your commit:

```execute
$ git commit -m "Put the description of your commit here"
```

- **Local repository:** This is a repository that resides on your local machine. When you commited your files from the staging area, they will reside at the current active branch, pointed by a pointer called **HEAD**, and that points to the last commit on that branch. 
  You can now push or upload your files to your remote repository (your GitHub repository):

```execute
$ git push
```

To get updates from the remote repository, 



# ------------ IN PROGRESS ... -----------


# Useful Links
 
[GitHub docs](https://docs.github.com/en)

[GitHub CLI](https://cli.github.com/)