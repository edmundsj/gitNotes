Chapter 2 Notes
==================

These are the notes for chapter 2 of the book "Pro Git"

The `git diff` command is used to explicitly ask which lines of which files you changed. It's like a more detailed `git status`. But it appears to only show unstaged changes, not staged ones. For that you want to use 

.. code-block::
   
    git diff --staged

This shows the difference between what is in your staging area and what is in your previous commit. So `git status` and `git status --staged` are both very useful.

.. code-block::

    git commit -a

This command adds all previously tracked files and commits them in the same command. Is it the same as git add -u, followed by a command?

Now for a dangerous command:

.. code-block::
   
    git rm FILENAME

This not only removes a file from being tracked in git, but ALSO deletes it in your actual filesystem, too. It doesn't just "un-track" the file. How do I un-track a file? Using that command, but with the --cached flag:

.. code-block::

    git rm --cached FILENAME


Then, you can add the file to your .gitignore and everything will be hunky-dory. You can also explicitly rename files with git using the "git mv" command. 
