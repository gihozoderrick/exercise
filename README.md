# git exercises #
practical exercises
## bundle 1 ##
### exercise 1 ###
### exercises 2 ###
## bundle 3 ##
### exercises 1 ###
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
PS C:\Users\user\exercises git> git commit -m "exercises 2"
[dev 5de3901] exercises 2
 1 file changed, 410 insertions(+), 1 deletion(-)
PS C:\Users\user\exercises git> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 3.97 KiB | 3.97 MiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/gihozoderrick/exercise.git
   edefe95..5de3901  dev -> dev
PS C:\Users\user\exercises git> git status
On branch dev
Your branch is up to date with 'orgin/dev'.

nothing to commit, working tree clean
PS C:\Users\user\exercises git>
```
```bash PS C:\Users\user\exercises git> git pull
Already up to date.
PS C:\Users\user\exercises git> git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
PS C:\Users\user\exercises git> git add .
PS C:\Users\user\exercises git> git status
On branch ft/team-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    team.htm -> team.html

PS C:\Users\user\exercises git> git commit -m "team"
[ft/team-page 4d45d39] team
 1 file changed, 1 insertion(+)
 rename team.htm => team.html (86%)
PS C:\Users\user\exercises git> git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream orgin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\user\exercises git> git push --set-upstream orgin ft/team-page
fatal: unable to access 'https://github.com/gihozoderrick/exercise.git/': OpenSSL SSL_read: SSL_ERROR_SYSCALL, errno 0
PS C:\Users\user\exercises git> git status
On branch ft/team-page
nothing to commit, working tree clean
PS C:\Users\user\exercises git> git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream orgin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\user\exercises git> git push --set-upstream orgin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 424 bytes | 424.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/gihozoderrick/exercise/pull/new/ft/team-page
remote:
To https://github.com/gihozoderrick/exercise.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'orgin/ft/team-page'.
PS C:\Users\user\exercises git> git checkout main
Switched to branch 'main'
Your branch is ahead of 'orgin/main' by 3 commits.
  (use "git push" to publish your local commits)
PS C:\Users\user\exercises git> git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
PS C:\Users\user\exercises git> git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'orgin/ft/team-page'.
PS C:\Users\user\exercises git> git log
commit 4d45d39abec440c68de2b07aef768caf33fbf6cd (HEAD -> ft/team-page, orgin/ft/team-page)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Thu Jun 13 23:21:29 2024 -0700

commit 4d45d39abec440c68de2b07aef768caf33fbf6cd (HEAD -> ft/team-page, orgin/ft/team-page)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Thu Jun 13 23:21:29 2024 -0700

    team

commit 482503f7557c3e986350a590215c5a5acddfd181 (orgin/ft/service-redesign, ft/service-redesign)
Merge: fce4f5a 636f89f
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Wed Jun 12 09:38:16 2024 -0700

    merge main into service redesign

commit fce4f5a6ae49d1f20b93eabbdfef93e9eea75292
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Wed Jun 12 09:04:47 2024 -0700

    types of money roundering

commit 636f89ffcdd322670954c93e9e8f7e0c8e70a4e5 (main, ft/contact-page)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:54:46 2024 -0700

    merge1

commit 92a5c0de475996efa3ce6458ddc690bb6413aafa
Merge: f0ff1c5 72144ee
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:53:24 2024 -0700

    merge

commit f0ff1c51fb4d756c714fe0fdf1015b39f212d215
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:43:50 2024 -0700

    services explained

commit b7047349cbf5edcf1f69cd7b975968258da88a4a
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:25:24 2024 -0700

    services detailed

commit 72144ee0cc6dcb15f35df65dd59a69f8e9d02b6a (orgin/main)
Merge: 78dd1ac b704734
Author: gihozoderrick <167696725+gihozoderrick@users.noreply.github.com>
Date:   Mon Jun 10 13:39:10 2024 -0700

    Merge pull request #2 from gihozoderrick/ft/service-redesign

     services detailed

commit 78dd1ac97d3b7274adc883f072916045f9d6faeb
Merge: c9f629a d417b4e
Author: gihozoderrick <167696725+gihozoderrick@users.noreply.github.com>
Date:   Mon Jun 10 13:05:33 2024 -0700

    Merge pull request #1 from gihozoderrick/ft/bundle-2

    Add new html pages to the project

commit d417b4e2666fe35aca12f1e5b0f9ed040f6aef0b (orgin/ft/bundle-2, ft/bundle-2)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:40:22 2024 -0700

    services page

