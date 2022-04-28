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
git config --global user.signingkey ????
git config --global commit.gpgsign true
git config --global gpg.program "C:\Program Files\Git\usr\bin\gpg.exe"
```

**BackUp** :

```powershell
gpg --export-secret-keys ???? > backup.gpg
```

**import previous keys** :

```powershell
# importing public key
gpg --import my_public_key.pub

# importing private key
gpg --allow-secret-key-import --import my_private_key.private
```


**The resulting .gitconfig would have the user section like so:** :

```powershell

[user]
    name = Your Name
    email = your@email.com
    signingkey = [long-key]
[commit]
    gpgsign = true
```
**You can verify this is working by attempting to commit anything and then viewing the log with signatures turned on:** :

```powershell
mkdir ~/test
cd ~/test
git init
echo "test" >> test
git add test
git commit -m "test"
git log --show-signature
cd ..
rm -rf test
```

**Troubleshooting** :

We include this extra section for those times when something doesn’t go quite right.
```Error: “signing failed: No secret key”```
This means GPG can’t find the secret key that corresponds to the public key you configured. To see what the current value is, run the following command:
```git config --global user.signingkey```
You can then list your existing keys with ```gpg --list-keys```. The two should match. If they don’t you need to change the key git uses to the one from gpg. You can do so by running the command
```git config --global user.signingkey NEWKEYHERE```


```powershell
# restart the gpg-agent
gpgconf --kill gpg-agent

#where gpg
git config --global gpg.program "C:/Program Files (x86)/GNU/GnuPG/gpg.exe"

#where gpg
[gpg]
program = "C:\\Program Files (x86)\\GnuPG\\bin\\gpg.exe"


# copied everything from
C:\Users\USERNAME\.gnupg
# to
C:\Users\USERNAME\AppData\Roaming\gnupg
```

**[Direct link to Add my GPG Key to GitHub](https://github.com/settings/keys)**
**[Direct link to Add my SSH Key to SourceHut](https://meta.sr.ht/keys)**


**[Tutorial how to add my GPG Key to GitHub](https://help.github.com/articles/adding-a-new-gpg-key-to-your-github-account/)**



**[More info](https://medium.com/bootstart/signed-commits-ec2cab9e7254)**
