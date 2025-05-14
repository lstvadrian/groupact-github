## Short summary for Activity 1 Github Basics (setup, Repositories, Branching, Merging)

I created a repository called git-training and added a README.md file to initialize it. After cloning the repo to VSCode, I created a new branch named master using git checkout -b master. I edited the README.md file in the master branch by adding a new sentence, then switched back to the main branch to merge the changes using git merge master. I pushed the changes to GitHub using git push origin main, but didn’t initially see the master branch on GitHub. To fix this, I pushed the master branch with git push -u origin master. This exercise helped me understand how to create branches, make changes, merge them, and push updates to remote repositories.

## Git Commands I Learned i've learn in Acitvity 1
- git clone <repo-url> – Clone a remote repository
- git checkout -b <branch-name> – Create and switch to a new branch
- git status – Check the current status
- git add . – Stage all changes
- git commit -m "message" – Commit with a message
- git checkout main – Switch back to the main branch
- git merge <branch-name> – Merge a branch into the current one
- git push origin main – Push changes to the main branch
- git push -u origin <branch-name> – Push a new branch to remote and set upstream

## Git Commands I Learned i've learn in Acitvity 2


## Git Commands I Learned i've learn in Acitvity 3
`For this GitHub collaboration task, I began by watching a video that explained how collaboration works using issues and pull requests. I then opened an issue in the main repository to describe a bug or feature request. After that, I created a new GitHub account to fork the main repository and made the necessary changes in the forked copy. Initially, I tried to push the changes directly to the main repository but encountered a permission error, as the new account had not been added as a collaborator. With the slight help of a developer who guided me on how to properly submit a pull request, I was able to push the changes to my forked repository and open a PR to the main repo. Since I had made little progress on my own during training, this guidance helped me better understand the process. Overall, this experience showed me how GitHub issues and pull requests help streamline collaboration by allowing contributors to communicate, review, and integrate changes in a structured and permission-based workflow.

## Git Commands I Learned i've learn in Acitvity 4
'i've learn using git rebase, stash, cherry-pick'
 - *rebase*, used for having a new saving point for local committing.
 - *stash*, used for saving in the local unit before pulling the changes from repository.
 - *cherry-pick*, used for backtracking the codes from previous commits. for bigger project safety.


## Git Commands I Learned i've learn in Acitvity 5
' based on our discussion with the developer that having a security in one repo is a must. we must protect the main branch for having pushing by other people without PR in there end. we also add an colaborative so the 3 of us can push in our branches even request a commit to main branch.'