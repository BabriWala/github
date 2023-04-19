> So, we do not have the new branch on our local Git. But we know it is available on GitHub. So we can use the -a option to see all local and remote branches:

    git branch -a
    * master
    remotes/origin/html-skeleton
    remotes/origin/master

>Note: branch -r is for remote branches only.

We see that the branch html-skeleton is available remotely, but not on our local git. Lets check it out:

    git checkout html-skeleton
    Switched to a new branch 'html-skeleton'
    Branch 'html-skeleton' set up to track remote branch 'html-skeleton' from 'origin'.

And check if it is all up to date:

    git pull
    Already up to date.

Which branches do we have now, and where are we working from?

    git branch
    * html-skeleton
    master