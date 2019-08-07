# Gitflow
Trying out git flow and recording all the equivalent git commands
3] git flow feature start addsecondfile --showcommands
git config --local gitflow.branch.feature/addsecondfile.base develop
git checkout -b feature/addsecondfile develop
Switched to a new branch 'feature/addsecondfile'

Summary of actions:
- A new branch 'feature/addsecondfile' was created, based on 'develop'
- You are now on branch 'feature/addsecondfile'

Now, start committing on your feature. When done, use:

     git flow feature finish addsecondfile