commit b50c41fb0c528c7fed938801043d73fc3ff8b42b
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:25:42 2024 -0700

    services

commit 5de390177f2a82af21d2168e2cafc513e8d43f49 (orgin/dev, dev)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:10:17 2024 -0700

    exercises 2

Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:25:42 2024 -0700

    services

commit 5de390177f2a82af21d2168e2cafc513e8d43f49 (orgin/dev, dev)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:10:17 2024 -0700

    exercises 2

    exercises 2

Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:25:42 2024 -0700

    services

commit 5de390177f2a82af21d2168e2cafc513e8d43f49 (orgin/dev, dev)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:10:17 2024 -0700

    exercises 2

commit 4d45d39abec440c68de2b07aef768caf33fbf6cd (HEAD -> ft/team-page, orgin/ft/team-page)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Thu Jun 13 23:21:29 2024 -0700

    team

commit 482503f7557c3e986350a590215c5a5acddfd181 (orgin/ft/service-redesign, ft/service-redesign)
Merge: fce4f5a 636f89f
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Wed Jun 12 09:38:16 2024 -0700

    merge main into service redesign

commit fce4f5a6ae49d1f20b93eabbdfef93e9eea75292
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Wed Jun 12 09:04:47 2024 -0700

    types of money roundering

commit 636f89ffcdd322670954c93e9e8f7e0c8e70a4e5 (main, ft/contact-page)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:54:46 2024 -0700

    merge1

commit 92a5c0de475996efa3ce6458ddc690bb6413aafa
Merge: f0ff1c5 72144ee
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:53:24 2024 -0700

    merge

commit f0ff1c51fb4d756c714fe0fdf1015b39f212d215
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:43:50 2024 -0700

    services explained

commit b7047349cbf5edcf1f69cd7b975968258da88a4a
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:25:24 2024 -0700

    services detailed

commit 72144ee0cc6dcb15f35df65dd59a69f8e9d02b6a (orgin/main)
Merge: 78dd1ac b704734
Author: gihozoderrick <167696725+gihozoderrick@users.noreply.github.com>
Date:   Mon Jun 10 13:39:10 2024 -0700

commit b7047349cbf5edcf1f69cd7b975968258da88a4a
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:25:24 2024 -0700

    services detailed

commit 72144ee0cc6dcb15f35df65dd59a69f8e9d02b6a (orgin/main)
Merge: 78dd1ac b704734
Author: gihozoderrick <167696725+gihozoderrick@users.noreply.github.com>
Date:   Mon Jun 10 13:39:10 2024 -0700

    Merge pull request #2 from gihozoderrick/ft/service-redesign

     services detailed

commit 78dd1ac97d3b7274adc883f072916045f9d6faeb
Merge: c9f629a d417b4e
Author: gihozoderrick <167696725+gihozoderrick@users.noreply.github.com>
Date:   Mon Jun 10 13:05:33 2024 -0700

    Merge pull request #1 from gihozoderrick/ft/bundle-2

    Add new html pages to the project

commit d417b4e2666fe35aca12f1e5b0f9ed040f6aef0b (orgin/ft/bundle-2, ft/bundle-2)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:40:22 2024 -0700

    services page

commit b50c41fb0c528c7fed938801043d73fc3ff8b42b
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:25:42 2024 -0700

    services

commit 5de390177f2a82af21d2168e2cafc513e8d43f49 (orgin/dev, dev)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:10:17 2024 -0700

    exercises 2

    exercises 2

Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:25:42 2024 -0700

    services

commit 5de390177f2a82af21d2168e2cafc513e8d43f49 (orgin/dev, dev)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:10:17 2024 -0700

    exercises 2

commit 4d45d39abec440c68de2b07aef768caf33fbf6cd (HEAD -> ft/team-page, orgin/ft/team-page)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Thu Jun 13 23:21:29 2024 -0700

    team

commit 482503f7557c3e986350a590215c5a5acddfd181 (orgin/ft/service-redesign, ft/service-redesign)
Merge: fce4f5a 636f89f
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Wed Jun 12 09:38:16 2024 -0700

PS C:\Users\user\exercises git> git checkout ft/contact-page
Switched to branch 'ft/contact-page'
PS C:\Users\user\exercises git> git cherry-pick 4d45d39abec440c68de2b07aef768caf33fbf6cd
[ft/contact-page 892f7be] team
 Date: Thu Jun 13 23:21:29 2024 -0700
 1 file changed, 1 insertion(+)
 rename team.htm => team.html (86%)
