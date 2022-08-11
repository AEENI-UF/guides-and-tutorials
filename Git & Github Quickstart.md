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
  
![[GitHub CLI.png]]


# 3. Teams
## 3.1 Join the organization
After registering the team to participate to DevHunt, team members will receive an email invitation allowing him/her to join the [AEENI-UF organization](https://github.com/AEENI-UF). 

<img src="./img/Pending team.png"/>

![]("img/")

![[Email invitation.png]]

Click the join button and you will be redirected to github:

![[GitHub invitation.png]]

Once joined, you will be able to see and create repositories on the organization. You will be able to join or create teams and subteams also.

![[AEENI-UF.png]]


## 3.2 Team leader tasks

For now, the **team leader** should :
1. [Create a visible subteam](https://github.com/orgs/AEENI-UF/new-team)  inside the organization for their team, under the `devhunt-edition-1-teams` (the parent team):


![[New team.png]]

Then, it will be pending until approved to become a child of the `devhunt-edition-1-teams` :

![[Pending team.png]]

2. [Create a repository](https://github.com/organizations/AEENI-UF/repositories/new) for their project. Use the prefix `devhunt-edition-1-` before your repos name.  It should have a README.md file that describes how to install and use their project.
   
   > Eg:  devhunt-edition-1-cocotte-minute
   
![[Pasted image 20220810224801.png]]



**



# 3. Repositories






# Useful Links
 
[GitHub docs](https://docs.github.com/en)
[GitHub CLI](https://cli.github.com/)