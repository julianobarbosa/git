```console
- Clone
-- git flow init
-- git flow feature start <<FeatureName>>
-- Work On
-- git flow feature finish <<FeatureName>
-- git pull origin develop
```


- git flow
  - setup the git flow project
  - create branches and merge everything to develop
  - run the command "git flow release start "
  - then provide a meaningful message for the release
  - run the command "git flow release finish "
  - it will merge everything in to master and change the branch to master.
  - run the command "git push" to publish the changes to the remote master.

Reference
- URL: https://stackoverflow.com/questions/14168677/merge-development-branch-with-master
