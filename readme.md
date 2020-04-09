# Git config
## Git main config
```bash
git config --global user.name "username"
git config --global user.email "email"
```
## Get git config
```bash
git config --list
```


# Git help
```bash
git help config
git config --help
git add --help
```

# Initialize a repository from existing code
```bash
git init
```

# Remove git
```bash
rm -rf .git
```

# Get git status
```bash
git status
```

# Ignore some files and folders
.gitignore
*.pyc

# git area | where are we now?
working directory | staging area | .git directory (Repository)

## Add files to staging area
```bash
git add .gitignore
git add -A
git status
```

## Remove files from staging area
```bash
git reset .gitignore
git reset
```

## Commit
```bash
git commit -m "Initial commit"
git log
```

## Writing commit messages
- Short single-line summary (less than 50 characters)
- Optionaly followed by a blank line and a more complete description
- Keep each line to less than 72 characters
- Write commit messges in present tense, not past tense
  > "fix bug" or "fixes bug" not "fixed bug"
- Bullet points are usually astrisks or hyphens
- Can add "ticket tracking numbers" from bugs or support request
- Can develope shorthand for your orgnization
  > "[css, js]"

  > "bugfix: "

  > "#38405 - "

- Be clear and descriptive
  > Bad: "Fix typo" | Good: "Add missing > in project section of HTML"

  > Bad: "Update login code" | Good: "Change user authentication to use Blowfish"

  > Bad: "Update member report, we should discuss if this is right next week" |

### Exmaple of good commit:
> t23094 - Fixes bug in admin logout

> When an admin logged out of the admin area, they could not log in to the members
> because their sesson[:user_id] was still set to the admin ID. This patch fixes the bug by
> setting session[:user_id] to nil when any user logs out of any area.


# Clone Repository
## Track an existing remote repository with Git
```bash
git clone <url> <where to clone>
git clone ../remote_repo.git .
```

## Viewing information about the remote repository
```bash
git remote -v
git branch -a
```

# Pushing changes
## Commit 
```bash
git diff
git status
git add -A
git commit -m "Modified multiply function"
```

## Then push it
```bash
git pull origin master
git push origin master
```

# Common workflow
## Crate a branch for desired feature
```bash
git branch calc-divide
git branch
git checkout calc-divide
```

## After commit push branch to remote
```bash
git push -u origin calc-divide
git branch a
```

## Merge a branch
```bash
git checkout master
git pull origin master
git branch --merged
git merge calc-divide
git push origin master
```

## Deleting a branch
```bash
git branch --merged
git branch -d calc-divide
git branch -a
git push origin --delete calc-divide
```
