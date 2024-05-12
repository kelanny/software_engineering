# How to pull all Branches of a Git Repository
Git branches can be stored in a remote or local repository. When you want to work on a feature from a branch stored in a remote repository, you must download it to the local repository first.

The two Git commands used to download content from a remote repository are [git pull](https://phoenixnap.com/kb/how-to-use-git#ftoc-heading-19) and **`git fetch`**:

- **`git fetch`** is the safer version of **`git pull`**. It downloads the remote content without updating the local repository's working state, which means your work remains intact.
- **`git pull`** is more aggressive because it downloads the content from the remote repository and executes [git merge](https://phoenixnap.com/kb/how-to-use-git#ftoc-heading-16) on the local active branch. The merge creates a new merge commit and integrates the content with your work. However, merging content like that can cause conflicts with work in progress, and it may require manual resolution.

### The sections below show how to pull all Git branches to a local repository using the two commands.
With **`git fetch`**, you can download metadata from the remote repository without affecting your local work. It is a useful option when you want to check if another developer has made any changes in the remote repository. **`git fetch`** is also used when [cloning a repository](https://phoenixnap.com/kb/git-clone-submodule) and downloading the data to a local machine.

The **`git fetch`** command retrieves the latest updates from the remote repository. Depending on whether you want to download metadata for individual branches or all branches, the command has the following variations:

1. - The command fetches only the specified branch from the remote repository.
	```
	git fetch <remote> <branch>
	```
2.  - A command is considered a power move since it fetches all the registered remotes and their branches.
	```
	git fetch --all
	```


 ### Steps to follow to clone a git repository with all its branch
 1.  Clone the git repository
		```
		git clone <URL>
		```
	
2. After cloning the repository, check the branches available in the local and remote repositories. 
	- To check the local branches, run:
		```
		git branch
		```
	-  To check  remotely available branches by running:
		```
		git branch -r
		```

3.  Fetch the metadata for remote branches and start tracking them.
	- The **`--all`** flag tells Git to fetch the metadata for all the branches in the repository.
	```
	git fetch --all
	```

4.  After fetching the metadata, start tracking the branches with the following command:
	```
	git branch -r | grep -v '\->' | sed "s,\x1B\[[0-9;]*[a-zA-Z],,g" | while read remote; do git branch --track "${remote#origin/}" "$remote"; done
	```
	- The command sets up the branches in the local repository and makes them track their counterparts in the remote repository.
	