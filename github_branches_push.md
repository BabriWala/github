Start by creating a branch, like we did earlier:

    git checkout -b update-readme
    Switched to a new branch 'update-readme

    git status
    On branch update-readme
    Changes not staged for commit:
    (use "git add ..." to update what will be committed)
    (use "git restore ..." to discard changes in working directory)
            modified:   README.md

    no changes added to commit (use "git add" and/or "git commit -a")

Now push the branch from our local Git repository, to GitHub, where everyone can see the changes:



    git push origin update-readme
    Enumerating objects: 5, done.
    Counting objects: 100% (5/5), done.
    Delta compression using up to 16 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 366 bytes | 366.00 KiB/s, done.
    Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
    remote:
    remote: Create a pull request for 'update-readme' on GitHub by visiting:
    remote:      https://github.com/w3schools-test/hello-world/pull/new/update-readme
    remote:
    To https://github.com/w3schools-test/hello-world.git
    * [new branch]      update-readme -> update-readme