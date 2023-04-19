# Git* for researchers tips and tricks

... a beginning

![image](https://user-images.githubusercontent.com/32324155/233045375-67648e11-44fc-46f8-bd28-e3b4affe9344.png)
https://xkcd.com/1597/

---

# What is version control and why should I care?

* snapshot, roll-back functionality
* branching
* collaboration, merging
* reproducibility

<img src="https://user-images.githubusercontent.com/32324155/233046924-ac11b227-ba4f-4814-9181-29ad5469b099.png" width="30%" />


* not just code

see also: [CodeRefinery git motivation](https://coderefinery.github.io/git-intro/motivation/)

---

# Collaboration

<img src="https://user-images.githubusercontent.com/32324155/233045262-cf3a2b1d-affe-44e8-aed9-a8a4774fdf80.png" width="30%" />

https://phdcomics.com/comics/archive.php?comicid=1531 

git - github - gitlab - bitbucket - ...

public - private

<img src="https://user-images.githubusercontent.com/32324155/233041841-6b789e7c-d9cc-4b5e-8135-6c5f382f94f6.png" width="30%" />

`git config --global user.name My Name`

`git config --global user.email y.name@org.fi`

---

# Github suggestions (+-)

-> Collaborating and discussion via pull requests.
-> Suggest in code

Demo time!

---


# Optional: Git clone demo

If we have time, should we demo a cloning a repository? As an alternative to copy-paste code from GitHub web pages. 


---


# This is not a crash course

Check out these awesome materials:

[Coderefinery self-learning material ](https://coderefinery.github.io/git-intro/)

[Coderefinery collabrorative git](https://coderefinery.github.io/git-collaborative/)

[Atlassian tutorials](https://www.atlassian.com/git/tutorials)

[Learn git branching](https://learngitbranching.js.org/)

[Aalto SciComp "git the way you need it"](https://aaltoscicomp.github.io/cheatsheets/git-the-way-you-need-it-cheatsheet.pdf)

Join a community of learners and people happy to help: https://coderefinery.zulipchat.com/ 

---

# Extensions and GUIs

[Github desktop](https://desktop.github.com/)

[VSCode](https://code.visualstudio.com/docs/sourcecontrol/overview) and other IDEs

Jupyter [git](https://github.com/jupyterlab/jupyterlab-git) and [gitplus](https://github.com/ReviewNB/jupyterlab-gitplus), [nbdime](https://github.com/jupyter/nbdime) for notebooks diff and merge , RStudio (eg Tools -> Version control)

---


# collaborative manuscript writing with version control
[Typst for markdown](https://typst.app/)

[Overleaf for LateX](https://www.overleaf.com/)

---

# Why use remote git repository rather than copying files between several own computers/HPC/cloud manually

git takes the guesswork out of it by having commits/branches/tags to pointing to exactly the same things. Git also reduces clutter by getting rid of project_v20_final2_fixedversion.zip type files. If you have the same commit hash / tag on your machine as somewhere else, you have the same content. And tags are cheap, and can even be visualized in various tools. And super easy then to also switch back and forth between different versions.

---

# other useful commands from CSC'ers

* Branches: Branches are very useful to store work that you are not done with yet, but don't want to throw away either. That way you don't have to make a copy of your git repository if you need it for something else. E.g. you're working on a feature so your project is currently broken, but then you want to demo your project, and for that you obviously need a working version. Then you can simply switch to your working branch, and then after the demo switch back to what you were working on. Branches are also the foundation of merge requests / pull requests.
* `git stash`. With stash and stash pop you can store your work and get a clean checkout, and then restore it later. It is like a lightweight branch. Very useful!
* `git archive`. Creates a clean version of your repository without the .git folder and such, can also make .zip straight from it.
* `git blame`. Shows commit information per line for a file of your choice, you get the commit message (e.g. what / why was this line done), who and when it was done. That is very useful for investigating repositories, you get to know if the code is fresh or not, and who you should ask for more information about something from.
* `git rebase -i`. Allows you to move commit(s) around in the repository, useful for incorporating others work in your copy, and cleaning up commits and branches so they're easier to work with for both yourself and your co-workers when they become merge requests. (N.b that git rebase and git rebase -i are very versatile and powerful tools, but thus also quite hard to learn since you can do so much with them. Thus not easy for beginners! 😞 )
* `git tag`. Tags are unique, persistent and immutable pointers to specific important points in your repository. Very good as the foundation for version numbers, as the version numbers can then flow forward to your build process and be used there to giving you a consistent view of what version "1.2.3-beta7" means exactly.
* `git bisect`. If you have an older known working version, and a later broken version, and a lot of commits in between, and you want to find out which version broke your stuff, git bisect is the tool for you. It uses an effective divide and conquer method to let you test version and find the commit that broke your stuff. Can even be scripted!

---



# WIP: Merging
---
# WIP: cherrypicking changes from one branch to another

---
# WIP: git with R

---

# WIP: branches on remotes/local

`git fetch` and `git merge` vs `git pull`

---
