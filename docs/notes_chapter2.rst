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

Questions and Answers
------------------------
Q: Does un-staging a file using git reset do anything to my local files?
A: No, only git reset --hard does this.

Q: How do I remove a file from git and my local directory?
A:
.. code-block::

    git rm <FILENAME>

Q: How do I fix a commit I already made?
A: Do whatever additional stuff you want to do, and then run: 
.. code-block::

    git commit --amend

This will allow you to "amend" your previous commit (and its message). It's a way to edit commits after the fact.

Q: How do I remove a file from git without removing it from my local directory?
A: 
.. code-block::

    git rm --cached FILENAME

Q: I made a change to one of my files that I want to undo, and I don't want git to track it. 
A: The following code destroys any of the changes you made that have not yet been staged for a commit:
.. code-block::

    git checkout -- <FILENAME>

Q: How do I get data from a remote repository without merging it with my local stuff? Where is that located?
A: 
.. code-block::

    git fetch origin

Should do this. I'm not sure then how to merge stuff.
