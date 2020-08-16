# miskate-commit

### [From the documentation](https://rtyley.github.io/bfg-repo-cleaner/0), it should be:

```
java -jar bfg.jar <options> yourrepo

```
Try and use the full path of the jar if you have an error like "Unable to access jarfile bfg.jar": /home/user/path/to/bfg.jar.

The alternative is described in "[Remove sensitive data](https://docs.github.com/en/github/authenticating-to-github/removing-sensitive-data-from-a-repository)"

```
git filter-branch --force --index-filter \
'git rm --cached --ignore-unmatch PATH-TO-YOUR-FILE-WITH-SENSITIVE-DATA' \
--prune-empty --tag-name-filter cat -- --all
```
You need to push force & tag again history commit
```
git push origin --force --all
git push origin --force --tags
```

Important after when removing file secret on the repo, add it in .gitignore


### Delete Github Cached View


My ref:
[BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/)


