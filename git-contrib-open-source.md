# How to contribute to open source projects
###### Source: https://www.dataschool.io/how-to-contribute-on-github/ (Contains nice pictures)

**Naming conventions:**
* repo: repository
* main repo: the project (source) you are trying to contribute to
* fork: your copy of the main repo on the server
* local: your machine repo
* origin: your fork on the server
* upstream: main repo

**Steps:**
1. Create a fork in your server account\
	You will have to "pull" to sync with main repo if fork is old 
2. Crate a branch with an appropriate name
3. Make required changes
4. Push branch to your fork
5. Create PR

**Details with commands:**
1. Create a account on the server if you dont have one and login to it
2. Now you will see an option to fork the project repo on the git server in your account. Click on "**Fork**" button.
3. Clone your fork to your machine `git clone URL_OF_FORK`\
	To check that your fork is the "origin" remote `git remote -v` or add it with `git remote add origin <URL_OF_FORK>`
4. Add the main repo as the "upstream" remote `git remote add upstream <URL_OF_PROJECT>`\
	To check if remote is added `git remote -v`
5. Pull the latest changes from upstream into your local repo `git pull upstream master`
6. Create a new branch `git checkout -b BRANCH_NAME`
	To check all available branches on your local `git branch`\
7. Make changes in your local repo
8. Stage your changed files `git add -A`
9. Commit your changes, one commit per issue and properly comment `git commit -m <DESCRIPTION OF CHANGE>"`
10. Push your changes to your fork `git push origin BRANCH_NAME`
11. Begin the pull request (Go to the webpage of your fork and select the pushed branch which will let you create a pull request)
12. Create the pull request (from your head repo (your fork) to base repo (main repo), read contribution guideline and include issue numbers if related)
13. Review the pull request (If the project maintainer requires additional action, if yes do the following:)
	1. Checkout the branch in your local repo `git checkout <BRANCH_NAME>`
	2. Make changes, stage, commit and push (steps 7 - 10) this should add the new commit to the pull request automatically
	3. Add additional notes to the pull request and close the discussion (on github this is "Resolve conversation")
14. Once pull request is merged into upstream delete the branch by:
	1. First switch to master `git checkout master`
	2. Delelte the branch `git branch -D <BRANCH_NAME>`
16. If required synchronize your fork with the project repository `git pull upstream master && git push origin master`
