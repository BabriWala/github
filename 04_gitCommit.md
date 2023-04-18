>Since we have finished our work, we are ready move from stage to commit for our repo.

>Adding commits keep track of our progress and changes as we work. Git considers each commit change point or "save point". It is a point in the project you can go back to if you find a bug, or want to make a change.

>When we commit, we should always include a message.

>By adding clear messages to each commit, it is easy for yourself (and others) to see what has changed and when.

    git commit -m "First release of Hello World!"
    [master (root-commit) 221ec6e] First release of Hello World!
    3 files changed, 26 insertions(+)
    create mode 100644 README.md
    create mode 100644 bluestyle.css
    create mode 100644 index.html

>
    The commit command performs a commit, and the -m "message" adds a message.

    The Staging Environment has been committed to our repo, with the message:
    "First release of Hello World!"

>
    we will use the --short option to see the changes in a more compact way:

> 
    git status --short
    M index.html



Note: Short status flags are:

    ?? - Untracked files
    A - Files added to stage
    M - Modified files
    D - Deleted files

We see the file we expected is modified. So let's commit it directly:

    git commit -a -m "Updated index.html with a new line"
    [master 09f4acd] Updated index.html with a new line
    1 file changed, 1 insertion(+)

    Warning: Skipping the Staging Environment is not generally recommended.
    Skipping the stage step can sometimes make you include unwanted changes.

To view the history of commits for a repository, you can use the log command:

    git log
    commit 09f4acd3f8836b7f6fc44ad9e012f82faf861803 (HEAD -> master)
    Author: w3schools-test 
    Date:   Fri Mar 26 09:35:54 2021 +0100

        Updated index.html with a new line

    commit 221ec6e10aeedbfd02b85264087cd9adc18e4b26
    Author: w3schools-test 
    Date:   Fri Mar 26 09:13:07 2021 +0100

        First release of Hello World!