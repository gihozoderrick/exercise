# git exercises #
practical exercises
## bundle 1 ##
### exercise 1 ###
### exercises 2 ###
``` bash PS C:\Users\user\exercises git> git init
Initialized empty Git repository in C:/Users/user/exercises git/.git/
PS C:\Users\user\exercises git> git branch -M  master main
PS C:\Users\user\exercises git> git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\user\exercises git> git add README.md
PS C:\Users\user\exercises git> git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md

PS C:\Users\user\exercises git> git commit -m
error: switch `m' requires a value
PS C:\Users\user\exercises git> git commit -m "all"
[main (root-commit) c9f629a] all
 1 file changed, 3 insertions(+)
 create mode 100644 README.md
PS C:\Users\user\exercises git> git add remote orgin https://github.com/gihozoderrick/exercise.git
fatal: pathspec 'remote' did not match any files
PS C:\Users\user\exercises git> git remote add orgin https://github.com/gihozoderrick/exercise.git
PS C:\Users\user\exercises git> git status
On branch main
nothing to commit, working tree clean
PS C:\Users\user\exercises git> git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream orgin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\user\exercises git> git push --set-upstream orgin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 250 bytes | 50.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/gihozoderrick/exercise.git
 * [new branch]      main -> main
branch 'main' set up to track 'orgin/main'.
PS C:\Users\user\exercises git> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\user\exercises git> git checkout -b test
Switched to a new branch 'test'
PS C:\Users\user\exercises git> git checkout dev
Switched to branch 'dev'
PS C:\Users\user\exercises git> git checkout -d test
HEAD is now at c9f629a all
PS C:\Users\user\exercises git> git checkout -D test
error: unknown switch `D'
usage: git checkout [<options>] <branch>
   or: git checkout [<options>] [<branch>] -- <file>...

    -b <branch>           create and checkout a new branch
    -B <branch>           create/reset and checkout a branch
    -l                    create reflog for new branch
    --[no-]guess          second guess 'git checkout <no-such-branch>' (default)
    --[no-]overlay        use overlay mode (default)
    -q, --[no-]quiet      suppress progress reporting
    --[no-]recurse-submodules[=<checkout>]
                          control recursive updating of submodules
    --[no-]progress       force progress reporting
    -m, --[no-]merge      perform a 3-way merge with the new branch
    --[no-]conflict <style>
                          conflict style (merge, diff3, or zdiff3)
    -d, --[no-]detach     detach HEAD at named commit
    -t, --[no-]track[=(direct|inherit)]
                          set branch tracking configuration
    -f, --[no-]force      force checkout (throw away local modifications)
    --[no-]orphan <new-branch>
                          new unborn branch
    --[no-]overwrite-ignore
                          update ignored files (default)
    --[no-]ignore-other-worktrees
                          do not check if another worktree is holding the given ref
    -2, --ours            checkout our version for unmerged files
    -3, --theirs          checkout their version for unmerged files
    -p, --[no-]patch      select hunks interactively
    --[no-]ignore-skip-worktree-bits
                          do not limit pathspecs to sparse entries only
    --[no-]pathspec-from-file <file>
                          read pathspec from file
    --[no-]pathspec-file-nul
                          with --pathspec-from-file, pathspec elements are separated with NUL character

PS C:\Users\user\exercises git>
PS C:\Users\user\exercises git> git branch -D test
Deleted branch test (was c9f629a).
PS C:\Users\user\exercises git> git add home.html
PS C:\Users\user\exercises git> git status
HEAD detached at c9f629a
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

PS C:\Users\user\exercises git> git stash
Saved working directory and index state WIP on (no branch): c9f629a all
PS C:\Users\user\exercises git> git add about.html
PS C:\Users\user\exercises git> git status
HEAD detached at c9f629a
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

PS C:\Users\user\exercises git> git stash
Saved working directory and index state WIP on (no branch): c9f629a all
PS C:\Users\user\exercises git> git add team.htm
PS C:\Users\user\exercises git> git stash
Saved working directory and index state WIP on (no branch): c9f629a all
PS C:\Users\user\exercises git> git add home.html
PS C:\Users\user\exercises git> git stash
Saved working directory and index state WIP on (no branch): c9f629a all
PS C:\Users\user\exercises git> git stash list
stash@{0}: WIP on (no branch): c9f629a all
stash@{1}: WIP on (no branch): c9f629a all
stash@{2}: WIP on (no branch): c9f629a all
stash@{3}: WIP on (no branch): c9f629a all
PS C:\Users\user\exercises git> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --[no-]quiet      be quiet, only report errors
    --[no-]index          attempt to recreate the index

PS C:\Users\user\exercises git> git stash pop stash@{2}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --[no-]quiet      be quiet, only report errors
    --[no-]index          attempt to recreate the index

PS C:\Users\user\exercises git> git stash list
stash@{0}: WIP on (no branch): c9f629a all
stash@{1}: WIP on (no branch): c9f629a all
stash@{2}: WIP on (no branch): c9f629a all
stash@{3}: WIP on (no branch): c9f629a all
PS C:\Users\user\exercises git> git stash pop stash@{2}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --[no-]quiet      be quiet, only report errors
    --[no-]index          attempt to recreate the index

PS C:\Users\user\exercises git> git stash pop
HEAD detached at c9f629a
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Dropped refs/stash@{0} (8993490f07eda4cd548da9c2d3ee9ace23673bac)
PS C:\Users\user\exercises git> git stash
Saved working directory and index state WIP on (no branch): c9f629a all
PS C:\Users\user\exercises git> git stash pop stash@{2}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --[no-]quiet      be quiet, only report errors
    --[no-]index          attempt to recreate the index

PS C:\Users\user\exercises git> git stash pop [2]
error: [2] is not a valid reference
PS C:\Users\user\exercises git> git stash pop stash@[2]
error: stash@[2] is not a valid reference
PS C:\Users\user\exercises git> git stash pop stash@{2}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --[no-]quiet      be quiet, only report errors
    --[no-]index          attempt to recreate the index

PS C:\Users\user\exercises git> git stash pop stash@"{2}"
HEAD detached at c9f629a
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{2} (91a9aaa8fcc9365cea1212b7645fe3fab628a4c7)
PS C:\Users\user\exercises git> git stash pop stash@"{3}"
fatal: log for 'stash' only has 3 entries
PS C:\Users\user\exercises git> git stash list
stash@{0}: WIP on (no branch): c9f629a all
stash@{1}: WIP on (no branch): c9f629a all
stash@{2}: WIP on (no branch): c9f629a all
PS C:\Users\user\exercises git> git stash pop stash@"{2}"
HEAD detached at c9f629a
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Dropped stash@{2} (2c9b30ed83ca93d109830b0808463d6309e7ae2d)
PS C:\Users\user\exercises git> git commit -m "exercise"
[detached HEAD 5c37d6f] exercise
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
PS C:\Users\user\exercises git> git push
fatal: You are not currently on a branch.
To push the history leading to the current (detached HEAD)
state now, use

    git push orgin HEAD:<name-of-remote-branch>

PS C:\Users\user\exercises git> git push <name-of-remote-branch>
At line:1 char:10
+ git push <name-of-remote-branch>
+          ~
The '<' operator is reserved for future use.
    + CategoryInfo          : ParserError: (:) [], ParentContainsErrorRecordException
    + FullyQualifiedErrorId : RedirectionNotSupported

PS C:\Users\user\exercises git> git push --<name-of-remote-branch>
error: unknown option `<name-of-remote-branch>'
usage: git push [<options>] [<repository> [<refspec>...]]

    -v, --[no-]verbose    be more verbose
    -q, --[no-]quiet      be more quiet
    --[no-]repo <repository>
                          repository
    --[no-]all            push all branches
    --[no-]branches       alias of --all
    --[no-]mirror         mirror all refs
    -d, --[no-]delete     delete refs
    --[no-]tags           push tags (can't be used with --all or --branches or --mirror)
    -n, --[no-]dry-run    dry run
    --[no-]porcelain      machine-readable output
    -f, --[no-]force      force updates
    --[no-]force-with-lease[=<refname>:<expect>]
                          require old value of ref to be at this value
    --[no-]force-if-includes
                          require remote updates to be integrated locally
    --[no-]recurse-submodules (check|on-demand|no)
                          control recursive pushing of submodules
    --[no-]thin           use thin pack
    --[no-]receive-pack <receive-pack>
                          receive pack program
    --[no-]exec <receive-pack>
                          receive pack program
    -u, --[no-]set-upstream
                          set upstream for git pull/status
    --[no-]progress       force progress reporting
    --[no-]prune          prune locally removed refs
    --no-verify           bypass pre-push hook
    --verify              opposite of --no-verify
    --[no-]follow-tags    push missing but relevant tags
    --[no-]signed[=(yes|no|if-asked)]
                          GPG sign the push
    --[no-]atomic         request atomic transaction on remote side
    -o, --[no-]push-option <server-specific>
                          option to transmit
    -4, --ipv4            use IPv4 addresses only
    -6, --ipv6            use IPv6 addresses only

PS C:\Users\user\exercises git> git push orgin HEAD:<name-of-remote-branch>
error: The destination you provided is not a full refname (i.e.,
starting with "refs/"). We tried to guess what you meant by:

- Looking for a ref that matches '<name-of-remote-branch>' on the remote side.
- Checking if the <src> being pushed ('HEAD')
  is a ref in "refs/{heads,tags}/". If so we add a corresponding
  refs/{heads,tags}/ prefix on the remote side.

Neither worked, so we gave up. You must fully qualify the ref.
hint: The <src> part of the refspec is a commit object.
hint: Did you mean to create a new branch by pushing to
hint: 'HEAD:refs/heads/<name-of-remote-branch>'?
error: failed to push some refs to 'https://github.com/gihozoderrick/exercise.git'
PS C:\Users\user\exercises git> git checkout -b dev
fatal: a branch named 'dev' already exists
PS C:\Users\user\exercises git> git checkout dev                  
M       README.md
Warning: you are leaving 1 commit behind, not connected to
any of your branches:

  5c37d6f exercise

If you want to keep it by creating a new branch, this may be a good time
to do so with:

 git branch <new-branch-name> 5c37d6f

Switched to branch 'dev'
PS C:\Users\user\exercises git> git commit -m "exercises"
On branch dev
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\user\exercises git> git add all 
fatal: pathspec 'all' did not match any files
PS C:\Users\user\exercises git> git add all .
fatal: pathspec 'all' did not match any files
PS C:\Users\user\exercises git> git stash pop [2]                 
error: [2] is not a valid reference
PS C:\Users\user\exercises git> git stash list
stash@{0}: WIP on (no branch): c9f629a all
stash@{1}: WIP on (no branch): c9f629a all
PS C:\Users\user\exercises git> git stash pop stash@{"1"}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --[no-]quiet      be quiet, only report errors
    --[no-]index          attempt to recreate the index

PS C:\Users\user\exercises git> git stash pop stash@"{1}"
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.htm

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Dropped stash@{1} (fd71406935abd7124299eb88d8cdaf8da00ead8a)
PS C:\Users\user\exercises git> git stash pop stash@"{0}"
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html
        new file:   team.htm

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Dropped stash@{0} (217bd357ba1f50b4c56cecd3ae1e160977b0b73c)
PS C:\Users\user\exercises git> git stash pop
No stash entries found.
PS C:\Users\user\exercises git> git add about.html
fatal: pathspec 'about.html' did not match any files
PS C:\Users\user\exercises git> git commit -m "commit"
[dev edefe95] commit
 2 files changed, 24 insertions(+)
 create mode 100644 home.html
 create mode 100644 team.htm
PS C:\Users\user\exercises git> git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream orgin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\user\exercises git> git push --set-upstream orgin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 502 bytes | 502.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/gihozoderrick/exercise/pull/new/dev
remote:
To https://github.com/gihozoderrick/exercise.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'orgin/dev'.
PS C:\Users\user\exercises git> git status
On branch dev
Your branch is up to date with 'orgin/dev'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\user\exercises git> git stash list
PS C:\Users\user\exercises git> git reset --hard
HEAD is now at edefe95 commit
PS C:\Users\user\exercises git>
```
