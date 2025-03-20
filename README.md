# Learning-Git-and-Github
Git and Github
-Helps to work together on a common project folder, and also saves history of the project. It saves the code, as well as who made what changes and when were they made.

Git Repository is the folder where all this changes, history, etc are stored. Git Repo is just a separate folder storing/copying the exact things what you r doing in your project folder/work directory. 
GIT-
1. Get inside the project folder by cd name.
2. Than do git init. This makes the git repo that will now store all the history of this folder. The folder is named .git
3. The .git folder is a hidden folder. So ls won’t show it. Do ls -a This shows all the hidden files as well
4. You can also see what’s inside this .git folder by ls .git
5. Now any change made in this project, git will pick it up.
6. Now, let’s make a folder by touch name.txt inside our yoyo folder
7. Git status lets us see what’s all changes made are not currently saved as history in grit repo. Here, if we do git status, we will see this text folder as under the pretext of ‘untracked files’. So, if I share this folder or git repo, no one will know about this change, which here is out text folder
8. And now, first we select the files which are to be saved or not in git repo. We do git add . for all files in the project folder. We do git add names.txt for this particular folder.
9. Now, these files are selected whose history is to be saved. And now to save the changes- git commit -m “your message” -m is for the readable message you want to add alongside the change you made.
10. Now, let’s say we do some changes in the file, so again after doing the changes, we have to put the file on stage(track) and then do git commit -m “message”
11. If we want to remove some file from stage, i.e  remove it from stage(track) and don’t commit it, we do git restore --staged names.txt
12. git log for viewing all this stored history
13. Now, if I delete the text file and then I can restore it using git restore name.txt 
14. The git status will remain clean, as no modification has actually been made. So nothing to be tracked will show up if I do git status.
15. Now, let’s say I deleted the text file, and then committed the change rather than restoring it, now I can’t restore the file as even git repo don’t have the file now.
16. We can’t remove a particular commit but we can remove the latest sequence till a point we want in git repo. To do it- git reset hashid Take commit hash-id from git log. This will now keep the git log till the point of this hash-id. And now, all this things that are different in actual work directory than to git repo, would be placed in un-staged area. Eg- I don’t have a file in work directory as I created and deleted it. But in git repo, I reset it till the point I created it. So now in un-staging area, I will have it as deleted this folder. Or if I deleted the file and made a new one. In unstaged area, I will be shown as rename.
17. To see al the changes in a particular commit do, git show hashid
18. Git stash  stores the uncommitted work in some temporary folder, and removes it from actual working directory i.e the uncommitted changes would be reversed in actual folder. And if I want to bring this changes into project, do git stash pop. It brings it all to staging/tracking area. Now commit the changes. So It helps up when nor we want to loose our changes, and nor we want to commit it. 
19. However, if we have that changes in git stash and now we no longer desire it, and so we can delete it permanently by git stash clear

Github is one of the platforms/online website that allows us to host our git repositories. Some other platforms are gitlab, bitbucket, etc.
GITHUB-
Hosting your own project-
1. Dashboard -> Create repository -> Url generated
2. Now, we want this URL to be connected to our project/working directory. git remote add origin URL .By convention, all repositories in our personal github account are called origin. 
3. Git remote -v shows all the URLs attached to this particular folder/working directory
4. Now, to share the changes to this URL, do git push origin main  main is the branch where we want to push these changes made in work folder(actual local working directory) onto origin(i.e remote URL)
5. To create a new brach,  git branch name. Branching is useful. For eg- if we want to edit a code, we should do it on a separate branch so that the main code doesn’t get affected.
6. Git branch to check what branch we are on
7. Now, head will be pointing towards this branch i.e all the changes u now make and commit will be added onto this branch.
8. To shift to branch, do git checkout name
9. S

Red- these lines were deleted
Green- these lines were added

1. To open the GitHub Folder in your laptop i.e local machine, do github clone URL .The path to this local folder would be the same folder you typed this command in.
Github don’t allow to do push,pull etc without asking for username and password. Password is not the id password but this PAToken generated through developer options ins settings. This will be asked in terminal when you try to push/pull etc.


