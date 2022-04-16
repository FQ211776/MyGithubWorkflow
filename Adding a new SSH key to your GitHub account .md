# Adding a new SSH key to your GitHub account

**Description :**   Generate a new SSH key to use for authentication, then add it to the ssh-agent.

**Example** :

```powershell
# creates a new SSH key, using the provided email as a label.
ssh-keygen -t ed25519 -C "your_email@example.com"

# start the ssh-agent in the background
eval "$(ssh-agent -s)"

# Add your SSH private key to the ssh-agent.
ssh-add ~/.ssh/id_ed25519

# Copy the SSH public key to your clipboard
clip < ~/.ssh/id_ed25519.pub

```

**[Direct link to Add my SSH Key to GitHub](https://github.com/settings/keys)**



**[Tutorial how to add my SSH Key to GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)**
