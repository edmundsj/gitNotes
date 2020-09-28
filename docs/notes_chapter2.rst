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

Apparently, you *can* lose information when undoing things - I suspect this is what happened with my RCWA stuff. I need to figure out which 'undos' are permanent and which are not. 

Looks like "git pull" is an alias for fetch, which grabs from a remote repository, and then "git merge", which merges the fetched information with your local stuff. Fetching the remote repository doesn't do anything to your local stuff.
