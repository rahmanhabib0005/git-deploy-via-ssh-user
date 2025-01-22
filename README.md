# Git-Deploy-via-ssh-user
## Deploying to a Single Private Repository from local terminal with SSH access

# How-to-connect-putty-with-ssh
### Step 1: install puttly for required os
### Step 2: open puttygen with from windows app
### Step 3: open private key in puttygen ( which one you get from server or ssh server )
### Step 4: save private key with .pkr format -- it will automatically set the extention from puttygen
### Step 5: go to the putty
### Step 6: put server address or ip
### Step 7: in the sidebar go to the ssh > auth > credentials then upload the private key which one you save
### Step 8: open the terminal and acess the ssh 


### Go to the SSH directory
```bash
 cd ~/.ssh/
```
```bash
 ssh-keygen -t rsa -b 2048 -C "username@ip" -f ~/.ssh/new_project_rsa
```
```bash
 cat ~/.ssh/new_project_rsa.pub
```

### Copy it and open your private repositories settings and there has deploy keys section
### add the ssh key there
```bash
 nano ~/.ssh/config
```
```bash
 Host github.com
    User git
    IdentityFile ~/.ssh/dploy-git
```
### after paste click ctrl-s, ctrl-c, ctrl-x
```bash
 ssh -T github-new-project
```
### Go to the directory
```bash
 git clone "clone-url" 
```
 

