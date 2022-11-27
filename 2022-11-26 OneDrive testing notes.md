# 2022-11-26 OneDrive testing notes

Today's testing involves using a vault that resides on a local OneDrive directory in two places:
1. Bill's iMac OneDrive directory; and
2. a directory on a Windows10 VM

The directory houses a Github repository and the main testing is to see how well Obsidian-git works with vaults held in OneDrive folders.

Initial testing is on Bill's iMac with this very notes file.
 - stage, commit, and push this thing
 -  this seems to work OK; but why am I seeing `.obsidian/workspace.json`  in the Obsidian-git "Changes" list? it should be `.gitignore`-ed
- OK. added a file directly on Github. `push`-ing from here should raise an error.
	- and it did raise the expected error.


## 2022-11-27
 - fiddled with the .gitignore file to ignore changes to `.obsidian/workspace.json` file and ended up using this command:
 - `git update-index --skip-worktree .obsidian/workspace.json`
 - still do not understand why this was needed


