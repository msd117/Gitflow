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


3] git flow feature start addsecondfile --showcommands
git config --local gitflow.branch.feature/addsecondfile.base develop
git checkout -b feature/addsecondfile develop
Switched to a new branch 'feature/addsecondfile'

Summary of actions:
- A new branch 'feature/addsecondfile' was created, based on 'develop'
- You are now on branch 'feature/addsecondfile'

Now, start committing on your feature. When done, use:

     git flow feature finish addsecondfile

4]  git flow feature finish addsecondfile --showcommands
git checkout develop
Switched to branch 'develop'
git merge --ff feature/addsecondfile
Updating b526a21..4adc8f1
Fast-forward
 README.md     | 12 ++++++++++++
 secondfile.js |  0
 2 files changed, 12 insertions(+)
 create mode 100644 secondfile.js
git branch -d feature/addsecondfile
Deleted branch feature/addsecondfile (was 4adc8f1).

Summary of actions:
- The feature branch 'feature/addsecondfile' was merged into 'develop'
- Feature branch 'feature/addsecondfile' has been locally deleted
- You are now on branch 'develop'
