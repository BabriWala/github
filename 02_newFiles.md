You just created your first local Git repo. But it is empty.

    ls
    index.html

> ls will list the files in the directory. We can see that index.html is there.
Then we check the Git status and see if it is a part of our repo:

    git status
    On branch master

    No commits yet

    Untracked files:
    (use "git add ..." to include in what will be committed)
        index.html

    nothing added to commit but untracked files present (use "git add" to track)

> Now Git is aware of the file, but has not added it to our repository!

> Files in your Git repository folder can be in one of 2 states:

    Tracked - files that Git knows about and are added to the repository
    Untracked - files that are in your working directory, but not added to the repository

> When you first add files to an empty repository, they are all untracked. To get Git to track them, you need to stage them, or add them to the staging environment.