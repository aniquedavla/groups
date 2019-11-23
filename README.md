# Git workflow

## Where to write your code
- #### local master: 
	is the master branch you have on your computer. 
- #### remote master: 
	it is usually the master branch on github 
- #### local and remote master branch: 
	used to keep a working version of the app that you can merge changes from your local branch changes to.
- #### your branches: 
	you can make branches for each feature, update or one branch for all your work. This is your branch which is not master. This is where you make changes to the project. Once you are ready to submit this code to master, you can follow the steps to merge your code with master below. 

## Steps to merge your code with master
### Prereq:
- Only do this when you have something significant to merge with master like a decent amount of code or progress towards a feature.
- Notify group that you would be will be merging and pushing your changes to master so there is only one person pushing changes to master. To avoid a lot of merge conflicts its better if one person merges their changes to master at a time. 
- Your changes should be in your own branch which is not master.
- Your current local master should pull from master before you merge your changes(step 1 helps you do this).

### Step 1: pulls any updates from remote master to your local master.
	git checkout master
	git pull

### Step 2: merges your branch's code to your local master. You don’t have to type the “<>”
	git checkout <your branch name where your code is>
	git merge --strategy=ours master 	#keeps the content of this branch, but records a merge
	git checkout master
  	git merge <your branch name where your code is>		#fast-forwards master up to the merge
### Step 3: verify merge and push to master
	git checkout master 
	# check the changes and try to run the code. Fix any errors in merging. Make sure the entire app works before pushing. YOU WILL REDO OTHER 		PEOPLE’S WORK IF YOU PUSH BROKEN CODE TO MASTER	
	git add .
	git commit -m  “You name and changes merged with master ”
	git push

