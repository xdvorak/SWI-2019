# SWI 2019 (/2020)

## SWI 1

These are materials for the [Software Engineering 1](http://is.mendelu.cz/katalog/syllabus.pl?kod=PEF:SWI1) course,
Tuesday group, 11am local time, even-numbered weeks, taught on Mendel University in Brno, fall 2019, led by [@ZitaNemeckova](https://github.com/ZitaNemeckova) and [@himdel](https://github.com/himdel).

The topic will be Git, the whole semester.

If you need to contact us, please use the [ManageIQ/welcome](https://gitter.im/ManageIQ/welcome) channel on [Gitter](https://gitter.im). (You'll need a github login anyway.)  
Feel free to use that channel to share anything useful you've found :).


### Synopsis:

| date | topic |
|-|-|
| 2019-10-01 | Intro @ Red Hat |
| 2019-10-15 | (dekanske volno) |
| 2019-10-29 | Basics recap, Github, get it working |
| 2019-11-12 | Synchronization, Conflicts |
| 2019-11-26 | Rebase, graded exercise |
| 2019-12-10 | Advanced git |


#### 2019-10-15 (homework :))

Check out https://learngitbranching.js.org/ , go through the whole Introduction Sequence in the Main section, and look at the first Push & Pull exercise in the Remote section.
You can also try for yourself at http://git-school.github.io/visualizing-git/#free .


#### 2019-10-29 - Basics recap, Github, get it working

1. Recap of the git branching exercises

1. Make sure you have a github account, quick intro to github if needed

1. Get git working on your machines, make sure you can push to github

1. History, the why, what?  
  - `git log` - show what's what

5. Basics - `init`/`clone`, `git config`  
  - commits
  - branches
  - exercises, see below


#### 2019-11-12 - Synchronization, Conflicts

1. remotes

1. updating (pull vs fetch & merge...)

1. Conflicts  
  - branches (continued)
  - merge


#### 2019-11-26 - Rebase, graded exercise

1. rebase flow

1. `git rebase -i` - more real examples, get to try everything


#### 2019-12-10 - Advanced git

1. aliases, scripting, more configuration, .git directory structure


### Exercises

- Basics (2019-10-29)
  - Install some text editor if you don't like vim/nano
  - Set git username and email
  - Add a ssh key to your GitHub account
  - Fork [the SWI-2019 repository](https://github.com/RoadToSoftwareFactory/SWI-2019)
  - Clone the repository
  - Set up remotes
  - Create new branch
  - Create a file `<github login>/commit.md` inside the repository
  - Add some text to the file and create 1st commit
  - Add the hash of the 1st commit to the file and create 2nd commit
  - Add another line of text to the file, then add diff to the file and create 3rd commit
  - Create a pull request to the upstream repository

(TODO: rest of this section may change yet)

- Synchronization (3rd class)
  - Update your repository from upstream and push it
  - Add additional remote from one of your classmates
  - Create local branch from your classmates repostiory

- Conflicts and rebasing (4th class 1st group)
  - Part 1 (resolving conflicts)
    - Synchronize your PR branch from 2nd class with current master
    - Resolve any conflicts you have but, keep both changes in your file
    - **For those who had put their files in some other location than `uisLogin/commit.md`**
      - move your PR file to folder that is named after your UIS login
      - rename your file to `commit.md` if it has different name
      - we need this to assign points (sorry about that)
    - push updated PR
  - Part 2 (rebasing)
    - checkout to your branch with PR from 2nd class
    - create new file at `uisLogin/rebasing.md` (you will be working with this file for the rest of this exercise)
    - add some text to the file and create 1st commit (this is not the actual first commit of your branch, but we will call it that way)
    - after that, add another text and copy contents of git diff to the file
    - add the changes into the previous (1st) commit
    - add another text and create 2nd commit
    - check the commit hash of the 2nd commit
    - add the hash of the 2nd commit to file, but add it as a new line of text to the 1st commit
    - after that add another lines of text and create 3rd commit
    - add another lines and create 4th commit
    - check the commit hash of the 4th commit
    - change the commit message of the 3rd commit to this: `<your-first-name>: <4th-commit-hash>`
    - after that merge the 3rd and 4th commits into single one. Keep only the commit message of the 3rd commit.
    - push your changes to gitHub
  - This exercise will be rated
  - If you get stuck on something try to search for a solution on Google first (just for a couple of minutes). If you find a solution but you are not confident it will solve your issue, just let us know ;-). But if you don't find any solution, ask us anyway and we will help you.
  - If you finish sooner, you can help your classmates. You might get a bonus for that later!
- Conflicts and rebasing (**4th class 2nd group**)
  - Part 1 (Resolving conflicts)
    - Update your master
    - Checkout a new branch
    - Make changes to `rebase_task` file and create a PR
    - After everyone is done conflict will be merged
    - Update your master and branch
    - Resolve conflicts
    - Push changes
  - Part 2 (interactive rebase)
    - Make changes to `interactive_rebase_task` file but every change **MUST** be in separated commit
    - Push all changes
    - Delete commit with your favorite color
    - Rename commit with your favorite season to something in UPPERCASE
    - Edit commit with your favorite city so it's Helsinki 
    - Squash all food related commits into one (hint ice cream, vegetables, fruit)
    - When done mention one of instructors in a comment (if you are the first one and everything is done correctly you will get a GitHub code for free t-shirt via Gitter) 
  - This exercise will NOT be rated but the one next week will be (and it will be pretty much the same as this one)
  - If you get stuck on something try to search for a solution on Google first (just for a couple of minutes). If you find a solution but you are not confident it will solve your issue, just let us know ;-). But if you don't find any solution, ask us anyway and we will help you.
  - If you finish sooner, you can help your classmates. You might get a bonus for that later!
- Useful usages (**last class 1st group**)
    - Topics
        - (1) How to "transfer" change (not from commit)
        - (2) How to "transfer" change (from commit)
        - (3) How to remove file from commit
    - (1) How to
        - `git-apply` or `git apply` (https://git-scm.com/docs/git-apply)
        - git apply <name_of_file>
    - (2) How to
        - git cherry-pick <commit_hahs> (https://git-scm.com/docs/git-cherry-pick)
    - (3) How to remove file from commit
        - git reset --soft (git reset --hard)
        - https://stackoverflow.com/questions/12481639/remove-files-from-git-commit
    - Your task
        - (0) 
            - sync the repo from master (check with `git log` that you last commit with name `last class`)
            - you will need to create new PR - (it means you need a new branch)
            - you will need to add my fork of repo as remote
        - (A) 
            - you can download it by `curl https://raw.githubusercontent.com/RoadToSoftwareFactory/swi-2018/master/transform_values.patch > transform_values.patch`
            - apply patch from https://github.com/RoadToSoftwareFactory/swi-2018/blob/master/transform_values.patch
            - now you have some changes - create a commit
        - (B) 
            - find a switch for cherry pick command which will append original commit hash to new commit message created by cherry-pick
            - cherry pick (with using the switch ^ )the only commit from my(lpichler) PR in repo https://github.com/RoadToSoftwareFactory/swi-2018
        - (C) 
            - remove file accident.1 from cherry picked commit
        - (D) 
            - Create PR - check that you have 2 commits
        - (E) 
            - help class mates

- Graded exercise (**last class 2nd group**)
  - Interactive rebase
    - update your local repository
    - Fill out `interactive_rebase_task` file but every change on a line **MUST** be in separated commit (you should have six commits)
    - Push all changes and create a PR
    - Write your uni login in the description of your PR
    - Now use interactive rebase to make the following changes:
      - Drop commit with your favorite color
      - Reword commit with your favorite season to something in UPPERCASE
      - Edit commit with your favorite city so it's Helsinki 
      - Squash all food related commits into one (hint ice cream, vegetables, fruit)
    - Force push your changes
    - When you checked that everything is on Github correctly mention one of instructors in your PR
  - Feel free to Google :)

---

The course will be followed by [Software Engineering 2](https://is.mendelu.cz/katalog/syllabus.pl?kod=PEF:SWI2).  
Details to be determined.
