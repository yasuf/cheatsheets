## Git cheatsheet

1. How to trigger a CI re-run without a new commit:
```
# Recreate last commit
git commit --amend --no-edit

# Force push
git push --force-with-lease origin [PR Branch]
```
