Hello litle ones, I am the Sensai Raul.
My favorite code School path is JavaScript.
 Deadly skills:
*Git
*Javascript
*PHP
*HTML-CSS
*rebase

Mastering GitHub

* Configuration
	$ git config --global color.ui true
	$ git config --global alias.s "status -s"
	$ git config --global alias.lg "log --oneline --decorate --all --graph"

* create a branch named "deadly_skills"

	$ git checkout -b deadly_skills
	$ git push origin deadly_skills

* add and commit the changes locally.

	$ git commit -am "Added deadly skills"

* Push these changes up to the deadly_skills branch on GitHub

	$ git push origin deadly_skills

* Review a pull request
	1-
		** download all branches from github
			$ git fetch
		** view all the branches
			$ git branch -a
		** checkout a local copy of a remote branch
			$ git checkout <branch_name>
		**  test code, make any change and then commit and push changes
			$ git commit
			$ git push
	2-
		** view all the branches 
			$ git branch
		** get all from the server
			$ git pull
		** we can check all the branches and the corrently pointed and then to select the one we can to check
			$ git branch -a
		** checkout a local copy of a remote branch
			$ git checkout <branch_name_to_be_check>
		**  test code, make any change and then commit and push changes
			$ git commit
			$ git push

* Closing Pull Requests by Merging. 
	- Start by getting all changes on GitHub on your master branch:
		dojo_rules (deadly_skills)$ git checkout master
		dojo_rules (master)$ git pull

	- Next, merge in the using the no-ff option.
		dojo_rules (master)$ git merge --no-ff deadly_skills -m "Merging in deadly_skills"

	- Force push it to GitHub:
		dojo_rules (deadly_skills)$ git push

* Creating a Tag --Task : Find the deadly_skills merge commit, checkout it out, create the v1.2.0 tag, and push it to GitHub.
	-Check out master of dojo_rules.

		dojo_rules$ git checkout 

	- Find the commit where deadly_skills was merged.

		dojo_rules$ git log

	- Once you find the SHA-1 of the deadly_skills merge commit, check it out.

		dojo_rules$ git checkout 0248078

	- Add tag v1.2.0 to this revision.

		dojo_rules$ git tag -a v1.2.0 -m "Creating v1.2.0 tag."

	- Finally, push the tag to GitHub using –tags option.

		dojo_rules$ git push origin --tags

* Creating a Release Branch
	Checkout the v1.0.0 tag, use it to create release branch release_branch_1.0, and push to GitHub.

	- First, checkout the tag into a new branch.

		$ git checkout tags/v1.0.0 -b release_branch_1.0

	- Push the release branch up to GitHub.

		$ git push origin release_branch_1.0

	-Tag the fixed commit as v1.0.1, and push the tag up to GitHub.
		-Tag the release.

			git tag -a v1.0.1 -m "Tagging for release."

		-Push to GitHub.

		- Now that you've created the v1.0.1 tag, merge the release branch into master.	
			git push origin --tags
			git merge --no-ff release_branch_1.0 -m "Merge release branch 1.0.1"
			git push origin master

* Deleteing a branch
	-There are two ways to delete the branch both locally and remotely.

    -With the first way, you can use the command line to delete the branch locally, and push the deletion to GitHub

		$ git branch -d release_branch_1.0
    
    -Push the deletion up to GitHub.

		$ git push origin :release_branch_1.0
    
    -Using the second method, you can delete the branch using the GitHub UI, and then run the following command to delete the branch locally:

		$ git branch -D release_branch_1.0


4.2 Working on Issues 

	- Create a new branch named "kill_list" locally.

		$ dojo_rules (master)$ git checkout -b kill_list

	- After that make the changes to the kill list file. Commit them locally including the "fixes #" part in the message. For this example, we'll use the issue number 1.

		$ dojo_rules (kill_list)$ git commit -am "Added repos without readmes. fixes #1"

	- Lastly, you'll need to push this up to GitHub on the kill_list branch there. Our git upsteam is set to "master" though, so we can't just do a git push. Instead we'll need to specify a remote and path.

		$ dojo_rules (kill_list)$ git push origin kill_list
			

