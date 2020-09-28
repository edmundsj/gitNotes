Chapter 2 Notes
==================
The git model saves "snapshots", not deltas. It saves the entire state of the filesystem using hashes.

Git apparently stores files as "blobs", which I'm guessing are just some compressed version of the original file or something?

A branch is nothing but a pointer that you can move around as you wish. I am adding a test hook here.

It looks like when you switch branches you can no longer see the commits of the other branch which is "ahead" of you. No reason to fear, just switch back to the other branch.
