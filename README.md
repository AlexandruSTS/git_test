# git_test
squash branches testing

# 1. Link a new project to GitHub.

## 1.1. Add remote origin:
    git remote add origin https://github.com/AlexandruSTS/Git_testing

## 1.2. Add all files to be tracked:
    git add .
    
## 1.3. Make a small change and do the first commit:
    git commit -am "first commit
    
## 1.4. Push your first commit to origin:
    git push -u origin main



# 2. Squash commits into a single commit

## 2.1. Start an Interactive Rebase:
    git rebase -i HEAD~2
### "2" stands for the number of commits that you want to squash

## 2.2. Squash Commits:
### Your default text editor will open with a list of the last two commits. It will look something like this:
    pick f7f3f6d Change my commit
    pick 310154e Another commit
### To squash the commits, change the word pick to squash (or just s) at the beginning of the second commit (or the one you want to squash into the first). ### It should now look like this:
    pick f7f3f6d Change my commit
    squash 310154e Another commit

## 2.3. Save and Exit:
### Save and exit the editor. Git will now attempt to squash the commits.
## 2.4. Create a New Commit Message:
### After saving, another editor window will open for you to create a commit message for the new squashed commit. Here you can write a new message or keep one of the existing messages.
## 2.5. Complete the Rebase:
### Save and exit the editor. Git will complete the rebase and squash your commits.
## 2.6. Force Push to Update Remote Repository:
### Since you've rewritten the commit history, you'll need to force push to update the remote repository:
    git push origin your-feature-branch --force
