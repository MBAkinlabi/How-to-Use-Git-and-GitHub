# [Git & GitHub Crash Course For Beginners by Traversy Media](https://www.youtube.com/watch?v=SWYqp7iY_Tc)

- This is a quick course on Git and GitHub
- Git is a Version Control System for tracking changes in computer files (In the case of your code)
- It just stores files. You can use it with any programming language.
- When you use Git, you have a local repository on your local machine (computer). And you can push it to a remote repository (like GitHub or BitBucket). You don't need an internet connection to use it locally. But you need it to push it to a remote repository like GitHub.
- You can also import (or download) from a remote repository.
- Here are the basic commands.
- **$ git init**        // will initialize a local git repository. You never have to touch the .git file that this action will create. As a programmer you shouldn't care about this.
```bash
    $ git init
```
- Once you've initialized git in your project folder. You can then begin to run other commands.
- **$ git add <file>**     // Will add file or files to the staging area. More information about the staging area later to make it ready for commit. More examples later the below shell code to better understand how it works.
```bash
    $ git add
```
- **$ git status**    // If you want to see what you have in the staging area and the status and the differences, this code gives you that. It gives you information you need to know the status of things.
```bash
    $ git status
```
- **$ git commit**    // When you're ready, you can go ahead and commit your files. It'll put everything in the staging area and put it into the local repository. There are also some options with git commit. You'll learn about them later.
```bash
    $ git commit
```
- **$ git push**      // Will take your local repository, which you've just created and push it to your remote repository. Again examples of remote repositories are GitHub and BitBucket. You'll have to add a bit more information like your credentials and the name of your repository. Don't worry, we'll talk about them in the examples you'll come across later below. You can also create ssh keys so that you won't have to add username and password.
   ```bash
    $ git push
```
- **$ git pull**   // If you want to pull the latest changes from the remote repository, you can just do git pull. So, you have the files already, you just want to pull in the latest changes. That's when you use this.
```bash
    $ git pull
```
- **$ git clone**    // If you want to clone a repository into a new directory on your local machine, you use git clone. Clone anything like a project or module (library) you like. Anything available publicly. And maybe for free.
```bash
    $ git clone 
```
 - Installing git is simple.
