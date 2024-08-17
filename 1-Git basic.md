# Git basic


## Configure Git
```
git config --global user.name "[YOUR_NAME]"
git config --global user.email "[YOUR_EMAIL]"
```

![Git configuration](img/git-config.png "Git Configuration")




## Git Workflow

![Git Workflow](img/git-workflow.avif "Git Workflow")
[credit](https://dev.to/mollynem/git-github--workflow-fundamentals-5496)



### 0. Initialize Git
```
git init
```
![Git Init](img/git-init.png)


### 1. Add files to staging area
```
git add [file_name]
git add .
git add --all
git add -A
```
```
git status

    U - Untracked files
    A - Files added to stage
    M - Modified files
    D - Deleted files
```

### 2. Commit
```
git commit -m "[COMMIT_MESSAGE]"
```
```
git log
```


---
## Work with branch
```
git branch
```

**New Git Branch**
```
git branch [NEW_BRANCH_NAME]
git checkout [NEW_BRANCH_NAME]
```

**Switching Between Branches**
```
git checkout [EXIST_BRANCH_NAME]
```

**Delete Branch**
```
git branch -d [EXIST_BRANCH_NAME]
git push origin --delete [EXIST_BRANCH_NAME]
```


---
## Branch Merge
Merge [TARGET_BRANCH] to [BASE_BRANCH]
```
git checkout [BASE_BRANCH]
git merge [TARGET_BRANCH]
```