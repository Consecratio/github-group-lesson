# Github Workflows

## What is a Github Workflow? 

How can we have multiple people contributing to the same software project while working as a distributed team?

We've already been using the answer - it is the same system we use to submit homework via Github. 


![Example of Group Github. Credit: Coderefinery](https://coderefinery.github.io/git-collaborative/img/forking/forking-overview.svg)

The image above illustrates an exmaple "forking" based Github workflow. 

In this style of workflow:
- One user initializes and owns a central repository
- Each invidual working on the project forks that initial repo
- Each individual then clones that forked repo to their local machine
- As commits happen, they are pushed up to the forked repository. 
- For these new changes to be added to the central repository code, workers submit pull requests from their forked repositories. The central owner approves or edits these pull requests. 


The only difference between this system and how we have been submitting homeworks is the following: 
1. We do not accept your pull requests, thus merging your code into the assignment repos. 
2. If we ever update the class repos, you never update your forked versions. 


Number two is where the magic of Github comes in. 

In order to update a forked repo to the most recent version of a central repository it was forked from, we just have to run `git pull`. This will "pull" any updates from central repository so you can see what cool things your teamates have contributed to the project!

Often times, in order for the pull request to initially work we have to explicitly tell our local repository where to find this central hub. Lucky for us this process, formally known as setting an upstream branch, has been simplified by Git/Github. **The first time you run `git pull` you will get an error. Run the command to set upstream passed to you in the error message to resolve!* 

---
## Thinking in Github Terms

This process, distilled into Git commands is the following: 

*Central Repository/Project Owner:*
- Creates a repository, either locally or on Github. 
- **Add a `.gitignore` at this stage to prevent issues down the line.**

![Github personal workflow example. Credit: Coderefinery](https://coderefinery.github.io/git-collaborative/img/forking/forking-3.svg)

*Project Worker:*
- Forks on Github the central repository. 
- Runs `git clone forked-repository-url` on their work machine. 
- Works on the project/a feature, making git commits as they progress (using `git add` and `git commit`). 
- Once ready to have project owner review code, runs `git push`. This sends current version of repo up to forked repo. 
- On forked repo creates a pull request to compare new code to original repository. 
- When the central repository owner announces updates/changes, run `git pull` locally to update personal repository. 
*Note: you might run into merge conflicts, even at this stage!*

---
## Mini Lab: Merge Conflicts and Pull Updates

We will all be contributing to the same main repository with just a README.md.

*Steps to Achieve:*

- Appoint a "main github human" and have them create a repository on Github with a README. 
- Have everyone in your group fork this repository. 
- After forking, `git clone` the repo to your computer. Next, we need to set the *original repo* as the remote repo.
- Run `git remote add upstream original_repo_url_here`. 
- Edit the README.md file by adding a picture of your favorite animal. 
- `git add .` and `git commit -m "your message"` your work. Then run `git push`. 
- On Github, go ahead and submit a pull request to the central repository. 
- Watch as your main github human fixes merge conflicts, and approves, a few pull requests. Once they are done, run `git pull upstream branch_name`. *Use the full command `git pull upstream branch_name` each time you run the command (as a heads up).*

**What does the README.md now look like on your local machine?**





