
## 3. Unstaged diff of notes.txt
diff --git a/part1/notes.txt b/part1/notes.txt
index 0bb61b6..6830305 100644
--- a/part1/notes.txt
+++ b/part1/notes.txt
@@ -1 +1,4 @@
 Git notes
+Git has a working directory.
+The staging area stores selected changes.
+A commit records a snapshot.

## 4. Staged diff of notes.txt
diff --git a/part1/notes.txt b/part1/notes.txt
index 0bb61b6..6830305 100644
--- a/part1/notes.txt
+++ b/part1/notes.txt
@@ -1 +1,4 @@
 Git notes
+Git has a working directory.
+The staging area stores selected changes.
+A commit records a snapshot.

## Difference between git fetch and git pull
git fetch downloads new commits and updates remote-tracking branches, but it does not modify the current local branch or working files.
git pull downloads remote changes and integrates them into the current local branch. It normally performs fetch followed by merge or rebase.

## Final status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	part1/status_log.md

nothing added to commit but untracked files present (use "git add" to track)
