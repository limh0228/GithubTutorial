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
  - Go to your fork's repository on GitHub
  - Click the green **Clone** button. This will give you the project URL for your fork. Copy this URL.
  - In your shell, navigate to the directory where you would like to clone the project. If you are unfamiliar with navigating through the shell, use [this page](https://linuxize.com/post/linux-cd-command/) as a helpful guide to **cd**.
  - Type `git clone <project_url>`
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

If do not want to make a change to existing material, create your own file under the `supplementary_labs` folder, using the file `supplementary_labs/rebasing` as a template.

1. 
2. Open up the file you would like to make a change to in your local machine. Make your change, and save it.
3. Now, push your local change to your remote fork by running this command:
```
git push 
```