PS C:\Users\user\exercises git>  git add contact.html
PS C:\Users\user\exercises git> git commit -m "Adding contact"
[ft/contact-page e4cad28] Adding contact
 1 file changed, 14 insertions(+)
 create mode 100644 contact.html
PS C:\Users\user\exercises git> git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream orgin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\user\exercises git> git push --set-upstream orgin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 748 bytes | 748.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/gihozoderrick/exercise/pull/new/ft/contact-page
remote:
To https://github.com/gihozoderrick/exercise.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'orgin/ft/contact-page'.
PS C:\Users\user\exercises git> git checkout -b ft/faq-page                                                       
Switched to a new branch 'ft/faq-page'
PS C:\Users\user\exercises git> git add faq.html
PS C:\Users\user\exercises git> git commit -m "Faq"
[ft/faq-page 692389c] Faq
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html
PS C:\Users\user\exercises git> git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream orgin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\user\exercises git> git push --set-upstream orgin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 423 bytes | 423.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/gihozoderrick/exercise/pull/new/ft/faq-page
remote:
To https://github.com/gihozoderrick/exercise.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'orgin/ft/faq-page'.
PS C:\Users\user\exercises git> git log
commit 692389c96a49ca6c909b80a494acaa5e99c162f5 (HEAD -> ft/faq-page, orgin/ft/faq-page)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Fri Jun 14 00:14:41 2024 -0700

    Faq

commit e4cad280857ba6adcb84e18efb742493b7a926e5 (orgin/ft/contact-page, ft/contact-page)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Fri Jun 14 00:07:18 2024 -0700

    Adding contact

commit 892f7be2ee7efdf19781fd1f1bc718647b12641f
PS C:\Users\user\exercises git> git revert 892f7be2ee7efdf19781fd1f1bc718647b12641f
hint: Waiting for your editor to close the file... error: cannot spawn code--wait: No such file or directory
error: unable to start editor 'code--wait'
Please supply the message using either -m or -F option.
PS C:\Users\user\exercises git> git log
commit 692389c96a49ca6c909b80a494acaa5e99c162f5 (HEAD -> ft/faq-page, orgin/ft/faq-page)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Fri Jun 14 00:14:41 2024 -0700

    Faq

commit e4cad280857ba6adcb84e18efb742493b7a926e5 (orgin/ft/contact-page, ft/contact-page)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Fri Jun 14 00:07:18 2024 -0700

    Adding contact

commit 892f7be2ee7efdf19781fd1f1bc718647b12641f
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Thu Jun 13 23:21:29 2024 -0700

    team

commit 636f89ffcdd322670954c93e9e8f7e0c8e70a4e5 (main)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:54:46 2024 -0700

    merge1

commit 92a5c0de475996efa3ce6458ddc690bb6413aafa
Merge: f0ff1c5 72144ee
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:53:24 2024 -0700

    merge

commit f0ff1c51fb4d756c714fe0fdf1015b39f212d215
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:43:50 2024 -0700

    services explained

commit 72144ee0cc6dcb15f35df65dd59a69f8e9d02b6a (orgin/main)
Merge: 78dd1ac b704734
Author: gihozoderrick <167696725+gihozoderrick@users.noreply.github.com>
Date:   Mon Jun 10 13:39:10 2024 -0700

    Merge pull request #2 from gihozoderrick/ft/service-redesign

     services detailed

commit b7047349cbf5edcf1f69cd7b975968258da88a4a
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:25:24 2024 -0700

    services detailed

commit 78dd1ac97d3b7274adc883f072916045f9d6faeb
Merge: c9f629a d417b4e
Author: gihozoderrick <167696725+gihozoderrick@users.noreply.github.com>
Date:   Mon Jun 10 13:05:33 2024 -0700

    Merge pull request #1 from gihozoderrick/ft/bundle-2

    Add new html pages to the project

commit d417b4e2666fe35aca12f1e5b0f9ed040f6aef0b (orgin/ft/bundle-2, ft/bundle-2)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:40:22 2024 -0700

    services page

commit b50c41fb0c528c7fed938801043d73fc3ff8b42b
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:25:42 2024 -0700

    services

commit 5de390177f2a82af21d2168e2cafc513e8d43f49 (orgin/dev, dev)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:10:17 2024 -0700

    exercises 2

