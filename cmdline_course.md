---
layout: default
title: Command Line Course
---

<div class="course-page">

<section class="course-hero">
  <p class="eyebrow">LEARN · EXPLORE · CREATE</p>
  <h1>Command-Line Course</h1>
  <p class="course-lead">
    A practical guide to the tools behind everyday computing,
    from navigating files to publishing a website.
  </p>
  <a class="moochi-button" href="{{ '/' | relative_url }}">Back to MOOCHI</a>
</section>

<section class="course-intro">
  <p class="eyebrow">THE COURSE</p>
  <h2>Small commands, powerful tools.</h2>
  <p>
    These notes collect the main concepts, commands, and practical
    examples covered across four weekly modules. Each module introduces
    essential tools and reflects on how they can support everyday
    computing and development work.
  </p>
</section>

<figure style="margin: 2rem 0;">
  <img src="{{ '/assets/images/study-photo.jpg' | relative_url }}" alt="A quiet study moment with a laptop, coffee, and a book" style="display: block; width: 100%; max-width: 720px; height: auto; margin: 0 auto; border-radius: 8px;">
  <figcaption style="text-align: center; color: #667783; font-size: 0.9rem; margin-top: 0.75rem;">A quiet moment for learning and exploring new tools.</figcaption>
</figure>

<section class="course-module">
  <p class="eyebrow">WEEK 01</p>
  <h2>Introduction to the Command Line</h2>
  <p>
    The command line provides a text-based way to interact with a
    computer. This week focuses on navigating directories, managing
    files, and learning basic commands.
  </p>

  <h3>Learning goals</h3>
  <ul>
    <li>Understand what the command line is and why it is useful.</li>
    <li>Navigate directories and manage files.</li>
    <li>Learn basic commands and command-line help.</li>
  </ul>

  <h3>Essential commands</h3>
<table class="course-table">
<thead><tr><th>Command</th><th>What it does</th><th>Example</th></tr></thead>
<tbody>
<tr><td><code>pwd</code></td><td>Prints the current working directory.</td><td><code>pwd</code></td></tr>
<tr><td><code>ls</code></td><td>Lists files and directories.</td><td><code>ls -la</code></td></tr>
<tr><td><code>cd</code></td><td>Changes directory.</td><td><code>cd Documents</code></td></tr>
<tr><td><code>mkdir</code></td><td>Creates a directory.</td><td><code>mkdir practice</code></td></tr>
<tr><td><code>touch</code></td><td>Creates an empty file.</td><td><code>touch notes.txt</code></td></tr>
<tr><td><code>cp</code></td><td>Copies files.</td><td><code>cp notes.txt notes-backup.txt</code></td></tr>
<tr><td><code>mv</code></td><td>Moves or renames files.</td><td><code>mv old.txt new.txt</code></td></tr>
<tr><td><code>rm</code></td><td>Removes files.</td><td><code>rm old.txt</code></td></tr>
</tbody></table>
<h3>Example: create a practice folder</h3>
  <table class="course-table">
    <thead><tr><th>Command</th><th>Explanation</th></tr></thead>
    <tbody>
      <tr><td><code>mkdir command-line-practice</code></td><td>Creates a new practice directory.</td></tr>
      <tr><td><code>cd command-line-practice</code></td><td>Moves into that directory.</td></tr>
      <tr><td><code>touch notes.txt</code></td><td>Creates an empty text file.</td></tr>
      <tr><td><code>pwd</code></td><td>Shows the current directory.</td></tr>
      <tr><td><code>ls -la</code></td><td>Lists files, including hidden files.</td></tr>
    </tbody>
  </table>
  <p class="course-explanation">
    These commands demonstrate how several simple operations can be
    combined into a practical workflow for creating and exploring files.
  </p>
  <blockquote>
    Be careful with <code>rm</code>: deleted files may not be easy to
    recover. Check the filename before running it.
  </blockquote>
  <p class="course-reflection">
    <strong>Reflection.</strong> I learned how to navigate the filesystem
    and manage files using commands instead of relying entirely on a
    graphical interface.
  </p>
</section>

<section class="course-module">
  <p class="eyebrow">WEEK 02</p>
  <h2>Text Processing</h2>
  <p>
    Text-processing tools help us read files, search for information,
    filter results, and combine commands to work efficiently with text.
  </p>

  <h3>Useful commands</h3>
