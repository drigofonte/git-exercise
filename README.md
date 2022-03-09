# git-exercise

This is a simple git exercise to explore functionality related to tags and trunk-development. Below are the steps I followed:

## Step 1

1. Create the project
2. `git tag -a v0.0.1 -m "First version"`
3. `git push origin v0.0.1`

## Step 2

1. Update the README.md to include the **Step 1** and **Step 2** sections
2. `git add .`
3. `git commit -m "Updated documentation"`
4. `git push origin main`
5. `git tag -a v1.0.0 -m "Second version"`
6. `git push origin v1.0.0`

## Step 3

1. `git checkout -b hotfix/1 v0.0.1`
2. Create v0.0.1.hotfix.md file with some content
3. `git add .`
4. `git commit -m "Created hotfix v0.0.2"`
5. `git push origin hotfix/1`
6. Create PR - assume no squash is needed after the PR is approved
7. Approve PR
8. Delete branch after approving PR
9. `git tag -a v0.0.2 -m "Hotfix v0.0.2"`
10. `git push origin v0.0.2`

## Step 4

1. `git checkout -b hotfix/2 v0.0.2`
2. Create v0.0.2.hotfix.md file with some content
3. `git add .`
4. `git commit -m "Created v0.0.2.hotfix.md"`
5. Update v0.0.2.hotfix.md file with some content
6. `git add .`
7. `git commit -m "Updated v0.0.2.hotfix.md"`
8. `git rebase -i HEAD~2` - squash the last commit into the first and change the message to 'Created hotfix v0.0.3'
9. `git push origin hotfix/2`
10. Create PR - assume no squash is needed after the PR is approved
11. Approve PR
12. Delete branch after approving PR
13. `git tag -a v0.0.3 -m "Hotfix v0.0.3"`
14. `git push origin v0.0.3`
