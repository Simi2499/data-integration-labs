<!-- Answer in `labs/02/shell.md`: for each question, the command you typed, its output in a code block, and your answer in one sentence.

1. **Which shell?** Which shell runs in your terminal, and which version is it? `echo $0` prints its name, `bash --version` or `zsh --version` its version.
2. **Where am I?** Which absolute path does your shell print for your home directory and for your downloads folder? On Windows, compare it with the path that File Explorer shows.
3. **Where do commands come from?** How many directories are in your `PATH`, and which one is searched first? Where are `curl`, `python3` and `git` installed? Run `git --version`, too: if Git is missing, install it before 06.11.26. On a Mac, `git --version` offers to install it for you.
4. **How full is your disk?** How much space is left on it, and how much space do your downloads take up?
5. **Stop a runaway process.** Run `sleep 600` in one terminal window: it does nothing for ten minutes, like a script that hangs. In a second window, find its process ID with `ps aux | grep sleep` and stop it with `kill` and the ID. What does the first window show? Why does `ps aux | grep sleep` list two processes?

Hint: one directory per line</summary>
`echo $PATH | tr ":" "\n"` puts each directory on a line of its own. Pipe the result into `wc -l` to count them, or into `head -n 1` to see the first one.
Hint: <code>ps aux</code> in Git Bash</summary>
The `ps` of Git Bash ignores `aux` and lists only program names, without their arguments. Use `ps -ef | grep sleep` there.
Answer in `labs/02/shell.md`: for each question, the command you typed, its output in a code block, and your answer in one sentence.
--> 

## 1. Which shell runs in your terminal, and which version is it?  \
  **shell**: \
  `echo $0`\
  `/usr/bin/bash`\
  On my Windows laptop I'm using GitBash. It gives me a Bash command line and common Unix tools, so I can run commands like `ls`, `grep`, and `git` without using Linux itself.
  
  **version**: \
  `bash --version`\
  `GNU bash, version 5.3.15(2)-release (x86_64-pc-cygwin)
Copyright (C) 2025 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html> \
This is free software; you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.` \
GitBash is using the version 5.3.15(2)-release (x86_64-pc-cygwin)

## 2. Which absolute path does your shell print for your home directory and for your downloads folder?  
`echo $HOME` \
`/c/Users/Simi24` \
My File Explorer shows the whole path for my home directory as `/c/Users/Simi24` and for the downloads folder as `/c/Users/Simi24/downloads`.

## 3. Where do commands come from? How many directories are in your `PATH`, and which one is searched first? Where are `curl`, `python3` and `git` installed?


 

