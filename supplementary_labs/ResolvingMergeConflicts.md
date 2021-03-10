### Resolving merge conflicts in Git
Uh oh! You've got a merge conflict. Whether you have performed a pull or initiated your own merge, it seems that you are trying to unify two potentially conflicting versions of your project. 

Normally, Git will perform perfunctory merges for you, but updating files without conflicting changes (if only one person edited the file). However, for complicated merges, such as those containing changes by two different people on the same exact line, Git will ask you to help it resolve these conflicts, and help it choose which version of the code to keep.

[Link to additional documentation](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/resolving-a-merge-conflict-using-the-command-line)

### Follow these steps to try it out!
1. Open your code editor, and search for the conflict marker to see the beginning of the merge conflict: `<<<<<<<`.
2.  When you open the file in your text editor, you'll see the changes from the HEAD or base branch after the line `<<<<<<< HEAD`. Next, you'll see `=======`, which divides your changes from the changes in the other branch, followed by `>>>>>>> BRANCH-NAME`.
3. Now, resolve the merge by doing one of the following:
   - Choose a better version. If one revision completely replaces the other, choose the correct revision, and erase the other one. Delete all the merge markers like `<<<<<<<`, `<<<<<<< HEAD`, `=======`, and `>>>>>>> BRANCH-NAME`.
   - Combine the versions. If both chnages or some combination of bothe changes should be kept, write out your final, correct version, and delete all the merge markers.

   Make sure to save your changes.
4. Run the following command to see which files you have changed:

   ```
   git status
   ```
5. Stage your changes by running the following command for every file you resolved a merge conflict in. There may be multiple conflicts across multiple files.

   ```
   git add <filepath of changed file>
6. Commit your staged changes byt running the following:

   ```
   git commit -m "Resolved merge conflicts in <insert filename(s)>"
   ```
7. Now retry whatever command you were running which gave you the merge conflict in the first place.
8. For additional help, feel free to flag me over or send me a message.



