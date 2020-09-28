Chapter 3 Notes
==================
The git model saves "snapshots", not deltas. It saves the entire state of the filesystem using hashes.

Git apparently stores files as "blobs", which I'm guessing are just some compressed version of the original file or something?

A branch is nothing but a pointer that you can move around as you wish. I am adding a test hook here.

So apparently HEAD is a pointer that points to your current branch pointer? It's sort of a meta-pointer?

I'm going to add a line of code so I can commit now.

Branches can diverge - right now I'm making additional commits on the chapter3 branch, but I've also made some extra commits not seen by my testing branch on the master branch.

WOW - branching in git is as cheap as writing 41 bytes to a file - all a branch is storing is a pointer to a particular commit. That's so cheap.

It looks like when you switch branches you can no longer see the commits of the other branch which is "ahead" of you. No reason to fear, just switch back to the other branch.

Apparently when you try to merge from two branches with divergent history, git attempts to find the most recent common ancestor and do the merge automatically. It then creates a commit which represents that merge. If it isn't able to merge, it will ask you to fix conflicts and then create a merge commit manually. Once you perform that commit everything will be all good.

OK, so here's an outline of my desired git workflow:
1. Setup a git repository. Create a "develop" branch and switch to it.
2. Setup your build so that every time you commit your core (fast) unit tests are run and your documentation is generated via git hooks.
3. Setup your build so that every time you push, your entire unit test suite (all integration tests) are run via git hooks.
General workflow notes
------------------------
- NEVER work directly on the master branch. This should be your stable codebase
- ALWAYS work on the 'develop' branch.
- Whenever possible, create branches off the develop branch for particular features you are working on.
- Merge the develop branch into the master branch once you have a stable codebase and are content with the changes.

7. Go back to the develop branch, create additional feature branches as needed and continually merge them back into master.
