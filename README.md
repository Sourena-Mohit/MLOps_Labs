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
