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
1. Merge changes into main:
   - `git checkout main`
   - `git merge develop`
   - `git push origin main`