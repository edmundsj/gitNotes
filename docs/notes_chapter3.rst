Chapter 3 Notes
==================
The git model saves "snapshots", not deltas. It saves the entire state of the filesystem using hashes.

Git apparently stores files as "blobs", which I'm guessing are just some compressed version of the original file or something?

A branch is nothing but a pointer that you can move around as you wish. I am adding a test hook here.

So apparently HEAD is a pointer that points to your current branch pointer? It's sort of a meta-pointer?

I'm going to add a line of code so I can commit now.
