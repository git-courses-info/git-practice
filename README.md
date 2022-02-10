# git-practice

A repo to practice git
Let's say this is the starting point of a new app, that footios and fotistsakiris are going to implement together.\
In order to achive this, i.e. play the roll for two different devs, I cloned the repo in two different places and started commiting changes in each cloned project, after I change the personal settings in `git config --global -e`.

**Let the game begin!**

Note: The maintainer of this repo is going to be `footios` and `fotiostsakirs` will be the collaborator.

1. Collaboration

- (fotistsakiris) OK, may I please have my first assignment?
- (footios) I created `App.js`, `Auth.js` and `Home.js` your assingment is to create a new branch called `feature/home` where you implement `Home.js` according to instructions. Success!
- (fotistsakiris) Thanks! I created a new branch: `git switch -C featur/home`.\
  Then I implemented a basic implementation of `Home.js` and then I pushed it: `git push -u origin feature/home`.\
  The rest of the dialog went on in the pull request with name `Feature/home`, that can be found in fotistsakiris account.
- (footios) Nice! So we made our first simple colaboration. Now I will delete the remote branch `feature/home` and we both should delete it from our local repos.\
  Notes:
  - To see all branches (local and remote): `git branch -a`. See only remote: `git branch -r`
  - To delete local branches: `git branch -d feature/home`. If it wasn't merged: `git branch -D feature/home`.
  - To delete remote branches: `git push origin --delete feature/home`.
  - Remove tracking branches that are deleted on the remote repo: `git remote prune origin`, or `git fetch --prune`.

2. Pull requests

- (footios) Now fotistsakiris should implement `Auth.js` too. Note: repeate the above steps.
- (fotistsakiris) I created `feature/auth` branch, implemeted the UI for `Auth.js`, commited the changes, pushed the new branch.
- (footios) This time I will make some changes. So: `git fetch` to get the new branch and `git switch -C feature/auth origin/feature/auth`\
  to create a local branch and map it to the remote one.

3. Resolve conflicts

- (fotistsakiris) - I created a new branch: `git switch -C feature/login`. Then implemented login feature. Pushed to `git push -u origin feature/login`.\
  Then for siplicity, switched to master and make a change. Then pushed master. Now we have a conflict and we cannot have a ff merge. Conflicts mast be resolved.\
  Then I opend a pull request and requested review from footios.\
  Now the one that is responsible for merging this branch must resolve the conflicts. He can use the command line, or the user interface. The process is the same as resolving conflicts in local branches. First ofcourse you pull and then start the merge. Resolve conflict, add commit, push to github. But this time we're going to resolve the conflicts on github.\
  Then did the usual steps to delete the branches.

4. Revert commits

5. drop commit

update readme
