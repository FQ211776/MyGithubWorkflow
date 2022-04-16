# Adding a new GPG key to your GitHub account

**Description :**  If you don't have an existing GPG key, you can generate a new GPG key to use for signing commits and tags..
  
**Example** :

```powershell
# Install scoop
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
iwr -useb get.scoop.sh | iex

# Install git
scoop install git
git config --global credential.helper manager-core

# Install gpg4win
scoop install gpg4win

#
gpg --list-key
gpg --list-secret-keys --keyid-format LONG
gpg --gen-key
gpg --list-keys
gpg --list-secret-keys --keyid-format=long
gpg --armor --export ????

# in case don't work.

#where gpg
#git config --global gpg.program "C:/Program Files (x86)/GNU/GnuPG/gpg.exe"

```


**[Add my GPG Key to GitHub](https://help.github.com/articles/adding-a-new-gpg-key-to-your-github-account/)**