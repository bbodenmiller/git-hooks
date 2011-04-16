# VersionOne Git Hooks
So you can be lazy and make the computer do the boring stuff!

## Current Hooks

- [prepare-commit-message](http://www.kernel.org/pub/software/scm/git/docs/githooks.html#_prepare_commit_msg): 
  when you `git commit`, this hook will inspect the current branch name looking for a [VersionOne ID](#versionone-id). 
  If it finds one, I'll will append it to the commit message for you, magically! You'll have an opportunity to edit 
  or remove it if you like (assuming you did't do `git commit -m "..."`).
  
  Also, if you've already mentioned the asset in your commit message, the hook leaves things exactly as they are.


Have some hooks you'd like to see? Let us know. Or better yet, fork, add your hook, and send us a Pull Request!

## Installing
Currently you need to download both the [`prepare-commit-message`](https://github.com/versionone/git-hooks/blob/master/prepare-commit-msg)
hook and supporting [`git_wrapper.rb`](https://github.com/versionone/git-hooks/blob/master/git_wrapper.rb) file, and put them in the 
`.git/hooks/` directory in each repository you want to use the hooks with. We'll make this a whole lot easier, real soon!

## License
VersionOne Git Hooks are covered under the MIT License. See [LICENSE](https://github.com/versionone/git-hooks/blob/master/LICENSE) for more information.

### VersionOne ID
Current ID's look like

- Story : `S-01234`
- Task : `TK-01234`
- Defect : `D-01234`
- Acceptance Test : `AT-01234`
- Regression Test : `RT-01234`
- Environment : `ENV-01234`

