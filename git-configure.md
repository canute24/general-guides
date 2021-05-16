# Configue git after install
##### Source: http://happygitwithr.com/usage-git-cmds.html

Git has multiple config files are various levels. Config options across levels are additive unless same option setting is specified at multiple levels in which case lowest file in the scope takes precidence:
--system > --global > --local

```shell
git config --global --list
git config --global user.name "USERNAME"
git config --global user.email "EMAIL"
git config --global color.ui auto
git config --global core.editor "emacs" / "'C:/Program Files/vim.exe --wait'"
git config --global merge.conflictstyle diff3
git config --global push.default current (This is alternate to `checkout -b branch push` error fix)
git stash pop # if failed with conflict then `git reset` and `git stash drop` required after merge to cleanup
```
