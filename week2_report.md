<<<<<<< Updated upstream
# PART A

## 1.

```bash
=======
PART A
1.
>>>>>>> Stashed changes
touch week2.md
touch week2_report.md
git add week2.md week2_report.md
git commit -m "Create week2 files"
git switch -c week2
<<<<<<< Updated upstream
```

## 2.

```bash
=======
2.
>>>>>>> Stashed changes
echo "Content from working 1" >> week2.md
git add week2.md
git commit -m "working 1"

echo "Content from working 2" >> week2.md
git add week2.md
git commit -m "working 2"
<<<<<<< Updated upstream
```

## 3.

```bash
=======
3.
>>>>>>> Stashed changes
echo "Final content on week2 branch" >> week2.md
git add week2.md
git commit -m "Add final line to week2"

<<<<<<< Updated upstream
git switch main

echo "After switching to main, the new content from the week2 branch is not visible because the commits only belong to the week2 branch." >> week2_report.md
git add week2_report.md
git commit -m "Document findings about week2 file"
```

After switching from `week2` to `main`, the changes made on the `week2` branch were no longer visible. This happened because each branch points to a different commit history. The new lines were committed only on the `week2` branch and had not yet been merged into `main`.

## 4.

```bash
git switch -c week2b
git merge --no-ff week2 -m "Merge week2 into week2b"
git branch -d week2
```

The merge was a three-way merge because both branches contained different commits created after their common ancestor.

# PART B

## 1.

```bash
git switch -c wip

=======
git switch master

echo "After switching to master, the new content from week2 branch is not visible because the commits only belong to the week2 branch." >> week2_report.md
git add week2_report.md
git commit -m "Document findings about week2 file"
4.
git switch -c week2b
git merge --no-ff week2 -m "Merge week2 into week2b"
git branch -d week2

PART B
1.
git switch -c wip
>>>>>>> Stashed changes
echo "Initial work in progress" > wip.txt
git add wip.txt
git commit -m "Create wip file"

<<<<<<< Updated upstream
git switch main
git merge week2b
```

## 2.

```bash
git branch --merged
git branch --no-merged
```

Output of `git branch --merged`:

```text
* main
  week2b
```

Output of `git branch --no-merged`:

```text
wip
```

The `week2b` branch appeared in the merged list because its work had already been merged into `main`. The `wip` branch appeared in the unmerged list because its new commit was not yet part of `main`.

## 3.

```bash
git branch -d week2b
```

## 4.

```bash
git branch -m wip work-in-progress
git push -u origin work-in-progress
```

The local branch `wip` was renamed to `work-in-progress`. The renamed branch was then published to GitHub and connected to the remote branch `origin/work-in-progress`.

# PART C

## 1.

```bash
git switch work-in-progress

=======
git switch master
git merge week2b
2.
echo "Merged branches:" >> week2.md
git branch --merged >> week2.md

echo "Unmerged branches:" >> week2.md
git branch --no-merged >> week2.md

git add week2.md
git commit -m "Document merged and unmerged branches"
3.
git branch -d week2b
4.
git branch -m wip work-in-progress
git push -u origin work-in-progress

Nếu trước đó đã từng push nhánh wip lên GitHub:

git push origin --delete wip
PART C
1.
git switch work-in-progress
>>>>>>> Stashed changes
echo "More work completed on this branch" >> wip.txt
git add wip.txt
git commit -m "Update work in progress"
git push
<<<<<<< Updated upstream
```

## 2.

```bash
git branch -vv
```

The `git branch -vv` command displays every local branch, its latest commit, its upstream remote branch, and whether it is ahead of or behind the upstream branch.

## 3.

```bash
git push -u origin work-in-progress
```

A pull request was created on GitHub with the following branches:

```text
base: main
compare: work-in-progress
```

The pull request proposes merging the changes from `work-in-progress` into `main`.

# PART D

## 1.

```bash
git switch main
git switch -c experiment

echo "First experiment" > experiment1.txt
git add experiment1.txt
git commit -m "Add first experiment"

echo "Second experiment" > experiment2.txt
git add experiment2.txt
git commit -m "Add second experiment"
```

## 2.

```bash
git switch main

echo "New work on main" > master-work.txt
git add master-work.txt
git commit -m "Add new file on main"
```

## 3.

```bash
git switch experiment
git rebase main
```

## 4.

Before the rebase, the `main` and `experiment` branches had diverged. The `main` branch contained one new commit, while the `experiment` branch contained two separate commits.

When the following command was executed:

```bash
git rebase main
```

Git temporarily removed the two commits from the `experiment` branch. It then moved `experiment` to the latest commit on `main` and applied the two experiment commits again.

As a result:

- The commit history became linear.
- No merge commit was created.
- The experiment commits received new commit hashes.
- The experiment commits were placed after the latest commit on `main`.

The explanation was then committed to the report:

```bash
git add week2_report.md
git commit -m "Document rebase results"
```

## 5.

```bash
git switch main
git merge experiment
```

The merge was completed using fast-forward. After the rebase, `main` was a direct ancestor of `experiment`, so Git only needed to move the `main` pointer forward. No additional merge commit was required.

## 6.

```bash
git push origin main
```

## 7.

```bash
git add week2_report.md
git commit -m "Complete week 2 report"
git push origin main
```
=======
2.
git branch -vv
3.
git push -u origin work-in-progress
>>>>>>> Stashed changes
