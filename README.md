# Template-Repo
Template repository for new repos at SEB.

# Setup

## For Windows users:

1. Make sure git is installed with symlink support

During the install of git on Windows:
<img src="https://i.stack.imgur.com/Am9L1.png" />

2. Tell Bash to create hardlinks instead of symlinks

EDIT -- (git folder)/etc/bash.bashrc

ADD TO BOTTOM - `MSYS=winsymlinks:nativestrict`

3. Set git config to use symlinks
```bash
git config core.symlinks true
```
or

```bash
git clone -c core.symlinks=true <URL>
```
NOTE: I have tried adding this to the global git config and at the moment it is not working for me so I recommend adding this to each repo...

4. Pull the repo

NOTE: Unless you have enabled developer mode in the latest version of Windows 10, you need to run bash as **administrator** to create symlinks

5. Reset all Symlinks (optional) If you have an existing repo, or are using submodules you may find that the symlinks are not being created correctly so to refresh all the symlinks in the repo you can run these commands.

```bash
find -type l -delete
git reset --hard
```
NOTE: This will reset any changes since last commit so make sure you have committed first
