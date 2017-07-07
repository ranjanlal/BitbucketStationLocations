## New feature development workflow

### 1. Update local master:
```
git checkout master
git pull origin master
```

### 2. Create new branch off of master
```
git checkout -b [branch-name]
```

### 3. Implement changes in [branch-name]

### 4. Commit changes to [branch-name]

### 5. Rebase with master:
```
git pull --rebase origin master
Fix conflicts (if any)
git commit -am "[commit msg]"
```

### 6. Squash commits (as needed):
```
git reset --soft HEAD~[n]
git commit -am "[commit msg]"
```

### 7. Push to branch:
```
git push origin [branch-name]
```

### 8. Open a PR

### 9. Address Review comments
```
git pull origin [branch-name] ** (if other devs sharing the same branch)
commit changes
git push origin [branch-name]
```

### 10. After PR approved:
- check if master has changed (commits from other devs PR merged to master) 
- Follow steps : 5, 6, 7 

### 11. Merge [branch-name] to master

### 12. Delete [branch-name] from remote & local