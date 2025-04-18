
# TIPS
```python
use git bash then make aliases for commands.
```



# Add token to existing repository
```python
1. go to github profile
2. click developer setting
3. add token
4. check the main checkbox
5. generate a token
6. clone the repo of your github
7. set url_name and can be custom:
		- git remote add "custom_url_name" <url_of_repo> 

	the default name of the url when git pushing and for set-url is "origin":
		- git push origin <branch_name>

8. type "git remote set-url <url_name> https://<token>@github.com/<username>/<repo>"
9. set this:
	git config <options> user.name <username>
	git config <options> user.email <email>
```



# Update a new token
```python
1. unset the previous token:
	git config --global --unset credential.helper (Linux)

2. generate new token from setting/developer/personal access token > tokens > <repo name>/generate token

3. see the shortcut repo name:
	git remote -v

4. update the token:
	git remote set-url <shortcut repo_name given from "git remote -v"> https://<new_token_here>@github.com/<username>/<repo_name>

	ex:
		git remote set-url sec https://ghp_IA98tiP1vfJitIV1chgZi3zyD6nHhYn7tu43@github.com/ariel-canoy/cybersecurity
	



```



# Commands
```bash
git config <options> user.name <username>
git config <options> user.email <email>
	- add username and email to track a person who commit the changes.
	- if "--global" is not included then only the current folder will affected by the configuration.

	options:
		--global - configure all the folders to be that name and email




>> git init
	- create an empty Git repository or reinitialize an existing one. 

>> git add .
	- add all the untracked files and folders to the .git folder.

>> git commit -m "description of changes"
	- commit or add the all the folders and files from .git folder to the reposity.

>> git restore --stage <filename> or .
	- revert the filename or directory committed before.
	- it will remove the filename or directory from the staging area.

>> git rm --cached <filename>
	- remove the file or entire folder that is added to the staging folder (.git). 

>> git log <options>
	- track the log of commit
	- it will show the latest commit from the top to bottom

	options:
		--oneline - shorter version of log information.



------------- UNDOING COMMITS -------------

>> Checkout
	- change the head or the current progress of the project. You can go to previous commit repository.
	command:
		git checkout <hashed>
			- go to that changes after commit.
			- go to that state.

>> Revert
	- get another copy of specific previously committed and make changes then commit again. It will make another log commit.
	command:
		git revert <hashed>
			- go to that changes before commit.
			- go to that before that state.

>> Remove
	- remove all the committed files and folders until it goes back to specific committed





------------- BRANCHING -------------

>> git branch 
	- show all branches

>> git branch <branch name>
	- create new branch

>> git branch -b <branch name>
	- create and switch to that new branch

>> git checkout <branch name>
	- switch to specific branch

>> git branch -d <branch name>
	- delete specific branch
	- user should be outside the branch to delete that branch




------------- MERGING BRANCH -------------
note:
	- before doing "git merge <branch name>", make sure that you are in the main branch or any branch you want to put your another branch. 

>> git merge <branch name>
	- merge the branch to the master/main branch


```




# GitHub

Note:
You will use authentication token that will generate from profile>setting>developer>token(classic)>generate token>click repo>generate>copy before reloading the page.

```python


>> git remote add <name of url repository> <url of repo>
	- ex. "git remote add repo https://github.com/myusername/repository"
	- add shortcut for "git push <url repo>" 
	- now you can use "git push -u <name of url repo> <branch to push to github>"

>> git push <url of repo>/(-u <shortcut name for url repo>) <branch name to push to github>
	- push or send the specific latest branch commits to github




```









