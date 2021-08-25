# CS 61B: Data Structures

    University of California, Berkeley
    Instructors: Paul Hilfinger
    hilfingr@cs.berkeley.edu
    Office Hours: TBD
    Lecture: Mon/Wed/Fri 1:00pm-2:00pm, Stanley 105 as capacity allows
    https://berkeley.zoom.us/j/94882182481?pwd=Q1BuVGdHb2p3T3JKc2xhMHRpZE9jQT09#success
    Author: Will Tholke

## Lab01 Notes: [[Source]](https://inst.eecs.berkeley.edu/~cs61b/fa21/materials/lab/lab1/#test-run)

### Remote SSH Access

In your terminal, replace *** with your 3 character login and enter the following command: `ssh cs61b-***@derby.cs.berkeley.edu`

### Git Workflow: Receiving Assignments:

Copy skeleton code, transfer branch to central repository, and sync the repo copy with central repository with the following commands:

```
cd ~/Desktop
cd repo
git fetch shared
git merge -m "Start Assignment ##"
git push
```


### Java Compilation & Development

In this class, we'll use the `javac` Java compiler from the command line, which is included in the Java Development Kit (JDK). Here's a list of [helpful flags](https://www.mankier.com/1/javac-java-11).

If you change a file after compiling, **you must recompile that same file to reflect your changes.**

1. Compile: `javac File.java`
2. Run: `java File`

### Comments

*Avoid using single-line comments* ` // which look like this`. The [CS 61B Style Guide](https://inst.eecs.berkeley.edu/~cs61b/fa21/docs/style-guide.html) requires that they not be used in projects.

The style guide, however, does require javadoc (documentation) comments:

```java
/** Returns the current size of the list. */
public int size() { ... }
```

Multi-line comments look like this:

```java
/* This is a
   multi-line comment */
```

### Git

Basic commands:
- `git init`
- `git add .`
- `git commit -m "message"`
- See the status of each repo file: `git status`
- See previous commits: `git log`

Undo changes in Git with this workflow:
- Unstage a file that's uncommitted: `git reset HEAD [file]`
- Amend latest commit:
  - `git add [forgotten-file]`
  - `git commit --amend`
  - `git checkout -- [file]` *use with caution!*

Branching:
- Create branch: `git branch [new-branch-name]`
- Switch branch: `git checkout [destination-branch]`
  - Create & checkout at once: `git checkout -b [new-branch-name]`
  - Merge: `git merge [branch-name]`
- Delete branch: `git branch -d [branch-to-delete]`
- Figure out what branch you're on: `git branch -v`

### Remote Repos

- Add remotes: `git remote add [short-name] [remote-url]`
- Rename: `git remote rename [old-name] [new-name]`
- Remove: `git remote rm [remote-name]`
- Clone: `git clone [remote-url] [optional-directory-name]`
- Push: `git push [remote-name] [remote-branch]`
  - `git push origin master`
- Fetch: `git fetch [remote-name]`
  - Best used when reviewing changes without incorporating them into your own code
- Pull: `git pull [remote-name] [remote-branch-name]`
  - Equivalent to `fetch + merge`
  - When you know it won't break your code, use `git pull origin master`