---
title: "GitHub Info"
date: 2018-12-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
draft: false
# search related keywords
keywords: ["induct", "instate"]
---
This module is a guide for details and usage of GitHub. If you are a newbie especially coding beginners and get to know what it is. 

## Install git 
We can start to install git by running a command in Konsole:
```
pi -S git
```

{{< notice note >}}
Make sure you have already run the command `pi -Syu` to update your system.
{{< /notice >}}

---

## Clone an existing repository
If you want to clone your existing repository or you clone other people's repository, you run the command below:
```
git clone [url] 
```

{{< notice info >}}
**Url** is address of world wide web page.
{{< /notice >}}

---
## Initialize new version controlled project
In order, to create a new controlled project you have to run this command:
```
git init
```

---
## Save changes to the repository
As you have already build your project, you can make changes  in it.
```
git add .
git commit -m " message "
```
{{< notice info >}}
The Words in "... ". After you push the changes to the git, the directory that change will appear the words in "...".
{{< /notice >}}

---
## State the current state of the repository
If you want to state where repository you are working on, do this:
```
git status
```

---
## Create a new branch
On Github, we can create branches on the same repository if you do not want to use as a master. To create a branch:
```
git branch [branchName]
```

---
## List all remote or local branches
If you want all show all the branches that work on the repository.
```
git branch -a
```

---
## Delete branch
If you wish to remove the branch, you can do it by run:
```
git branch -d [branchName]
```

---
## Merge changes into current branch
When you are working as a team, you probably work with different branch from the team. So, we can pull the project together with command below:
```
git merge [branchName]
```

---
## Checkout an existing branch
When you want to create new branch, you might want to check out if the branch has already made on the same repository. So that you can create other branches instead.
```
git checkout -b [branchName]
```

In order to create new branch with that name you have to use command below:
```
git checkout -b [newBranch]
```

---
## Create and Delete tag
Git tags are used as reference points in your development workflow. You might want to create new Git tags in order to have a reference to a given release of your software. Creating tag with this:
```
git  tag [tagName]
```
You can delete tag by:
```
git tag -d [tagName]
```

---
## Push tags
If you want to push tags you can run this:
```
git push --tags
```

--
## Get the lastest version of the repository
In order to get the data of last updated on repository, type this in konsole:
```
git pull [branchName] [remoteURl/remoteName]
```

---
## Add remote repository
we can also remote on the git repository with this command line:
```
git remote add origin [url]
```

---
## Define the author name to be used for all commits
On git we can define the author name on all the commit use on repository:
```
git config --global user. name [name]
```

---
## Define the author email to be used for all commits
On git we can also define the author email on all the commit use on repository:
```
git config --global user. email [email]
```

---
## Helpful guides that come with git
```
git help -g
```

---
## Undo the previous commit
If you wish to revert previous commit, you can do it with this:
```
git revert HEAD^
```
## Forget about files that were tracked but are now in .gitignore
Here are those commands:
```
git rm -r --cached .
git add .
git commit -am " message "
```

---
## Send local commits to the remote repository
We can send as branch commits to the remote repository by:
```
git push [remoteURL/remoteName] [branch]
```

---
## Store current work with untracked files
If you want your file to be untrackable you can do it with:
```
git stash -u
```

---
## How to bring stashed work back to the working directory
You can also bring back all the untracked files back to working directory, too.
```
git stash pop
```

---
## Remove a file or a directory from the working index

you can remove the file from cached.
```
git rm --cached [fileName]
```


In order to remove the directory:
```
git rm -r --cached [directoryName]
```

---
## Delete a file or directory(force)
If you cant delete the file you can force it with this:
```
git rm -f [fileName]
```
Forcing delete on directory:
```
git rm -r -f [directoryname]
```

---
## Delete remote branch 
You can remove the remote branch with only command
```
git push origin :[branchName]
```

----
----
