# Git Advanced Commands

This document provides a quick reference to some advanced Git commands that are helpful in managing your repository's history and workflow.

## 1. Rebase

**Syntax**: 
```bash
git rebase <branchName>
```

**Use**:  
The `git rebase` command rewrites the history of your repository. It applies the changes from your current branch on top of the specified branch, allowing you to maintain a clean commit history.

---

## 2. Squash

**Syntax**: 
```bash
git rebase -i HEAD~n
```

**Where**:  
`n` is the number of commits you want to squash.

**Use**:  
The `git rebase -i` (interactive) command allows you to merge multiple commits into a single, larger commit. This is useful for cleaning up commit history before merging a feature branch.

---

## 3. Reset

**Syntax**: 
```bash
git reset --soft HEAD~n
```

**Use**:  
The `git reset` command is used to remove a commit. The `HEAD~n` part refers to the number of commits you want to move back. You can choose different reset options to control what happens to your changes:

- **--soft**: The commit is undone, but the changes remain staged for a future commit.
- **--hard**: The commit is completely removed, along with all changes.
- **--mixed**: The commit is undone, but the changes are not staged (still present in the working directory).

---

## 4. Cherry-Pick

**Syntax**: 
```bash
git cherry-pick <commitHash>
```

**Use**:  
The `git cherry-pick` command is used to apply a specific commit from another branch to your current branch. This allows you to selectively include individual commits from other branches without merging the entire branch.

---

## 5. Tags

**Syntax**: 
```bash
git tag -a <tagName> "message for tag"
```

**Use**:  
Tags are used to mark specific points in the repository's history, such as a release or important checkpoint. 

To push the tag to the remote repository (e.g., GitHub), you need to use the following command:
```bash
git push origin <tagName>
```

---


