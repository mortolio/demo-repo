# Demo Repo - Hackathon

On your local machine, make a clone of the repo if you want to experiment on your local machine.

```
git clone git@github.com>:mortolio/demo-repo.git .
```

or `fork` the repo to experiment with this code exersise yourself.

## References

- <https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository>
- <https://rtyley.github.io/bfg-repo-cleaner/>
- <https://buildvirtual.net/how-to-remove-or-delete-a-file-from-git/#:~:text=To%20delete%20a%20file>

## Share Links

- <https://ohmygit.org/>
- <https://learngitbranching.js.org/>
- <https://www.git-tower.com/learn/git/faq/git-squash>
- <https://www.git-tower.com/>

## Some More Reading

- <https://www.git-tower.com/blog/7-git-mistakes-a-developer-should-avoid/>
- <https://about.gitlab.com/blog/2018/08/08/git-happens/>
- <https://git-scm.com/docs/git-switch>

## Commands

>Reference: <https://sentry.io/answers/delete-a-file-from-a-git-repository/>

### Search for code in Github

```
https://github.com/search?q=secret&type=code
```

### Commands For Demo

Commit a removal of a file.

```
rm passwordrm.txt
git commit -m "DELETE: Remove a password file"
git push -u origin master
```

Delete a file from the repo. (.gitignore)

```
git rm password2.txt
git rm --cached password2.txt
```

Delete a file from the entire repo history. (Just watch out for the gotcha that you will have to do this for branches as well.)

```
git filter-repo -f --index-filter 'git rm --cached --ignore-unmatch password2.txt'

git push --force -u origin main
```

OR -

> Reference: <https://git-scm.com/docs/git-filter-branch>

```
git filter-branch --tree-filter 'rm -f password2.txt' HEAD

git push --force -u origin main
```
