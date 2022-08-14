If you developed your project without git and need to push it into a remote GitHub repository, follow the following steps to upload it one push at a time:

1. Find the location of your project.
   If you can't find it, check in your local web server directory, like in the following directories:

For windows users:
   - `C:\xampp\htdocs` (XAMPP)
   - `C:\wamp\www` (WAMP)

For GNU/linux users:
   - `/opt/lampp/htdocs` (XAMPP)
   - `/var/www` 

> If you are  using other local servers (tomcat,...), check the corresponding folders

2. Follow the git setup from [Git & Github Quickstart.md](https://github.com/AEENI-UF/guides-and-tutorials/blob/main/Git%20%26%20Github%20Quickstart.md) if you haven't done yet.

3. Change directory to the root location of your project
   > eg:  cd /opt/lampp/htdocs/cocotte-minutte-wordpress

```execute
$ cd /path/to/your/project
```

4. Init a local git repository
   
```execute
$ git init
```

5. Go to your GitHub repository and copy its HTTPS url.
   > eg:  https://github.com/AEENI-UF/devhunt-edition-1-cocotte-minute.git
   
6. Add your remote repository. 
   > eg: git remote add origin https://github.com/AEENI-UF/devhunt-edition-1-cocotte-minute.git
   
```execute
$ git remote add origin https://github.com/AEENI-UF/devhunt-edition-1-YOURREPONAME.git
```
   
7. Pull from your remote repository

```execute
$ git pull origin main
```

8. Set up the current branch to track `origin/main`
   
```execute
$ git branch -u origin/main
```

9. Add your files to the staging area.
   
```execute
$ git add .
```

If your are on linux and encounter fatal error like `fatal: CRLF would be replaced by LF in ...` , temporarily disable autocrlf:

```execute
$ git config --global core.autocrlf false

$ git add .

$ git config --global core.autocrlf input
```

10. Commit your files to HEAD

```execute
$ git commit -m "Your message here"
```

11. Push your files to the remote repository

```execute
$ git push origin main
```

12. If there are no errors, you can now check your remote repository at `https://github.com/AEENI-UF/devhunt-edition-1-YOURREPONAME`, your files should be there.
