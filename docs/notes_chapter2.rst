Chapter 2 Notes
==================

These are the notes for chapter 2 of the book "Pro Git"

The `git diff` command is used to explicitly ask which lines of which files you changed. It's like a more detailed `git status`. But it appears to only show unstaged changes, not staged ones. For that you want to use 

.. code-block::
   
    git diff --staged

This shows the difference between what is in your staging area and what is in your previous commit. So `git status` and `git status --staged` are both very useful.

.. code-block::

    git add -a

This command adds all previously tracked files. Is it the same as git add -u?


