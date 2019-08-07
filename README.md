# Gitflow
Trying out git flow and recording all the equivalent git commands
1] git flow init --showcommands

Which branch should be used for bringing forth production releases?
   - master
Branch name for production releases: [master]
git config gitflow.branch.master master
Branch name for "next release" development: [develop]
git config gitflow.branch.develop develop
git branch --no-track develop master
git checkout -q develop

How to name your supporting branch prefixes?
Feature branches? [] feature/
git config gitflow.prefix.feature feature/
Bugfix branches? [] bugfix/
git config gitflow.prefix.bugfix bugfix/
Release branches? [] release/
git config gitflow.prefix.release release/
Hotfix branches? [] hotfix/
git config gitflow.prefix.hotfix hotfix/
Support branches? [] support/
git config gitflow.prefix.support support/
Version tag prefix? []
git config gitflow.prefix.versiontag
Hooks and filters directory? [E:/Gitflow/.git/hooks]
git config gitflow.path.hooks E:/Gitflow/.git/hooks


2]  git flow feature start addfirstfile --showcommands
git config --local gitflow.branch.feature/addfirstfile.base develop
git checkout -b feature/addfirstfile develop
Switched to a new branch 'feature/addfirstfile'
M       README.md

Summary of actions:
- A new branch 'feature/addfirstfile' was created, based on 'develop'
- You are now on branch 'feature/addfirstfile'

Now, start committing on your feature. When done, use:

     git flow feature finish addfirstfile

