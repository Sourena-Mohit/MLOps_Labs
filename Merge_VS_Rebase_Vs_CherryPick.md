## Git Merge, Rebase, and Cherry-Pick

### 1. Merge
**Definition:**
Merge combines the changes from one branch into another. It creates a new commit that joins the history of both branches.

**Code Example:**
```bash
# Switch to the target branch
git checkout main

# Merge another branch into the current branch
git merge feature-branch
Resulting History:

*   Merge commit (main)
|\
| * Commit 2 (feature-branch)
| * Commit 1 (feature-branch)
* Commit A (main)
* Commit B (main)
A merge commit is created, preserving the commit history of both branches.

Usage Case:

Use merge when you want to combine changes from two branches while keeping the commit history clear and intact.
Ideal for team collaboration where the history of all contributors needs to be preserved.
2. Rebase
Definition: Rebase applies the commits of one branch on top of another branch. It rewrites the commit history to create a linear sequence.

Code Example:

# Switch to the branch you want to rebase
git checkout feature-branch

# Rebase it onto the target branch
git rebase main
Resulting History:

* Commit 2 (feature-branch, rebased)
* Commit 1 (feature-branch, rebased)
* Commit A (main)
* Commit B (main)
The commits from feature-branch are applied on top of main in a straight line.

Usage Case:

Use rebase to create a cleaner and linear commit history.
Ideal for personal branches or when collaborating in a small team to avoid unnecessary merge commits.
Warning: Avoid rebasing branches that have already been pushed and shared, as it rewrites history.
3. Cherry-Pick
Definition: Cherry-pick applies a specific commit from one branch to another without merging the entire branch.

Code Example:

# Switch to the target branch
git checkout main

# Cherry-pick a specific commit from another branch
git cherry-pick <commit-hash>
Resulting History:

* Commit 2 (cherry-picked, main)
* Commit A (main)
* Commit B (main)
Only the specified commit is added to main.

Usage Case:

Use cherry-pick when you want to apply specific changes from one branch to another without merging or rebasing the entire branch.
Ideal for hotfixes or when only part of the branch is relevant.
Comparison Table
Feature	Merge	Rebase	Cherry-Pick
Purpose	Combine two branches	Reapply commits onto a new base	Apply specific commit(s)
Commit History	Retains all branch histories	Linearizes commit history	Adds only selected commit(s)
New Commit?	Yes (merge commit)	No (reuses commits, changes hashes)	No
When to Use?	Collaboration, keep full history	Clean up history for smaller teams	Apply specific changes or fixes
Use Case Scenarios
Scenario 1: Collaborative Development (Use Merge)

Team members work on separate feature branches.
When features are ready, they are merged into main:
git checkout main
git merge feature-branch
git push origin main
This keeps the history intact, showing all team members’ contributions.
Scenario 2: Cleaning Up Personal Branches (Use Rebase)

You want to integrate main into your feature branch but avoid a merge commit:
git checkout feature-branch
git rebase main
After resolving conflicts, you push the rebased branch:
git push --force
This ensures a clean history for the final integration.
Scenario 3: Applying Specific Fixes (Use Cherry-Pick)

There’s a critical fix in a branch that needs to go into main without merging the branch:
git checkout main
git cherry-pick <commit-hash>
git push origin main
This avoids pulling in unrelated commits while integrating the necessary fix.