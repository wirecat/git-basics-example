# git-basics-example
The purpose of this repository is to show off the git flow for use in @wirecat's
"git basics" demonstration. This is a fork of @kfcampbells's "git basics"
demonstration with slight tweaks.

Test change, probably don't merge this.

## Usage
The facts folder contains a set of files listing information about those who
have done this workshop before. The goal is to add your own file to the facts
folder with information about yourself that you are comfortable sharing with
others. Please refer to [facts/wirecat.txt](facts/wirecat.md) for an example.

## Prerequisites
- Git installed on your machine.
  [Git](https://git-scm.com/downloads)
- A terminal or command line interface (CLI) to run git commands.
	- On Linux or Mac, the builtin terminal is fine.
	- On Windows, I recommend using the Git BASH terminal that comes with
	  the Git installation.
- A GitHub account.
  [GitHub Sign Up](https://github.com/signup).
- A registered SSH Key to your GitHub account.
  [GitHub Docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).

## Exercise
1. Fork this repository to your own GitHub account.
2. Clone your forked repository to your local machine.
3. Create a new branch for your changes.
4. Create a new file to the facts folder in the form of
   `{GitHubUsername}.md`.
5. Add your information to your file.
6. Stage your file for commit.
7. Commit your changes with a short commit message of what you've done.
8. Push your changes to your forked repository on GitHub.
9. Create a pull request to the original repository.
10. Wait for your pull request to be reviewed and merged.

## `git` command reference
### Cloning
- `git clone {repoURL}`
	- Clone a remote repository to your local machine.
	  [Offical docs](https://git-scm.com/docs/git-clone).

### Branching
- `git branch`
	- Show branches and see what branch you're on.
	  [Offical docs](https://git-scm.com/docs/git-branch).
- `git branch -D yourExistingBranch`
	- Delete a branch. Uppercase D to also pass --force, which allows us to
	  delete a branch that hasn't merged upstreatm. Only deletes local branches.
- `git checkout -b yourNewBranch`
	- Create a new branch and switch to it.
	  [Offical docs](https://git-scm.com/docs/git-checkout).
- `git checkout yourExistingBranch`
	- Switch to an existing branch.

### Commit loop
- `git status`
	- Shows what's changed since the last commit, what's staged, and more.
	  [Offical docs](https://git-scm.com/docs/git-status).
- `git add {fileOrPatternMatcher}`
	- Stage file(s) for commit. [Offical docs](https://git-scm.com/docs/git-add).
- `git restore --staged {fileOrPatternMatcher}`
	- Unstage file(s) from commit.
	  [Offical docs](https://git-scm.com/docs/git-restore).
- `git commit -m "{yourMessage}"`
	- Add a commit with a simple message.
	  [Offical docs](https://git-scm.com/docs/git-commit).
- `git revert -n HEAD~1..`
	- Reverts the last 1 local commits on current branch. Doesn't alter remote
	  state without further intervention.
	  [Offical docs](https://git-scm.com/docs/git-reset).

### Commit log
- `git log`
	- how all commits on a branch.
  	[Offical docs](https://git-scm.com/docs/git-log).
- `git show {commitSHAOrBranch}`
	- View details of a single commit.
  	[Offical docs](https://git-scm.com/docs/git-show).

## Remote sync
- `git pull`
	- Fetch changes from the remote and merge them into your local branch.
 	  [Offical docs](https://git-scm.com/docs/git-pull).
- `git push`
	- Push local changes to the remote.
  	  [Offical docs](https://git-scm.com/docs/git-push).
- `git remote  -v`
	- Show all remotes.
 	  [Offical docs](https://git-scm.com/docs/git-remote).

## Further Learning
- Adding a new SSH key to your GitHub account
  [GitHub Docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).
- GitHub pull request documentation.
  [GitHub Docs](https://docs.github.com/en/pull-requests).
- Beginner Git commands you need to know.
  [YouTube Video](https://www.youtube.com/watch?v=rE2zRhZdjFU).
- How to create a pull request in 4 min.
  [YouTube Video](https://www.youtube.com/watch?v=nCKdihvneS0).
- How to merge a pull request.
  [YouTube Video](https://www.youtube.com/watch?v=FDXSgyDGmho).
