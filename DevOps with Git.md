# DevOps with Git #

## What is a Version Control System? ##
A version control system records changes to a file or a set of files over time so that users can recall specific versions later. Developers working in teams are writing new source code and change existing source code. The code for a project, app or software component is typcially organized in a folder structure. A developer in the team may be working on a new feature while another developer fixes a bug and changes code - each developer may make changes in different (or the same) parts of the file(s).
Version control systems solve these issues. They help track individual changes by a contributor and can prevent concurrent work.
Here are a few of the most popular types of version control systems:
* git
* SVN

Git is an open-source distributed version control system. Git version control is one of the most popular options.

## What is Git? ##
Git is a distributed version control tool that is used to store different versions of a file in a remote or local repository. It is used to track changes in the source and allows multiple developers to work together.
Git supports non-linear development because you can create multiple parallel branches. The purpose of Git is to manage a project as they change over time. Git stores this information in a data structure called a repository. 
A git repository contains the following:
- a set of commit objects
- a set of references to commit objects, called heads

## Why we use GitLab? ##
GitLab is a fully integrated software development platform thatnenables your team to be transparent, fast, effective, and cohesive from the discussion of a new idea to production, all on the same platform.

- Concurrent Development
  Projects are getting more and more complex. There is a growing need to manage multiple versions of code and files - and entire products.
  This means that multiple developers and designers can work on the same set of files - without worrying that they are duplicating effort or overwriting the work of other team members.

- Feature Branch Workflow
  One of the biggest advantages of git is its branching capabilities. Unlike centralized version control systems, Git branches are cheap and easy to merge. This facilitates the feature branch workflow popular with many Git users. Feature branches provide an isolated environment for every change to your codebase. When a developer wants to start working on something - no matter how big or small - they create a new branch. This ensures that the master branch always contains production-quality code.

- Pull Request
  A pull request is a way to asak another developer to merge one of your branches into their repository. This not only makes it easier for project leads to keep track of changes, but also lets developers initiate discussions around their work before integrating it with the rest of the codebase.

  ## How is Git different from SVN? ##
  Git is different from SVN, not better or worse. The key difference is that it is decentralized which just means that when you do a git clone (+ URL of your repository), what you are actually getting is a complete copy of the entire history of that project. This means all of your commits!
  Subversion is being used for many years and is a simple to use yet effective source control system. However, it gives notion of the folder structure on the PC and does not deal with branches effectively.
  Some of the features of git that makes it a more effective tool compared to SVN are mentioned below:
  + git has a staging area
    This just means that if you made 100 new changes to your code, you can break these 100 changes into 10 or 20 or more commits each with their own comments and their own detailed explanation of what just happened! Not only can you stage your commits out to logically display what changes you made, but you can alsodo patch staging that asks you what you want. You would use patch stagign if you and a co-worker are both working on the same file and you only want to commit a particular function that you've worked on. You do a Git patch using "git add -p".
  + git is very flexible
    It's trivial to **fork** a project, modify it, and still keep merging in the bugfixes from the HEAD branch. Git works for the Linux kernel developers. That means it is really fast (it has to be), and scales to thousands of contributors. Git also uses less space (up to 30 times less space for the Mozilla repository). Git is very flexible, very TIMTOWTDI (There Is More Than One Way To Do It). You can use whatever workflow you want, and git will support it.
  + git has a 'clean' command
    * git has a 'clean' command. SVN desparately needs this command, considering how frequently it will dump extra files on your disk.
    * git has the 'bisect' command. It's nice.
  + git only creates a single directory
    SVN creates .svn directories in every single folder (git only creates one .git directory). Every script you write, and every grep you do, will need to be written to ignore these .svn directories. You also need an entire command ("svn export") just to get a sane copy of your files.
  + git will just figure out status on its own
    * in SVN, each file & folder can come from a different revision or branch. At first, it sounds nice to have this freedom. But what this actually means is that there is a million different ways for your local checkout to be completely screwed up (for example, if "svn switch" fails halfway through, or if you enter a command wrong). And the worst part is: if you ever get into a situation where some of your files are coming from one place, and some of the from another, the "svn status" will tell you that everything is normal. You'll need to do "svn info" on each file/directory to discover how weird things are. If "git status" tells you that things are normal, then you can trust that things really are normal.
    * You have to tell SVN whenever you move or delete something. Git will just figure it out.
  + Ignore semantics are easier in git
    Semantics to ignore is easier in git. If you ignore a pattern (such as *.pyc), it will be ignored for all subdirectories. (But if you really want to ignore something for just one directory, you can). With SVN, it seems that there is no easy way to ignore a pattern across all subdirectories. 
    Another item involved ignoring files. Git makes it possible to have "private" ignore settings (using the file .git/info/exclude), which won't affect anyone else.