<table class="course-table">
<thead><tr><th>Command</th><th>Purpose</th><th>Example</th></tr></thead>
<tbody>
<tr><td><code>cat</code></td><td>Displays file contents.</td><td><code>cat notes.txt</code></td></tr>
<tr><td><code>less</code></td><td>Views a file page by page.</td><td><code>less notes.txt</code></td></tr>
<tr><td><code>head</code></td><td>Shows the first lines.</td><td><code>head -n 5 notes.txt</code></td></tr>
<tr><td><code>tail</code></td><td>Shows the last lines.</td><td><code>tail -n 5 notes.txt</code></td></tr>
<tr><td><code>grep</code></td><td>Searches for matching text.</td><td><code>grep "error" log.txt</code></td></tr>
<tr><td><code>wc</code></td><td>Counts lines, words, or bytes.</td><td><code>wc -l notes.txt</code></td></tr>
<tr><td><code>sort</code></td><td>Sorts lines of text.</td><td><code>sort names.txt</code></td></tr>
<tr><td><code>uniq</code></td><td>Removes adjacent duplicate lines.</td><td><code>sort names.txt | uniq</code></td></tr>
</tbody></table>
<h3>Searching and filtering</h3>
  <table class="course-table">
    <thead><tr><th>Command</th><th>Explanation</th></tr></thead>
    <tbody>
      <tr>
        <td><code>grep -i "error" application.log</code></td>
        <td>Finds lines containing “error”, regardless of letter case.</td>
      </tr>
      <tr>
        <td><code>cat names.txt | sort | uniq</code></td>
        <td>Displays the names, sorts them, and removes adjacent duplicates after sorting.</td>
      </tr>
      <tr>
        <td><code>grep -i "error" application.log &gt; errors.txt</code></td>
        <td>Writes matching lines to <code>errors.txt</code>, replacing its previous contents if it exists.</td>
      </tr>
      <tr>
        <td><code>grep -i "error" application.log &gt;&gt; errors.txt</code></td>
        <td>Appends matching lines to the end of the file.</td>
      </tr>
    </tbody>
  </table>

  <p class="course-explanation">
    A pipe (<code>|</code>) passes one command's output to another.
    Redirection with <code>&gt;</code> writes output to a file, while
    <code>&gt;&gt;</code> appends output.
  </p>

  <p class="course-reflection">
    <strong>Reflection.</strong> I learned that combining small tools
    makes it easier to search, filter, and organize large amounts of
    text without manually opening every file.
  </p>
</section>

<section class="course-module">
  <p class="eyebrow">WEEK 03</p>
  <h2>Scripts, Configuration, and Installation</h2>
  <p>
    Shell scripts group commands into reusable workflows. Configuration
    files and environment variables help programs determine how to run,
    while package managers simplify software installation.
  </p>

  <h3>Example: a simple shell script</h3>
  <p>Create a file called <code>hello.sh</code> containing:</p>
  <table class="course-table">
    <thead><tr><th>Script code</th><th>Explanation</th></tr></thead>
    <tbody>
      <tr>
        <td><pre><code>#!/bin/bash
echo "Hello from the command line!"
date
pwd</code></pre></td>
        <td>The first line identifies Bash as the interpreter. The remaining lines print a message, display the date, and show the current directory.</td>
      </tr>
    </tbody>
  </table>

  <h3>Running a script</h3>
  <table class="course-table">
    <thead><tr><th>Command</th><th>Purpose</th></tr></thead>
    <tbody>
      <tr><td><code>bash hello.sh</code></td><td>Runs the script using Bash.</td></tr>
      <tr><td><code>chmod +x hello.sh</code></td><td>Adds execute permission to the file.</td></tr>
      <tr><td><code>./hello.sh</code></td><td>Runs the executable script from the current directory.</td></tr>
    </tbody>
  </table>

  <h3>Environment variables</h3>
  <table class="course-table">
    <thead><tr><th>Command</th><th>Purpose</th></tr></thead>
    <tbody>
      <tr><td><code>echo "$HOME"</code></td><td>Displays the home directory path.</td></tr>
      <tr><td><code>echo "$PATH"</code></td><td>Displays the directories searched when looking for commands.</td></tr>
      <tr><td><code>COURSE_NAME="Command Line Course"</code></td><td>Defines a variable in the current shell session.</td></tr>
      <tr><td><code>echo "$COURSE_NAME"</code></td><td>Prints the variable's value.</td></tr>
    </tbody>
  </table>

  <h3>Configuration and installation</h3>
  <table class="course-table">
    <thead><tr><th>Command</th><th>Purpose</th></tr></thead>
    <tbody>
      <tr><td><code>brew --version</code></td><td>Checks whether Homebrew is available and displays its version.</td></tr>
      <tr><td><code>brew install tree</code></td><td>Installs the <code>tree</code> utility using Homebrew.</td></tr>
    </tbody>
  </table>
  <p class="course-explanation">
    Configuration files control how programs behave. Their locations
    depend on the operating system and application. On macOS, Homebrew
    is one option for installing software, if it is already installed.
    Otherwise, follow its official setup instructions first.
  </p>

  <p class="course-reflection">
    <strong>Reflection.</strong> I learned how scripts make repeated
    tasks easier to run and how environment variables and configuration
    settings affect the command-line environment.
  </p>
