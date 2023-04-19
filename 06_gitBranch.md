In Git, a branch is a new/separate version of the main repository.

Let's say you have a large project, and you need to update the design on it.

How would that work without and with Git:

Without Git:

    Make copies of all the relevant files to avoid impacting the live version
    Start working with the design and find that code depend on code in other files, that also need to be changed!
    Make copies of the dependant files as well. Making sure that every file dependency references the correct file name
    EMERGENCY! There is an unrelated error somewhere else in the project that needs to be fixed ASAP!
    Save all your files, making a note of the names of the copies you were working on
    Work on the unrelated error and update the code to fix it
    Go back to the design, and finish the work there
    Copy the code or rename the files, so the updated design is on the live version
    (2 weeks later, you realize that the unrelated error was not fixed in the new design version because you copied the files before the fix)

With Git:

    With a new branch called new-design, edit the code directly without impacting the main branch
    EMERGENCY! There is an unrelated error somewhere else in the project that needs to be fixed ASAP!
    Create a new branch from the main project called small-error-fix
    Fix the unrelated error and merge the small-error-fix branch with the main branch
    You go back to the new-design branch, and finish the work there
    Merge the new-design branch with main (getting alerted to the small error fix that you were missing)

Branches allow you to work on different parts of a project without impacting the main branch.

When the work is complete, a branch can be merged with the main project.

You can even switch between branches and work on different projects without them interfering with each other.

Branching in Git is very lightweight and fast!

we create a new branch:

    git branch hello-world-images

Now we created a new branch called "hello-world-images"

Let's confirm that we have created a new branch:

    git branch
    hello-world-images
    * master

> We can see the new branch with the name "hello-world-images", but the * beside master specifies that we are currently on that branch.

> checkout is the command used to check out a branch. Moving us from the current branch, to the one specified at the end of the command:

    git checkout hello-world-images
    Switched to branch 'hello-world-images'

Now check the status of the current branch:

    git status
    On branch hello-world-images
    Changes not staged for commit:
        (use "git add ..." to update what will be committed)
        (use "git restore ..." to discard changes in working directory)
            modified:   index.html

    Untracked files:
        (use "git add ..." to include in what will be committed)
            img_hello_world.jpg

    no changes added to commit (use "git add" and/or "git commit -a")

So let's go through what happens here:

    There are changes to our index.html, but the file is not staged for commit
    img_hello_world.jpg is not tracked

So we need to add both files to the Staging Environment for this branch:

git add --all

Using --all instead of individual filenames will Stage all changed (new, modified, and deleted) files.

Check the status of the branch:

    git status
    On branch hello-world-images
    Changes to be committed:
    (use "git restore --staged ..." to unstage)
        new file: img_hello_world.jpg
        modified: index.html

We are happy with our changes. So we will commit them to the branch:

    git commit -m "Added image to Hello World"
    [hello-world-images 0312c55] Added image to Hello World
    2 files changed, 1 insertion(+)
    create mode 100644 img_hello_world.jpg

> Note: Using the -b option on checkout will create a new branch, and move to it, if it does not exist

We are currently on the branch hello-world-images. We added an image to this branch, so let's list the files in the current directory:

    ls
    README.md  bluestyle.css  img_hello_world.jpg  index.html

We can see the new file img_hello_world.jpg, and if we open the html file, we can see the code has been altered. All is as it should be.

Now, let's see what happens when we change branch to master

    git checkout master
    Switched to branch 'master'

The new image is not a part of this branch. List the files in the current directory again:

    ls
    README.md  bluestyle.css  index.html