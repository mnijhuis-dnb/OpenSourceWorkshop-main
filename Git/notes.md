# Git Reset
- `--soft`: uncommit changes, changes are left staged (index).
- `--mixed` (default): uncommit + unstage changes, changes are left in working tree.
- `--hard`: uncommit + unstage + delete changes, nothing left.

# Staging
- staging helps you split up one large change into multiple commits
- staging helps in reviewing changes
- staging helps when a merge has conflicts
- staging helps you keep extra local files hanging around 
- staging helps you sneak in small changes

# The Three Trees
Git as a system manages and manipulates three trees ("collection of files") in its normal operation:

| Tree              | Role                              |
|-------------------|-----------------------------------|
| HEAD              | Last commit snapshot, next parent |
| Index             | Proposed next commit snapshot     |
| Working Directory | Sandbox                           |

## HEAD
HEAD is the pointer to the current branch reference, which is in turn a pointer to the last commit made on that branch. That means HEAD will be the parent of the next commit that is created. It’s generally simplest to think of HEAD as the snapshot of your last commit on that branch.

## The Index
The index is your proposed next commit. We’ve also been referring to this concept as Git’s “Staging Area” as this is what Git looks at when you run git commit.

## The Working Directory
Finally, you have your working directory (also commonly referred to as the “working tree”).