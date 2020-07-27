If your git repository is full of dependency and generated build folders and bitbucket is warninig you, you may rewrite your repo's history with:

git filter-branch --index-filter "git rm -rf --cached --ignore-unmatch path_to_file" HEAD


You may be interested in the following list:

node_modules/
android/build/
android/app/build/
ios/Pods
