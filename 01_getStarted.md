
Now let Git know who you are. This is important for version control systems, as each Git commit uses this information:

    git config --global user.name "w3schools-test"
    git config --global user.email "test@w3schools.com"



    Note: Use global to set the username and e-mail for every repository on your computer.

    If you want to set the username/e-mail for just the current repo, you can remove global


Now, let's create a new folder for our project:

    mkdir myproject
    cd myproject

    mkdir makes a new directory.
    cd changes the current working directory.



    Note: If you already have a folder/directory you would like to use for Git:

    Navigate to it in command line, or open it in your file explorer, right-click and select "Git Bash here"

Once you have navigated to the correct folder, you can initialize Git on that folder:

    git init 
    Initialized empty Git repository in /Users/user/myproject/.git/ 



    Note: Git now knows that it should watch the folder you initiated it on.
    Git creates a hidden folder to keep track of changes.