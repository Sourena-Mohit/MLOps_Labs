# MLOps_Labs
This repo is for DSTI MLOps course labs.
## Set Up an SSH Key
Generate a New SSH Key : ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

Add the SSH Key to the SSH Agent : 
- eval "$(ssh-agent -s)"
- ssh-add ~/.ssh/id_rsa
## Add the SSH Key to GitHub Account
Copy the SSH Key :
- cat ~/.ssh/id_rsa.pub
- xclip -sel clip < ~/.ssh/id_rsa.pub
Add the Key to GitHub -> Settings > SSH and GPG keys
## Clone the Repository
using git clone 
## Verify the Connection
- ssh -T git@github.com
##  clone a repository using the HTTPS web URL
Using a Personal Access Token :
- Create a Personal Access Token (PAT) :
  -  Settings > Developer Settings > Personal Access Tokens
  -  Generate new token
  -  Copy the generated token and store it securely
    
Use the Token for HTTPS Authentication :
- When prompted for a username during the git clone process, use your GitHub username.
- For the password, paste your personal access token.


