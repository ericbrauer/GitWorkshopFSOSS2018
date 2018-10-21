## Working outside of github

When you write code, you will not be using the github web editor.  Learning to work outside of github and then committing the code back is really important.  This last section looks at doing the previous activity with editing outside of github.

### Keep your team and your repo
* We will use the same repo as activity 3 for this activity. 

### Step 1: Clone a repo

To work offline, you often start by creating a local version of your repository.  Click the arrow on the clone or download button (code tab, top right) and copy the url.  To keep it simple, we will use the https version.  The ssh version requires more setup.

In your git bash shell:

* ensure you are not sitting inside a repository (type ```git status``` at the prompt.  It should say: ```fatal: Not a git repository (or any of the parent directories): .git```)
* type ```git clone pasteYourRepoURLHere```
* This will create a folder that has the same name as your repo. 
* cd into this folder.  All git commands will be issued from in here


### Step 2: Create a local branch and go into that branch

To avoid naming conflict with your branch from activity 3, please name your branch differently (maybe shorten your branch name to something like: is1 instead of iss1 for example)

* Create a branch locally - ```git branch putBranchNameHere```
* Checkout the branch - ```git checkout putBranchNameHere```

### Step 3: Edit the file, save, add and commit

* Use whatever text editor you want, modify the file song.md with what you need
* Save the file
* Add the file - ```git add song.md```
* Commit the file - ```git commit -m "my commit message"

### Step 4: Push to github and create PR:

* Push your code to repo on github: ```git push origin putBranchNameHere```
* Create a PR for your pull request
* Assign a reviewer

### Step 5: Resolving "bugs"

If your PR was rejected you will need to fix your bugs
* Edit the file to fix the bug
* Add and commit
* push to the same branch

Note just like using the github interface you do not need to do a new PR.  When you push your code, the PR automatically updates to what is most recent on your branch.  Similarly if master was modified after you submitted your PR, it will be modified when you try to merge them.  This is why sometimes you can commit code that does not have a conflict and have to resolve conflicts because another patch was added before you finished.

### Step 6: Resolving conflicts

You may encounter a conflict. You will know that there is a conflict if you can't automatically merge your code.  If you are the author, this is what you need to do:

* Go into your master branch (git checkout master)
* pull down whatever is new (git pull origin master)
* Go into the branch with the conflict (git checkout putBranchNameHere)
* Merge in master branch (git merge master)
* Fix conflicts by editing file
* Save, add and commit (```git add song.md```, ```git commit -m "fixed conflicts"```)
* Push to repo (```git push origin putBranchNameHere```)




