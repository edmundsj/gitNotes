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
