

# To reproduce

Run these commands in the shell
```
git clone git@github.com:chrishiestand/atom-fuzzy-finder-git-bug.git
cd atom-fuzzy-finder-git-bug
git clone git@github.com:chrishiestand/atom-fuzzy-finder-git-bug-sub.git sub
atom sub
```

In atom, hit cmd+t (open fuzzy finder) and it incorrectly states the project is empty

The reason seems to be due to the pattern in .gitignore but this behavior is incorrect. The workdir for `atom-fuzzy-finder-git-bug-sub` is `sub` the parent's `.gitignore` should not be consulted
