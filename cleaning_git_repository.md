# Listing authors in repository

`git shortlog -e -s -n`

# Changing author's email in commits 
(useful if you commited with different e-mails because you were lazy or you were in different computers...)

Use this bash script:

```
#!/bin/sh

git filter-branch -f --env-filter '
OLD_EMAIL="old@email.com"
CORRECT_NAME="Alex Lage"
CORRECT_EMAIL="amlage.cv@gmail.com"
if [ "$GIT_COMMITTER_EMAIL" = "$OLD_EMAIL" ]
then
    export GIT_COMMITTER_NAME="$CORRECT_NAME"
    export GIT_COMMITTER_EMAIL="$CORRECT_EMAIL"
fi
if [ "$GIT_AUTHOR_EMAIL" = "$OLD_EMAIL" ]
then
    export GIT_AUTHOR_NAME="$CORRECT_NAME"
    export GIT_AUTHOR_EMAIL="$CORRECT_EMAIL"
fi
' --tag-name-filter cat -- --branches --tags
```



# Removing large files and directories rewriting history

If your git repository is full of dependency and generated build folders and bitbucket is warninig you, you may rewrite your repo's history with:

`git filter-branch --index-filter "git rm -rf --cached --ignore-unmatch path_to_file" HEAD`


You may be interested in the following list:

## React-native

node_modules/

android/build/

android/app/build/

android/.gradle

ios/Pods



