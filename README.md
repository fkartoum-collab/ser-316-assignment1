# Number Guessing Project Documentation

## Branch Structure

main:
Stable production branch with the basic number guessing game.

dev:
Integration branch currently close to the basic game version and used to combine completed features.

feature1:
Adds quitting with negative input, play-again functionality, and improved user feedback.

feature2:
Adds a maximum attempts limit (10) and game-over behavior.

feature3:
Adds hints such as "you're very close" or "you're getting warmer" and reports how many attempts were needed.

hotfix:
Fixes random number generation so the maximum value can be selected.

## Learning Summary

merge:
Combines histories of two branches, preserves historical context but can be confusing and non-linear

rebase: 
Rewrites project history, applies commits on top of target branch. Flat, linear history graph.

squash: 
Condenses series of smaller commits to single clean commit with one message.

cherry-pick:
Extracts single commit by hash and applies as brand-new commit to current branch.

Observations in git history:
Feature1 integrated into dev using standard merge, non-linear loop. Feature2 updated using rebase, so it looks like feature2 changes were coded on top of latest dev commit. Feature3 has several messy commits, which were compressed to one clean commit, so conflict only had to be dealt with once.

When to use each:
Merge is used when integrating major branches such as dev into main where an accurate timeline is critical. Rebase is used for local private feature branches. Squash would be used before merging feature branch into shared integration branch. Cherry-pick would be used for emergency production hotfixes to avoid pulling in unfinished features.