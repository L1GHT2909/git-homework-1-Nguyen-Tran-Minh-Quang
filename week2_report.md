PART A
1.
touch week2.md
touch week2_report.md
git add week2.md week2_report.md
git commit -m "Create week2 files"
git switch -c week2
2.
echo "Content from working 1" >> week2.md
git add week2.md
git commit -m "working 1"

echo "Content from working 2" >> week2.md
git add week2.md
git commit -m "working 2"
3.
echo "Final content on week2 branch" >> week2.md
git add week2.md
git commit -m "Add final line to week2"

git switch master

echo "After switching to master, the new content from week2 branch is not visible because the commits only belong to the week2 branch." >> week2_report.md
git add week2_report.md
git commit -m "Document findings about week2 file"
4.
git switch -c week2b
git merge --no-ff week2 -m "Merge week2 into week2b"
git branch -d week2

