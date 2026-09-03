# Lab 03: Git and GitHub
This repository documents my practice with 
local Git, GitHub, branches, and pull requests.

## README Responses

### 1.1 After initialization
```
ls -la
...total 12
drwxr-xr-x 3 dnldng dnldng 4096 Sep  3 10:35 .
drwxr-xr-x 6 dnldng dnldng 4096 Sep  3 10:33 ..
drwxr-xr-x 6 dnldng dnldng 4096 Sep  3 10:33 .git
-rw-r--r-- 1 dnldng dnldng    0 Sep  3 10:35 README.md...
```
### 1.2 First git status
```
git status
...On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)...
```

### 1.3 After the first commit

```
git status
...On branch main
nothing to commit, working tree clean...
```

### 1.4 git log

```
git log --oneline
...ca8c82c (HEAD -> main) Create lab README...
```

### 1.5 git diff

Paste the `git status` and `git diff` commands and their output.

```
git status
...On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")...
```

```
git diff
...diff --git a/README.md b/README.md
index 7e8e5d5..44c06ba 100644
--- a/README.md
+++ b/README.md
@@ -1,4 +1,6 @@
 # Lab 03: Git and GitHub
+This repository documents my practice with ^M
+local Git, GitHub, branches, and pull requests.^M

 ## README Responses

@@ -27,12 +29,26 @@ nothing added to commit but untracked files present (use "git add" to track)...

 ### 1.3 After the first commit

-
+```^M
+git status^M
+...On branch main^M
+nothing to commit, working tree clean...^M
+```^M

 ### 1.4 git log

+```^M
+git log --oneline^M
+...ca8c82c (HEAD -> main) Create lab README...^M
+```^M
+^M
:...
```

How does this `git status` differ from the one in **1.2**?
The get status of 1.5 differs from 1.2 in that 1.5 says that the README file is unstaged for a commit whereas in 1.2 it was untracked.

### 1.6 Git command reflections

In one or two sentences each, what does each command do?

- `git init`
It creates an empty local repo
- `git status`
Tells you the current directory and staging.
- `git add`
Moves changes from working dir to git staging.
- `git commit`
Makes a save point on the local dir of changes.
- `git log`
Returns commit history
- `git diff`
Lists changes between the working dir and the staging.
### 1.7 Repository link

https://github.com/gdelong4/lab03-exercises

### 1.8 Comparing approaches

In your own words:

- How does the nested-loop approach check for a duplicate?
- How does the set-based approach check for a duplicate?
- What is the runtime and memory trade-off of each?

### 1.9 Pull request merge options

In your own words, what does each GitHub merge option do?

- Create a merge commit
- Squash and merge
- Rebase and merge