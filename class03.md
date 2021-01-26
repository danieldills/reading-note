# Intro to Git

## What is Git?
[source](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/) for the following information.

### Snapshots
Git is a DVCS that stores data in a file system made up of snapshots. Each time you save a changed version of your project — called commit — Git creates a snapshot of the file and stores a reference to it. If the file has not changed, Git only stores a reference to the already-stored identical version of it.

### Local Operations
Git mostly relies on local operations because most necessary information can be found in local resources. This allows for process expediency because a project’s history resides on the local disk, eliminating the need to fetch history information from the server, and allowing one to continue work on a project even when not online or on a VPN.

### Tracking Changes
Every single change applied to any file or directory is tracked by Git. And, as the gatekeeper, Git will always detect file corruption or loss of information in transit.

### Loss of Data
Git is set up to greatly minimize the possibility of irreversible damage to files, such as accidentally lost data. Git makes it extremely difficult for a snapshot of your file that is committed to be lost.

### States
Files in Git can reside in three main states: committed, modified and staged.

![Git workflow](https://blog.udemy.com/wp-content/uploads/2015/08/image066.png)

### Cloning
Cloning pulls the file for a given project, from Github, and stores a copy to your computer, locally by using the following command:
$ git clone https://github.com/test *using the Code link in GitHub*

### Workflow
[source](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/)
The local Git repository has three components:

Working Directory: The actual files reside here.
Index: The area used for staging
Head: Points to the most recent commit

![Git Workflow](https://blog.udemy.com/wp-content/uploads/2015/08/image036.png)

### *git status* command line gives you current status

## Git **A**dd **C**ommit **P**ush Process



