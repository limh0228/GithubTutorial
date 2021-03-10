### Checking your Git status
The status command in git will reveal several pieces of useful information about the current status of any Git repository. It will show users the following information:
+ Which files have been changed
+ Which files have been staged
+ Which files have been committed
+ What branch you are currently on

Example usage:
```
git status
```

[Link to additional documentation](https://git-scm.com/docs/git-status)

## Follow these steps to try it out!
1. First, open your terminal, and naviagte to a project repository.
2. Run the command:

   ```
   git status
   ```
   Notice that this command will tell you what branch you are currently on
3. Make a change to a file. (The change may be trivial, you can undo this change later). Save your change.
4. Run the command again:

   ```
   git status
   ```
   Notice that the status will show you which file was changed. The filename should be red.
  
5. Stage the changed file by running:

   ```
   git add <filepath>
   ```
6. Run the command again:

   ```
   git status
   ```
   Notice that the status will show you which file was staged. The filename should be green now.
