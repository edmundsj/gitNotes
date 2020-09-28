Questions and Answers
=========================
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