Subversion (SVN) may be one of the most well known centralized version control systems. In Subversion you are checking out a single version of the repository. With SVN, your data is stored on a central server.
With Subversion, you have a problem: the SVN repository may be in a location you cannot reach (in your company, and you don't have internet at the moment), you cannot commit. If you want to make a copy of your code, you have to literally copy/paste it.

Git is better than SVN because it works well even for developers who aren't always connected to the master repository, as it is available offline. Branching and merging support are also thought to be superior with Git. When it comes to disk space storage, it's pretty close to equal between both SVN and Git repositories.

## Git concepts ##
Git is a distributed version-control system for tracking changes in source code during software development. It is designed for coordinating work among programmers, but it can be used to track changes in any set of files. Its goals include speed, data integrity, and support for distributed, non-linear workflows.

### Basic terms related to Git ###

**1. Repository**
A Git repository is just a file location where users store all the files related to a project. When a user commits his code, a version/snapshot is created in the local repository. A Remote repository is hosted on a remote machine.

Users can typically obtain a Git repository in one of the following ways:
- by taking a local directory that is currently not under version control and turn it into a Git repository, or
- by cloning an existing Git repository

**2. Basic Git commands**

*git init*
initializes a brand new Git repository and begins tracking an existing directory. It adds a hidden subfolder within the existing directory that houses the internal data structure required for version control.

*git clone*
create a local copy of a project that already exists remotely. The clone includes all the project's files, history, and branches.

*git add*
stages a change. Git tracks changes to a developer's codebase, but it is necessary to stage and take a snapshot of the changes to include them in the project's history. This command performs staging, the first part of that two-step process. Any changes that are staged will become a part of the next snapshot and a part of the project's history. Staging and committing separately gives developers complete control over history of their project without changing how they code and work.

*git commit*
saves the snapshot to the project history and completes the change-tracking process. In short, a commit functions like taking a photo. Anything that's been staged with *git add* will become part of the snapshot with *git commit*.

*git status*
shows the status of changes as untracked, modified, or staged.

*git branch*
shows the branches being worked on locally.

*git merge*
merges lines of development together. This command is typically used to combine changes made on two distinct branches. For examples, a developer would merge when they want to combine changes from a feature branch into the master branch for deployment.

*git pull*
updates the local line of development with updates from its remote counterpart. Developers use this command if a teammate has made commits to a branch on a remote repository, and they would like to reflect those changes in their local environment.

*git push*
updates the remote repository with any commits made locally to a branch.

**3. Command Line commands**

- Start working on your project
  To work on a Git project locally (from your own computer), first you will need to clone (copy) it to your computer.

**4. Merge Requests**
Merge requests allow you to visualize and collaborate on the proposed changes to source code that exist as commits on a given Git branch.

## GitLab ##
GitLab provides a complete CI/CD tool chain in a single application. It provides one interface, one conversation, one permission model.

**What is the difference between git and GitLab**
* Git is a free and open-source version control system designed to handle everything from small to very large projects with speed and efficiency.
* GitLab is a open-source self-hosted Git management software
* GitLab offers git repository management, code reviews, issue tracking, activity feeds and wikis

**What are the features of GitLab?**
GitLab is a complete DevOps platform, delivered as a single application. It provides features which are fundamentally changing the way Development, Security, and Ops teams collaborate and build software. From idea to production, GitLab helps teams improve cycle times from weeks to minutes, reduce development costs and time to marked while increasing developer productivity.

## Git Repositories ##
Repositories are critical for code organization and access control.

**Conceptual or functionality group per repository**
This could be named per product, per program, or per library. Dividing code or artefacts at a later stage is difficult and might lead to rewriting of the public history or missing history. Structuring the repository or related repositories at an early stage is important. 
The repository name should be unique to your account. Choose a descriptive name based on the product or project. Check Copyright and trademarks to ensure proper naming. As far as naming conventions, separate words with - (hyphen, dash), since typing a hyphen is easier than typing _ (underscore).

**Read and Write access control is at the repository level**
A user has access to the entire repository - that means all branches, the complete history. For fine grained access, compartmentalize read/write access by structuring the code base into different repositories.

**Shared files required by multiple projects into a separate repository**
A shared repository promotes code reuse and is highly recommended.

**Avoid repositories for large binary files**
Git sync activities become challenging for large binary files. Cloning and branching operations become slow for large repositories. Use Artifactory for storing binary files.

## Git Branching ##
Branching is one of the most powerful features. Branches are the perfect tool to differentiate separate lines of development. Project teams should use feature branching extensively in the development workflow: for new features, for bug fixes.

A Git repository comprises of two key types of branches
1. The master branch at origin should be familiar to every Git user
2. origin/master should be the main branch where the source code of HEAD always reflects a production-ready state

The project/product team can have additional types of branches.

- Feature Branches
  * Feature branches are used to develop new features for the upcoming or a distant future release
  * they are merged and deleted after merge to the development branch or release branch
  
- Release Branches
  * Release branches support preparation of a new production release
  
- Hotfix Branches
  * hotfix branches are like release branches for a new production release
  * they arise from the necessity to act immediately upon an undesired state of a live production version
  * a hotfix branch may be branched off from the corresponding tag on the master branch that marks the production version

**Feature branch naming**
Use a consistent naming convention for your feature branches to identify the work done in the branch

## Git commits ##

**Commit related changes**
- small commits make it easier for reviewers and other developers to understand the changes and roll them back in case something goes wrong
- for example, fixing two different bugs should have two separate commits
- a commit should comprise of related changes only

**Author**
- Git commits should be performed by a recognized author with valud organization email id only
- Unrecognized authors makes it difficult to track the author for the specific code commits
- Ensure Git client is configured with the correct email address and linked to the GitLab user login name

**Comment**
1. Git commit comments should have a reference to User story, Task, Bug fix, Feature ID
2. use the specific reference to the tracker ID in the comments, such as Bug #634377
3. Commit messages should reflect the user's intention and not just the contents of the commit
4. Commit messages should explain the reason for the changes
5. An example for a good commit message is: "combine templates to reduce duplicate code in the user views"
6. The words "change", "improve", "fix", and "refactor" do not add much information to a commit message
7. For example, "Improve XML generation" could be better written as "Bug #634377: properly escape special characters in XML generation"
8. For more information about formatting commit messages, please see this excellent blog post by Tim Pope.
    https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html


## Git feature commits ##
Each feature should reside in its own branch, which can be pushed to the remote repository for backup/collaboration.

* Do not use branching off from master, feature branches should use development as their parent branch
* on completion of the feature, it should be merged into development
* Features should never interact directly with the master branch