- **If you're Linux (Debian) do this:**
```bash
    $ sudo apt-get install git
```
- **If you're on Linux (Fedora) do this:**
```bash
    $ sudo yum install git
```
- **If you're on Mac, go to this site** [https://git-scm.com/downloads](https://git-scm.com/downloads) and download for Mac: [https://git-scm.com/download/mac](https://git-scm.com/download/mac)
- **If you're on Windows, go to this site** [https://git-scm.com/downloads](https://git-scm.com/downloads) and download for Windows: [https://git-scm.com/download/win](https://git-scm.com/download/win)
- **I should note that, you can download for Linux/Unix on the this site** [https://git-scm.com/downloads](https://git-scm.com/downloads) and link: [https://git-scm.com/download/linux](https://git-scm.com/download/linux)
- Downloading here for windows come with Git Bash, which is highly recommended.
- Running on Windows simple steps below:
- **While installing, you'll see the part that says Adjusting your PATH environment.**
- Choose the last one, which should be "Use Git and optional Unix tools from the Windows Command Prompt"
- **The next should be Configuring the line ending conversions:**
- Choose "Checkout Windows-style, commit Unix-style line endings"
- **The next should be "Configuring the terminal emulator to use with Git Bash"**
- Choose "Use MinTTY (the default terminal of MSYS2)
- **The next should be "Configuring extra options"**
- Choose "Enable file system caching" and "Enable Git Credential Manager"
- **In the next, you may be asked to use one experimental tool, Don't select it. Just install.**
- When installation is completed, just launch Git Bash.
- Author recommend Git Bash over Windows command line. So use Git Bash alone for git.
- Type this to check your git version.
```bash
    $ git --version
```
- You'll see the version you have. Make sure it's the latest.
- When you have Git Bash, you can go directly to the folder you want on normal windows and right click. You'll see "**Git Bash Here**."

![Opening Git Bash from a folder using File Explorer](/assets/git-bash-here.png "Opening Git Bash of a folder")

- It'll open Git Bash there. Easy.
- You can open the location of your project in the File Explorer.
- Use **git init** to initialize git in your project or project folder.
```bash
    $ git init
```
- It'll create a .git folder in your project.
- You may not be able to see in the File Explorer or code editor folder.
- If you're not seeing it, go back to the File Explorer.
- You'll see "View" at the top-left of the File Explorer (assuming that you're in Windows of course)
- Then go to "Options"
- Then click "Change folder and search options"
- Once it has opened, click "View" which is located at the top again.
- Inside "Advanced settings" and Under "Hidden files and folders," check "Show hidden files, folders, and drives"
- And make sure "Hide extensions for know file types" is unchecked."
- Click "Apply" and "Ok"
- Don't worry about the stuff in the .git folder.
- The next thing to do is set up your username and name for git.
- Inside Git Bash, type this:
- **$ git config —global [user.name](http://user.name) 'My Name"**
```bash
    git config --global user.name 'My Name'
```
- **$ git config —global [user.email](http://user.email) 'myemail@email.com**
```bash
    git config --global user.email 'myemail@email.com'
```
- If you want to add a file to staging in git do this:
- **$ git add index.html**
```bash
    git add index.html
```
- The above will add the index.html file to staging, which means part of the files you want to start watching or tracking for changes. The files that are edited or ready or anything.
- If you want to check files that are in the staging area (There for tracking for changes), use the below:
- **$ git status**
```bash
    git status
```
- This will give you information about your files.
- If you want to remove a file from the staging area, do this:
- **$ git rm —cached index.html**
```bash
    git rm --cached index.html
```
- Doing the above will remove the file index.html from the staging area.
- If you do git status after removing a file, you'll see that it is now untracked.
- There are different ways to add files to the staging area in git.
- **$ git add *.html** (will add all files that ended with .html)
```bash
    $ git add *.html
```
- If you want to add every file in your project, do the below:
- **$ git add .**
```bash
    $ git add .
```
- Now, if you do **git status**, you'll see that all files are added.
- If you make changes to a file, you need to add it again to the staging area. Make sure you add a file or files after making an edit (or simply writing more code in your project).
- You should always use **git status** to double check that all files have been added to the staging area.
- If you're done making a changes, it's time to commit it. It means it's done and you want to ensure that it's now saved. That's what git commit does. So to commit a project, use this:
- **$ git commit**
```bash
    git commit
```
- When you do a git commit, it'll take you to a place where you'll be asked to write some comments.
- If you type, you won't see anything. Click "I" on your keyboard to go into insert, which you'll see at the bottom. Then you can start writing your comments.
- Anything that has the "**#**" sign in front is treated as a comment. You must write on an area without the **"#**" sign. Or you can remove an "#" sign in one of the comment already there.
- **To get out of the comment mode, type escape and type ":wq" and press enter.**
- Now, you'll see that your files have been commited.
- **You can avoid going to the place where you need to type escape and ":wq" and enter to get out of.**
- To do that, just write this when next you want to commit:
- **$ git commit -m "This is where your commit message goes. I changed app.js for example"**
```bash
    git commit -m "I changed my login form page"
```
- You just included the comment and skipped that whole editing page. You included the comment within that commit.
- Now, let's talk about gitignore. It's the file that you add the files and folders that you don't want to include in your  repository or tracking at all to transfer to GitHub. So, if you do "git add ." it's not going to add these files you want to ignore.
- Create a file called .gitignore in your main project folder. You can do that inside your code editor.
- Go to .gitignore and add the file you want to ignore. Each file/folder you want to ignore should be on one line. Add the first at the beginning. The second one will have to be under the first and so on.
- If you now type "**git add .**" it won't add the file you want to ignore. You can type "**git status**" to view the status.
- If you want to ignore a whole directory/folder, you can add it like this "/directory1" to the **.gitignore** file.
- If you want to ignore all files of an extension, you can write ***.txt** and it'll add a txt files to be ignored.
- Let's talk about **branches.**
- If you're part of a team, you don't want to be working on a functionality for your app, and suddenly, someone change something in other files or folders that affects your code.
- That's why you need to create a branch. If you're working on a login form, for example, you can name your branch "log in form" branch. It's not part of the master. You test everything in this branch. When you're done and you know the functionality is working perfectly. Then you can move it to the master branch. If there's a change in the master branch that affects your log in form functionality, you can easily point that out and report to your boss.
- To create a branch, write this:
- **$ git branch login**
```bash
    git branch login
```
- login is the name of the new branch you just created. Just writing the above code won't automatically take you to the new branch.
- Always commit before you switch branches.
- To enter a branch, write this:
- **$ git checkout login**
```bash
    git checkout login
```
- Remember that "login" is the name of the branch.
- Now, you should be in the "login" branch after typing the above code.
- So, you can create a new file while you're inside this new branch.
- You can do anything inside your code editor when you're inside the branch.
- You can do **"git add ."** and **"git commit -m "login form"**
- If you switch to the master branch by writing **"git checkout master"** you'll notice that your new files and changes made while inside the "login" branch will be gone.
- If you want to merge the "login" branch with master, you'll have to write this while inside the master branch:
- **$ git merge login**
```bash
    git merge login
```
- Now, it'll merge the login branch with the master. And files created while in the login branch will now be visible.
- You'll have to write a comment about why the merge is necessary. Press "I" on the keyword to insert. Then press the "escape" key on the keyboard and ":wq" to get out of it.
- Now, let's work with a remote repository like GitHub.
- Create a new repository on the GitHub site. Of course, give it a name.
- After completing creating the repository, it'll take you to a page that shows you different ways to set it up.
- You just need to add the remote repository you want.
- First type "**$ git remote"**
```bash
    git remote
```
- Then copy and paste the "**git remote add origin ......"** line.
- You should be able to add it like that.
- After adding that, type "**git remote**" again.
- And now it should return origin in Git Bash.
- Now copy and paste something like "**git push -u origin master"**
- And that should push to that repository.
- You may have to login to your account while doing this.
- You should bush and be done.
- Once you reload on GitHub, you should see your files loaded on that url.
- Make sure you always add a [README.md](http://readme.md) along with your project.
- Now, if you want to push to GitHub again, all you have to do is type **"git push"** and it'll push it to the repository.
- So, if you want to get a project (library or framework) or file or code on github, all you have to do is go to the project url on github and you'll see the **"Clone or download link"** at the top-right of the site. You can clone with HTTPS.
- Copy the URL.
- Create a folder for the project you want to clone on your computer.
- Then right click and select "Git Bash here" You'll open to the folder straight on Git Bash.
- All you have to do is write this:
- **$ git clone andtheurlyoucopiedhere**
```bash
    git clone https.......
```
- You should get everything to that folder.
- You can clone anybody's project as long as it's available on GitHub.
- If a lot of developers are working on a project, you can just pull it to get the latest update of the project or file.
- Write this to pull to get the latest update:
- **$ git pull**
```bash
    git pull
```
- You pull the master of course, if that's what your team is working on.