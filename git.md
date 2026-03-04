# Git

Delete all stale remote-tracking branches under `name`
``` bash
git remote prune [-n | --dry-run] <name>
  
  OR BETTER:
  
git branch -vv | grep ': gone]' | awk '{print $1}' | xargs git branch -D
```
