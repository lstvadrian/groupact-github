# My GitHub Learning Journey

Hi there! I'm Cristel, and I have been exploring GitHub to learn more about version control. Here's a summary of what I have learned so far.

## GitHub Basic

I started with the basics:

### • Setting up a Repository:

1. First, created a public repository named `cristel-github-learning`
2. Then, created a folder named `cristel-github-learning` on my local machine.
3. I opened this folder in VS Code.
4. In VS Code, I opened the terminal and initialized a Git Repository by running these commands:
   - `git init`
   - `git remote add origin https://github.com/lstvcristel/cristel-github-learning.git`
   - `git branch -M main`
   - `touch README.md`
   - `git status`
   - `git add .`
   - `git commit -m "Initial commit"`
   - `git push -u origin main`

### • Generating SSH Key and Cloning using SSH:

1. Generate a SSH key to your local machine:
   - Open a termina and run `ssh-keygen -t ed25519 -C "lstv.cristel.millan@gmail.com"`
   - Enter the file name of the .shh key.
   - Enter a passphrase (optional).
2. Start the SSH agent by running this commands:
   - `eval "$(ssh-agent -s)"`
   - `ssh-add ~/.ssh/lstvcristel`
3. Copy your public key to your clipboard:
   - `clip < ~/lstvcristel.pub`
4. Go to GitHub and log in
5. Go to `Settings > SSH and GPG Keys`
6. Click `New SSH key`
7. Enter Title
8. Paste the key into the Key field
9. Click Add SSH Key to save.
10. Test if SHH is running `ssh -T git@github.com` if successful, this will show "Hi lstvcristel! You've successfully authenticated..."

### • Branching:

1. Create a new branch: `git branch develop`
2. Push and set upstream: `git push -u origin develop`
3. Switch to new branch: `git checkout develop`
4. Create and switch branch: `git checkout -b develop`
5. List all branches: `git branch`
6. Push a branch: `git push origin develop`
7. Delete branch from remote repo: `git branch --delete develop`

### • Merging:

1. Check or compare files between current branch and main branch:
   - `git diff main`
2. Merge changes into main:
   - `git checkout main`
   - `git merge develop`
   - `git push origin main`

### • Undoing Changes

1. Restore all files in current directory and will discards all unstaged changes
   - `git restore .`
2. Restore all files to their state in current or last commit
   -`git restore HEAD`

## GitHub Action

1. First I created a file `.github\workflows\test.yml`
2. Add this content:

   1. First I created a file `.github\workflows\test.yml`
3. Add this content:
   name: CI

   on:
   push:
   branches: ["develop"]
   pull_request:
   branches: ["develop"]

   workflow_dispatch:

   jobs:
   build:
   runs-on: ubuntu-latest
   steps:
   - uses: actions/checkout@v4

   - name: Run a one-line script
   run: echo "Hello, world!"

   - name: Notify
   run: echo "Workflow completed successfully!"

## GitHub Issues & Pull Requests

I learned how collaboration work using GitHub.

This is what I've learn so far:

1. Open a new Issue:
   - Title: Summary Activity 3
   - Description: Add summary of what have you learn in activity 3.
2. Forked the repository from team's repo, then clone it locally.
3. Create a new branch `git checkout -b fix-issue`
4. Made changes, then commit and push
5. Opened a Pull Request
6. After PR was merge, I closed the issue using the terminal with GitHub CLI:
   - Install GitHub CLI first by running this command in Powershell (Admin) `winget install --id GitHub.cli`
   - Check if isntalled `gh --version`
   - Log in and authenticate your account `gh auth login`
   - Set default remote repo `gh repo set-default`
   - Check issues `gh issue list`
   - Close issue `gh issue close 21`
7. GitHub Issue help track bugs and Pull Requests make collaboration organized

## Advance Git Commands

These helped me to manage commit history.

### • Squashing Commits Using Rebase

1. First I created a multiple commits
2. Check first recent commit history to make sure I am targeting the right commit. To show git commit history simply run `git log --oneline`
3. Then, squash commits using rebase to make multiple commits into single commit. Make commit history clean `git rebase -i HEAD~2`
     - Example:
            `pick f909087 Add Text1.txt`
            `pick 2328a6c Add Text2.txt file`
     - Change the second `pick` to `squash`
            `pick f909087 Add Text1.txt`
            `squash 2328a6c Add Text2.txt file`
     - Confirm if the Squash worked, run: `git log --oneline`
            `cfd1c8e (HEAD -> cristel) Add Text1.txt and Text2.txt file`

### • Cherry-picking
1. Create a new branch `git checkout -b cherry-picking-cristel`
2. Find a commit that you want to cherry pick `git log --oneline`
3. Cherry-pick a commit: `git cherry-pick 2328a6c`
4. Verify the commit is now on your current branch `git log --oneline`

Rebase: This is good for making commit history clean and organize.
Cherry-picking: This feature helps moving a commit to a different branch. Useful for bug fixes or enhamcement.