commit edefe95fa7180599f3e757c1b95812c3e48baf50
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 21:16:36 2024 -0700

    commit

commit c9f629afc28a34987c1449f0d1d7f8ae339fead8
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Thu Jun 6 08:59:45 2024 -0700

    all
PS C:\Users\user\exercises git> git revert 892f7be2ee7efdf19781fd1f1bc718647b12641f
error: your local changes would be overwritten by revert.
hint: commit your changes or stash them to proceed.
fatal: revert failed
PS C:\Users\user\exercises git> git status
On branch ft/faq-page
Your branch is up to date with 'orgin/ft/faq-page'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    team.html -> team.htm

PS C:\Users\user\exercises git> git commit -m "team"
[ft/faq-page 01468ed] team
 1 file changed, 1 deletion(-)
 rename team.html => team.htm (86%)
PS C:\Users\user\exercises git> git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 405 bytes | 405.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/gihozoderrick/exercise.git
   692389c..01468ed  ft/faq-page -> ft/faq-page
PS C:\Users\user\exercises git> git log
commit 01468edc766f167a2a24d982ef3711be7c0fcfe8 (HEAD -> ft/faq-page, orgin/ft/faq-page)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Fri Jun 14 00:29:17 2024 -0700

    team

commit 692389c96a49ca6c909b80a494acaa5e99c162f5
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Fri Jun 14 00:14:41 2024 -0700

    Faq

commit e4cad280857ba6adcb84e18efb742493b7a926e5 (orgin/ft/contact-page, ft/contact-page)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Fri Jun 14 00:07:18 2024 -0700

    Adding contact

commit 892f7be2ee7efdf19781fd1f1bc718647b12641f
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Thu Jun 13 23:21:29 2024 -0700

    team

commit 636f89ffcdd322670954c93e9e8f7e0c8e70a4e5 (main)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:54:46 2024 -0700

    merge1

commit 92a5c0de475996efa3ce6458ddc690bb6413aafa
Merge: f0ff1c5 72144ee
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:53:24 2024 -0700

    merge

commit f0ff1c51fb4d756c714fe0fdf1015b39f212d215
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:43:50 2024 -0700

    services explained

commit 72144ee0cc6dcb15f35df65dd59a69f8e9d02b6a (orgin/main)
Merge: 78dd1ac b704734
Author: gihozoderrick <167696725+gihozoderrick@users.noreply.github.com>
Date:   Mon Jun 10 13:39:10 2024 -0700

    Merge pull request #2 from gihozoderrick/ft/service-redesign

     services detailed

commit b7047349cbf5edcf1f69cd7b975968258da88a4a
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Mon Jun 10 22:25:24 2024 -0700

    services detailed

commit 78dd1ac97d3b7274adc883f072916045f9d6faeb
Merge: c9f629a d417b4e
Author: gihozoderrick <167696725+gihozoderrick@users.noreply.github.com>
Date:   Mon Jun 10 13:05:33 2024 -0700

    Merge pull request #1 from gihozoderrick/ft/bundle-2

    Add new html pages to the project

commit d417b4e2666fe35aca12f1e5b0f9ed040f6aef0b (orgin/ft/bundle-2, ft/bundle-2)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:40:22 2024 -0700

    services page

commit b50c41fb0c528c7fed938801043d73fc3ff8b42b
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:25:42 2024 -0700

    services

commit 5de390177f2a82af21d2168e2cafc513e8d43f49 (orgin/dev, dev)
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 22:10:17 2024 -0700

    exercises 2

commit edefe95fa7180599f3e757c1b95812c3e48baf50
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Sun Jun 9 21:16:36 2024 -0700

    commit

commit c9f629afc28a34987c1449f0d1d7f8ae339fead8
Author: Gihozo Derrick <gihozoderic@gmail.com>
Date:   Thu Jun 6 08:59:45 2024 -0700

    all
PS C:\Users\user\exercises git> git revert 892f7be2ee7efdf19781fd1f1bc718647b12641f
On branch ft/faq-page
Your branch is up to date with 'orgin/ft/faq-page'.

nothing to commit, working tree clean
PS C:\Users\user\exercises git> git push
Everything up-to-date
PS C:\Users\user\exercises git> git status
On branch ft/faq-page
Your branch is up to date with 'orgin/ft/faq-page'.

nothing to commit, working tree clean
PS C:\Users\user\exercises git> git push
Everything up-to-date
PS C:\Users\user\exercises git> 
