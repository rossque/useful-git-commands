# Useful GIT commands
The following lists a number of useful GIT commands.

### Reset all commits
The following will create a temporary branch and reset all commits into your "Initial commit". 
All files are will remain as they are. Your "main" branch will be replaced with a single commit.

``` shell
git checkout --orphan temp_branch && \
git add . && \
git commit -am "Initial release" && \
git branch -D main && \
git branch -m main && \
git push -f origin main
```

### Set global GIT name and email
Change your GIT configuration (globally) on your machine.

``` shell
git config --global user.name "<name>"
git config --global user.email <email-address>
```

### Prevent GIT checking file permissions

Check permissions are true or false
``` shell
git config --get --local  core.filemode
```

Locally (works best on vagrant)
``` shell
git config --local core.fileMode false
```

Globally
``` shell
git config --global core.fileMode false
```

### Deleting branches

Delete a branch locally
``` shell
git branch -d branch-name
```

Delete a branch remotely
``` shell
git push origin --delete branch-name
```
