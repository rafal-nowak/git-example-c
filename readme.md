Git
=================

Fundamental Git commands:
- ```git init```: Initialize a new Git repository.
- ```git clone```: Clone an existing Git repository.
- ```git add```: Stage changes for commit.
- ```git commit```: Commit changes with a message.
- ```git status```: Check the status of your working directory.
- ```git log```: View commit history.
- ```git branch <branch_name>```: create branch.
- ```git checkout <commit_hash>```: switch between branches / commits.
- ```git reset --hard <commit_hash>```: move your current branch to a different commit in the history.

Merging a Feature Branch into main:
Ensure you're on the main branch:
- ```git checkout main```

Merge the feature branch into main:
- ````git merge feature-branch````

This command will merge the changes from feature-branch into main. If Git can perform the merge automatically without conflicts, it will create a new merge commit on the main branch. If there are conflicts, Git will prompt you to resolve them before completing the merge.

Resolve Conflicts (if any):
- If there are conflicts, Git will pause the merge process and show you which files have conflicts.
- Manually edit the conflicting files to resolve the conflicts.
- After resolving conflicts, add the modified files and commit the changes.

Push the Changes to the Remote Repository (if needed):
- ```git push origin main```

Rebasing a Feature Branch onto `main`:
Ensure you're on the feature branch:
- ```git checkout feature-branch```

Rebase the feature branch onto main:
- ```git rebase main```

This command applies the commits from feature-branch on top of the latest commit on main. It replays the commits, creating a linear history.

Resolve Conflicts (if any):
- If there are conflicts during the rebase, Git will pause and show you which commits have conflicts.
- Manually edit the conflicting files to resolve the conflicts.
- After resolving conflicts, use git add to stage the changes, then continue the rebase with git rebase --continue.

Push the Changes to the Remote Repository (if needed):
- ```git push origin feature-branch```

If you've already pushed the feature branch to the remote repository before the rebase, you may need to force push it:
-  ```git push --force origin feature-branch```

Delete the local branch:
- ```git branch -d <branch_name>```

List all remote branches:
- ```git branch -r```

Delete the remote branch:
- ```git push origin --delete <branch_name>```