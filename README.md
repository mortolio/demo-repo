# Demo Repo - Hackathon

## References

- <https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository>

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

Delete a file from the entire repo history.

```
git filter-repo -f --index-filter 'git rm --cached --ignore-unmatch password2.txt'

git push --force -u origin main
```
