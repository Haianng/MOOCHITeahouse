---
layout: default
title: Command Line Course
---

# Command Line Course

Welcome to my command line course notes. This page collects the main concepts, commands, and practical examples covered across four weekly modules.

[Back to MOOCHI Teahouse]({{ '/' | relative_url }})

---

## Module 1: Introduction to the Command Line

### Learning goals

- Understand what the command line is and why it is useful.
- Navigate directories and manage files.
- Learn basic commands and command-line help.

### Essential commands

| Command | What it does | Example |
|---|---|---|
| `pwd` | Prints the current working directory | `pwd` |
| `ls` | Lists files and directories | `ls -la` |
| `cd` | Changes directory | `cd Documents` |
| `mkdir` | Creates a directory | `mkdir practice` |
| `touch` | Creates an empty file | `touch notes.txt` |
| `cp` | Copies files | `cp notes.txt notes-backup.txt` |
| `mv` | Moves or renames files | `mv old.txt new.txt` |
| `rm` | Removes files | `rm old.txt` |

### Example: create a practice folder

```bash
mkdir command-line-practice
cd command-line-practice
touch notes.txt
pwd
ls -la
```

**Explanation:** `mkdir` creates a directory, `cd` enters it, and `touch` creates an empty file. `pwd` shows where you are, while `ls -la` lists files, including hidden ones.

> Be careful with `rm`: deleted files may not be easy to recover. Check the filename before running it.

---

## Module 2: Text Processing

### Learning goals

- Read and search text files.
- Filter and transform command output.
- Combine commands using pipes and redirection.

### Useful commands

| Command | Purpose | Example |
|---|---|---|
| `cat` | Displays file contents | `cat notes.txt` |
| `less` | Views a file page by page | `less notes.txt` |
| `head` | Shows the first lines | `head -n 5 notes.txt` |
| `tail` | Shows the last lines | `tail -n 5 notes.txt` |
| `grep` | Searches for matching text | `grep "error" log.txt` |
| `wc` | Counts lines, words, or bytes | `wc -l notes.txt` |
| `sort` | Sorts lines of text | `sort names.txt` |
| `uniq` | Removes adjacent duplicate lines | `sort names.txt \| uniq` |

### Example: search a log file

```bash
grep -i "error" application.log
```

**Explanation:** `grep` finds lines matching a pattern. The `-i` option makes the search case-insensitive, so it can match `ERROR`, `Error`, or `error`.

### Example: use a pipe

```bash
cat names.txt | sort | uniq
```

**Explanation:** The pipe symbol (`|`) sends one command's output to the next command. Here, the names are displayed, sorted, and then deduplicated.

### Example: redirect output

```bash
grep -i "error" application.log > errors.txt
```

**Explanation:** The `>` symbol sends output into `errors.txt`, creating the file or replacing its previous contents. Use `>>` to append instead.

---

## Module 3: Scripts, Configuration, and Installation

### Learning goals

- Understand shell scripts and executable permissions.
- Work with configuration files and environment variables.
- Install software using the appropriate package manager.

### Example: a simple shell script

Create a file named `hello.sh`:

```bash
#!/bin/bash

echo "Hello from the command line!"
date
pwd
```

Run it with:

```bash
bash hello.sh
```

Or make it executable:

```bash
chmod +x hello.sh
./hello.sh
```

**Explanation:** The first line identifies the interpreter. Each subsequent line runs a command. `chmod +x` adds execute permission, allowing the script to be launched directly.

### Environment variables

```bash
echo "$HOME"
echo "$PATH"
```

**Explanation:** `$HOME` usually points to your home directory. `$PATH` lists directories that the shell searches when you run a command.

To define a variable for the current shell session:

```bash
COURSE_NAME="Command Line Course"
echo "$COURSE_NAME"
```

### Configuration and installation

Configuration files control how programs behave. They may be stored in your home directory or in application-specific locations.

Before installing software, identify your operating system and follow the software's official installation instructions. For example, macOS users may use Homebrew if it is installed:

```bash
brew --version
brew install tree
```

**Explanation:** The first command checks whether Homebrew is available. The second installs the `tree` utility through Homebrew. If Homebrew isn't installed, follow its official setup instructions first.

---

## Module 4: Processes, SSH, and Git

### Learning goals

- Inspect and manage running processes.
- Understand remote access using SSH.
- Use Git to track changes and collaborate on projects.

### Process commands

| Command | Purpose | Example |
|---|---|---|
| `ps` | Lists processes | `ps aux` |
| `top` | Displays live process information | `top` |
| `kill` | Sends a signal to a process | `kill PID` |
| `jobs` | Lists jobs in the current shell | `jobs` |

**Explanation:** A process ID (PID) identifies a running process. Replace `PID` with the actual number when using `kill`. Try normal termination before considering stronger signals.

### Connecting with SSH

```bash
ssh username@server.example.com
```

**Explanation:** SSH creates an encrypted connection to a remote computer. Replace the example username and hostname with the details provided by your system administrator or service.

To create an SSH key pair:

```bash
ssh-keygen -t ed25519
```

**Explanation:** This generates an Ed25519 key pair. Keep the private key secret; only share the public key when a service asks for it.

### Essential Git commands

```bash
git status
git add cmdline_course.md
git commit -m "Add command line course notes"
git log --oneline
```

**Explanation:**

- `git status` shows changed and untracked files.
- `git add` stages a file for the next commit.
- `git commit` records the staged changes.
- `git log --oneline` shows a compact commit history.

### Example: working with a branch

```bash
git switch -c cmdline-course
```

This creates and switches to a branch named `cmdline-course`. A separate branch lets you develop the course page without making changes directly on the main development branch.

---

## Summary

Across these four modules, I learned how to navigate the command line, process text, write simple scripts, inspect processes, connect to remote systems, and manage changes with Git. Practising these commands helps build confidence with everyday development tasks.

## Further practice

1. Create a folder and several text files.
2. Search the files with `grep`.
3. Write a shell script that prints the date and current directory.
4. Create a Git branch and inspect the changes with `git status`.
