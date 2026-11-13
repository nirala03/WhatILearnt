# Git Fundamentals — Repository and Revision Management

## Introduction

Git is a distributed version control system used to record changes made to files over time. It allows developers to preserve earlier versions of a project, inspect modifications, and manage the development history.

This directory contains the practical work for the Git Basics assignment in TW Lab 2025. The exercise uses a small sample project to demonstrate the commands involved in maintaining a local repository.

The work was carried out in a Linux-like environment using Windows Subsystem for Linux (WSL).

## Sample Project

The assignment uses two files for experimentation:

- `readme.txt` — A text file used to practise staging, modification, committing, and removal.
- `vecadd.py` — A Python program intended to accept two vectors and calculate their dot product.

The terminal operations were recorded through screenshots, accompanied by short descriptions of the actions performed.

## Operations Performed

### Repository Creation and Configuration

The first stage involves creating a project directory and initializing Git:

```bash
git init
```

Repository-specific identity information is then configured:

```bash
git config user.name "Your Name"
git config user.email "username@provider.com"
```

This information is associated with commits made in the repository.

### Adding and Recording Files

A text file is created and placed in Git's staging area:

```bash
git add readme.txt
git status
```

After checking the repository state, the staged content is recorded as a commit:

```bash
git commit -m "Adding first file."
```

This demonstrates the distinction between having a file in the working directory, preparing it for a commit, and saving it in the repository history.

### Examining Modifications

After the contents of the text file are changed, the following command is used:

```bash
git diff
```

It displays modifications that have not yet been staged, making it easier to inspect changes before recording them.

### Undoing Local Changes

The exercise explores `git restore` in two situations: when a file has been modified but not staged, and when changes have already entered the staging area.

```bash
git restore readme.txt
git restore --staged readme.txt
```

The first command restores the working-tree copy of the file, while the second removes the staged changes from the index. These operations demonstrate why the working directory and staging area need to be understood separately.

### Inspecting Repository History

The commit history can be examined with:

```bash
git log
```

The displayed information includes commit identifiers and details that can be used to locate earlier revisions.

### Reversing a Recorded Change

The assignment introduces:

```bash
git revert <commit-hash>
```

Rather than erasing an existing commit, this command creates another commit that applies the inverse of the selected change. The earlier entry remains part of the history.

### Adding the Python Program

The `vecadd.py` source file is added to the repository and committed. This applies the same version-control workflow to a program rather than only a text document.

### Removing a Tracked File

The text file is removed with:

```bash
git rm readme.txt
```

The deletion is subsequently committed so that it becomes part of the repository's recorded history.

### Visiting an Earlier Revision

The exercise also uses:

```bash
git checkout <commit-hash>
```

This changes the checked-out project state to an earlier commit, allowing its files to be inspected.

A checkout of a commit hash does not create a new commit to undo the selected changes. It can place the repository in a detached HEAD state, which is different from returning to a branch.

To return to the latest branch version, the branch name can be checked out:

```bash
git checkout <branch-name>
```

## Important Distinctions

Two comparisons are especially useful when learning these commands:

- **Restore versus revert:** `git restore` deals with changes in the working tree or staging area, whereas `git revert` records an inverse change as a new commit.
- **Revert versus checkout:** Reverting changes the history by adding a new commit; checking out an older commit changes which revision is currently being viewed.

Understanding these differences helps prevent accidental loss of work and makes repository operations easier to reason about.

## Submission Material

The assignment submission includes a PDF containing terminal screenshots and explanations of the steps. It records the repository setup, file operations, commit history, and experiments with earlier revisions.

## Takeaway

This exercise introduces the basic Git workflow and the role of version control in software development. It demonstrates that Git is not simply a tool for saving files; it provides a structured way to record, inspect, and navigate the evolution of a project.