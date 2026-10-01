# Lab 4 Notes: Git and GitHub

## Question 1
`--global` stores the setting in my user-level config file (`~/.gitconfig`), so it applies to every repository on my computer. If I left it out, Git would save the setting only for the current repository (in `.git/config`). It would apply only to that repo, and outside a repository the command would fail.

## Question 2
`.git` appeared. It is a hidden folder (it starts with a dot), so plain `ls` does not show it. It is where Git stores everything about the repository: the full commit history and saved versions of files (`objects/`), branch info (`refs/`), the current branch pointer (`HEAD`), the repo's config, and hooks.

## Question 3
Git offered to track roughly **[N]** files and folders (fill in from your own `git status` output). Yes, some entries were not written by me: the `.venv/` folder (thousands of files of other people's installed packages) and `__pycache__/` folders, which Python generated automatically.

## Question 4
The `.venv/` entries (and other ignored items like `__pycache__/`, `*.pyc` and `.DS_Store`) disappeared from the untracked list. Only my own files plus `.gitignore` remain.

## Question 5
It should be committed, not ignored. `.gitignore` is part of the project: committing it means anyone who clones the repo (a TA, a teammate, me on another computer) gets the same ignore rules and does not accidentally add `.venv/` or other junk.

## Question 6
`README.md` moved from **Untracked files** to **Changes to be committed**. In the three-places model, it moved from the **working directory** to the **staging area** (index) with `git add`. It is not yet in the repository (committed history).

## Question 7
Git printed a line like `[main (root-commit) abc1234] Lab work so far`, followed by a summary such as `N files changed, X insertions(+)` and a list of `create mode 100644 <filename>` lines. It reported **[N]** files changed (fill in from your own output). `root-commit` shows this was the very first commit.

## Question 8
The first seven characters are the short **commit hash** (SHA), for example `abc1234`. It is a unique ID for that commit, used to refer to it, for example in `git show`, `git diff`, `git checkout` or `git revert`.
Question 9
The four steps of the Git loop are modifying or creating a file (edit), checking the repository state with git status, tracking the changes with git add (stage), and permanently saving the snapshot to your history with git commit.

Question 10
README.md gets a special name and is placed at the root of the project because it serves as the main instruction manual for your code. Platforms like GitHub are programmed to automatically detect this specific file and display its contents on the repository's front page.

Question 11
The gh auth login command securely authenticated your terminal with GitHub and saved an authentication token locally on your machine. Git uses this saved token to automatically verify your identity in the background, skipping the need for manual password entry.

Question 12
The contents of the README.md file are showing on the front page. GitHub automatically renders this file when anyone visits the repository to instantly provide them with a summary and context of what the project is about.

Question 13
No, pushing did not change your local history in any way. Pushing simply uploads a copy of your local commit history to the remote GitHub server so that the online repository matches what you already have on your computer.

Question 14
A private repository physically exists on GitHub's servers and is safely backed up online, but its access is strictly locked down to you and specific people you invite (like your TAs). If a repository doesn't exist on GitHub at all, it only lives locally on your personal computer's hard drive and cannot be accessed or shared over the internet.
