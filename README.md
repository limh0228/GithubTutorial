# GitHub Workflows for Beginners

This tutorial will take you through a basic Git setup and workflow which most developers will use to contribute to repositories on GitHub. 
Once you have completed this lab, you should:
- understand the role of version control software in code development
- have a working Git setup on your machine
- be prepared to create basic changes to a GitHub project

Supplementary labs will introduce additional common Git commands and resources. Feel free to flag me down or message me if you have any questions! :)

## Getting started
1. First, make sure you have Git installed on your machine. To check if it is installed, open your shell of choice and type `git version`. This command should return your current version of Git. If it does not, you should go to [Git's Download Options](https://git-scm.com/downloads) and choose the download appropriate for your OS.
2. Go to Github and fork this repository, by navigating to [the project page](https://github.com/limh0228/GithubTutorial) and clicking the **Fork** button un the upper right.
> Hint: This creates a remote copy of the repository under your own account. This fork is connected to the original project, and is now ready for creating pull requests.
3. Open your shell again (Git Bash if using windows), and clone your personal fork to your local machine.
    -  Go to your fork's repository on GitHub
    - Click the green **Code** button. This will give you the project URL for your fork. Copy this URL.
    - In your shell, navigate to the directory where you would like to clone the project. If you are unfamiliar with navigating through the shell, use [this page](https://linuxize.com/post/linux-cd-command/) as a helpful guide to **cd**.
    - Clone your fork repository:
        ```
        git clone <project_url>
        ```
    - If you haven't used Git before, Git may ask you to configure your GitHub credentials. Do this by running the commands below, and then retry your clone command.
    
        ```
        git config ––global user.name “github_username”
        git config ––global user.email “email_address”
        ```
## Contributing a change
In this step, you will be making a change to your clone of this repository. Think of an improvement you could make to this project. Which steps did you find confusing? Did you ever feel like I had assumed too much about your knowledge of your system? Here are some examples:
- Fix a typo in this README to correct
- Add additional information to a step that confused you, or was not clear or specific enough
- Insert a helpful link
- Correct a mistake in my markdown styling
- Add more markdown styling to make the README more clear
- Add an additional note about OS specific corrections (i.e. in Windows, you will need to ...)

If do not want to make a change to existing material, create your own supplementary lab under the `supplementary_labs` folder, using the file `supplementary_labs/instructions` as a template. Look at the example `supplementary_labs/UnderstandingRebasing` for help.

1. In your shell, navigate to the repository clone you have made on your local machine.
2. Create a branch to encapsulate the changes you will make for your new "feature":
    
    ```
    git checkout -b "your_new_branch_name"
    ```
3. Now that you have made and switched to the new branch, make your change. Open up the file you would like to make a change to in your local machine, or alternatively, create you own supplementary lab under `supplementary_labs`. Make your change, and save it.
4. Run a git status to see your changes, and the filepaths of the files you have changed. Notice they are red because they have not been staged.
5. Stage your changes for commit by running the following command for every file you changed.
   
   ```
    git add <insert the filepath of changed file here>
    ```
6. Commit your staged changes, by running the following command just once:
   
   ```
    git commit -m "Write a descriptive commit message here about the changes you made"
    ```
7. Now, push your local change to your remote fork by running this command:
   
   ```
    git push origin <your branch name>
    ```
    The first time you run this command, the origin repository URL may not be set. To check if this is the case, use 
    
    ``` 
    git remote -v
    ```
    This command should tell you whetehr or not your "origin" alias is set to the correct repository. It should be set to the URL of your fork in GitHub. If it isn't, set it now in Git by running:
    
    ```
    git remote add origin <URL of your remote fork>
    ```
    Now retry the push command.
    At this point, if another student has modified the same line as you in the same file, you may get a merge conflict. Complete [this supplementary lab](supplementary_labs/ResolvingMergeConflicts.md) to resolve the merge conflict, and then retry the push command.
8. Open your remote repository on GitHub. On the main project page, there should be a new popup indicating that the branch containing your changes has been pushed from your local repository to your remote repository. Click the button that says `Compare and create pull request`. This will bring you to a menu showing you the commits encapsulated on this branch.
9. Once the pull request is submitted, I will need to approve it to merge it.

## Pulling after a merge
Once I have merged a pull request like yours, you will have pull the from the original remote project again to get the updated code. To pull from the upstream, first you will have to set the uptream alias by running:

    git remote add upstream <URL od the original remote repo>
    
jegfyudfuyawfwjhefbjwhebf
    ```
    git remote add upstream <URL of the original remote repo>
    ```
    
    Verify that the upstream URL was added correctly by running:
    
    ```
    git remote -v
    ```
    Now, you can pull the updated code from the upstream project into your local copy of the code.
    
    ```
    git pull upstream
    ```
You now have the most current version of the upstream project in your local machine, and if you navigate to where you made your change, you should see now that it has been incorporated! Great job!

## Additional materials
This lab is an extremely rudimentary look at the basics. Git has [hundreds of other advanced functionalities](https://git-scm.com/docs) which students will find extremely useful. Students who have finished the lab, should go complete at least one supplementary lab under the folder `supplementary_labs` which demonstrates one of these additional functions. Estimated time of completion for the supplementary labs is 5 minutes.

## Finally
Please let me know if you found this lab helpful. Especially let me know if you found this lab incomplete of confusing. Feedback is greatly appreciated. Thanks for your great work!