</section>

<section class="course-module">
  <p class="eyebrow">WEEK 04</p>
  <h2>Processes, SSH, and Git</h2>
  <p>
    This module introduces process management, remote access, and
    version control. These tools are useful for troubleshooting,
    connecting to other computers, and managing software projects.
  </p>

  <h3>Process commands</h3>
<table class="course-table">
<thead><tr><th>Command</th><th>Purpose</th><th>Example</th></tr></thead>
<tbody>
<tr><td><code>ps</code></td><td>Lists processes.</td><td><code>ps aux</code></td></tr>
<tr><td><code>top</code></td><td>Displays live process information.</td><td><code>top</code></td></tr>
<tr><td><code>kill</code></td><td>Sends a signal to a process.</td><td><code>kill PID</code></td></tr>
<tr><td><code>jobs</code></td><td>Lists jobs in the current shell.</td><td><code>jobs</code></td></tr>
</tbody></table>
<h3>Connecting with SSH</h3>
  <table class="course-table">
    <thead><tr><th>Command</th><th>Explanation</th></tr></thead>
    <tbody>
      <tr>
        <td><code>ssh username@server.example.com</code></td>
        <td>Opens an encrypted connection to a remote computer. Replace the example username and hostname with the details provided by your service.</td>
      </tr>
      <tr>
        <td><code>ssh-keygen -t ed25519</code></td>
        <td>Generates an Ed25519 SSH key pair. Keep the private key secret and share only the public key when requested.</td>
      </tr>
    </tbody>
  </table>

  <h3>Essential Git commands</h3>
  <table class="course-table">
    <thead><tr><th>Command</th><th>Purpose</th></tr></thead>
    <tbody>
      <tr><td><code>git status</code></td><td>Shows changed and untracked files.</td></tr>
      <tr><td><code>git add cmdline_course.md</code></td><td>Stages the course file for a commit.</td></tr>
      <tr><td><code>git commit -m "Add command line course notes"</code></td><td>Records staged changes in the repository history.</td></tr>
      <tr><td><code>git log --oneline</code></td><td>Shows a compact commit history.</td></tr>
      <tr><td><code>git switch -c cmdline-course</code></td><td>Creates and switches to a new branch named <code>cmdline-course</code>.</td></tr>
    </tbody>
  </table>

  <p class="course-explanation">
    A separate Git branch allows development to happen independently
    before changes are merged into the main branch.
  </p>

  <p class="course-reflection">
    <strong>Reflection.</strong> I learned how to inspect running
    processes, understand remote connections, and use Git to track
    changes and organize development work.
  </p>
</section>

<section class="course-summary">
  <p class="eyebrow">LOOKING BACK</p>
  <h2>From commands to confidence.</h2>
  <p>
    Across these four modules, I learned how to navigate the command
    line, process text, write simple scripts, inspect processes,
    connect to remote systems, and manage changes with Git. Practising
    these tools helps build confidence with everyday development tasks.
  </p>

  <h3>Further practice</h3>
  <ol>
    <li>Create a folder and several text files.</li>
    <li>Search the files with <code>grep</code>.</li>
    <li>Write a shell script that prints the date and current directory.</li>
    <li>Create a Git branch and inspect changes with <code>git status</code>.</li>
  </ol>
</section>

</div>