<style>

.footer {
    color: black; background: #E8E8E8;
    position: fixed; top: 90%;
    text-align:center; width:100%;
}

</style>
<div class="footer" style="margin-top;font-size:80%;">
Slide content modified from Jenny Bryan's <i>Happy Git with R</i></div>

Getting to know Git with R
========================================================
author: Melissa Monk
date: October 25-26, 2016
autosize: true

Workshop Goals
========================================================
Become familiar with the Assessment Document Template and Git

- Getting started with Git and examples
- R markdown basics and examples
- Assessment Document Template 


Workshop Plan
========================================================
  
    
**Tuesday morning**: Basics of Git and GitHub and R markdown   

**Tuesday lunch**: Fix remaining installation issues  

**Tuesday afternoon**: Finish R markdown basics and start template  

**Wednesday morning**: Continue working with the template  

**Wednesday afternoon**: I'll be around until 3   



Download a copy of the slides (if you haven't already)
========================================================
We're going to Fork the [Rmarkdown_workshop_2016 repository](https://github.com/melmonk/Rmarkdown_workshop_2016) from my repository and then clone it.

See the Agenda for detailed instructions.



Why Git?
========================================================
- [Git](http://git-scm.com) is a __version control system__. Its original purpose was to help groups of developers work collaboratively on big software projects. Git manages the evolution of a set of files -- called a __repository__ -- in a sane, highly structured way. If you have no idea what I'm talking about, think of it as the "Track Changes" features from Microsoft Word on steroids.

- Git has been re-purposed by the data science community. In addition to using it for source code, we use it to manage the motley collection of files that make up typical data analytical projects, which often consist of data, figures, reports, and, yes, source code.




Why GitHub?
========================================================
- This is where hosting services like [GitHub](https://github.com), [Bitbucket](https://bitbucket.org), and [GitLab](https://about.gitlab.com) come in. 

- They provide a home for your Git-based projects on the internet. 
- The remote host acts as a distribution channel or clearinghouse for your Git-managed project. 
- It allows other people to see your stuff, sync up with you, and perhaps even make changes. 
- Even for private solo projects, it's a good idea to push your work to a remote location for peace of mind. 

IF you haven't done so, register an account with [GitHub](www.github.com) now.


Is it going to hurt?
========================================================
You have to install Git, get local Git talking to GitHub, and make sure RStudio can talk to local Git (and, therefore, GitHub). This is one-time or once-per-computer pain.


**More bad news.**      
Do you use GitHub to work with other people or to coordinate your own work from multiple computers? 

If so, after you recover from the initial setup, Git will crush you again with **merge conflicts**. And this is not one-time pain, this could be a dull ache for a long time. The best remedy is prevention, but also understanding how to back out of tricky situations and tackle them on your own terms.

Who can do what?
========================================================
A **public repository** is readable by the world. The owner can grant higher levels of permission to others, such as the ability to push commits.

A **private repository** is invisible to the world. The owner can grant read, write (push), or admin access to others.

There is also a formal notion of an **organization**, which can be useful for managing repository permissions for entire teams of people.


  
Install software if needed
========================================================
   * RStudio
   * Update R packages
   * Git (see Section 7 http://happygitwithr.com/install-git.html)
   * PC: MikTek or TeX Live(needed to compile to PDF) 
   * Mac: MacTeX
   * Jenny Bryan reccommends installing a Git client (we aren't going to today, but the instructions are available)
   * Directions for setting up keys for SSH are available in the template ReadMe
   

Cloning vs. Forking
========================================================
Clone someone else's repository on GitHub where you just want a copy. But you also want to track its evolution.  You can keep the clone up-to-date by pulling new commits into your local copy.


What if you suspect you might want to propose a change to a repository? Then you should fork it, instead of clone it.

We're going to Fork the [Rmarkdown_workshop_2016 repository](https://github.com/melmonk/Rmarkdown_workshop_2016) and then clone it.

Make local changes, save, commit
========================================================
From RStudio, modify the `README.md` file, e.g., by adding the line "This is a line from RStudio". Save your changes.

Commit these changes to your local repo. How?

From RStudio:

  * Click the "Git" tab in upper right pane.
  * Check "Staged" box for `README.md`.
  * If you're not already in the Git pop-up, click "Commit".
  * Type a message in "Commit message", such as "Commit from RStudio".
  * Click "Commit".
  
  

Push your local changes online to GitHub
========================================================  
Click the green "Push" button to send your local changes to GitHub. If you are challenged for username and password, provide them (but see below). You should see some message along these lines.

``` sh
[master dc671f0] blah
 3 files changed, 22 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 myrepo.Rproj
```

Confirm the local change propagated to the GitHub remote
========================================================
Go back to the browser. I assume we're still viewing your new GitHub repo.

Refresh.

You should see the new "This is a line from RStudio" in the README.

If you click on "commits," you should see one with the message "Commit from RStudio".

If you have made it this far, you are DONE with set up. But first ...


Errors, errors and more errors
========================================================
This is a highly inelegant, but effective technique for disaster recovery.

Basic idea:

*Commit early and often.   

*Push to a remote, like GitHub, often. 

*The state of things on GitHub is your new "worst case scenario". 

*If you really screw things up locally, copy all the files (or the ones that have changed) to a safe place.   

*Usually your files are JUST FINE. But it is easy to goof up the Git infrastructure when you're new at this. And it can be hard to get that straightened out on your own.   

*Rename the existing local repo as a temporary measure, i.e. before you do something radical, like delete it.

*Clone the repo from GitHub to your local machine. You are back to a happy state.   

Errors, errors and more errors
========================================================

*Copy all relevant files back over from your safe space. The ones whose updated state you need to commit.

*Stage and commit. Push.   

*Carry on with your life.   


Practice this before you need it, so you see how it works.


.gitignore file
========================================================
This contains all of the files that you don't want to push to GitHub

By default this contains .Rproj.user, .Rhistory, .RData, .Ruserdata

Reasons for not pushing a file:
* Large file pushed by accident
* Extraneous files you don't care about, e.g., .docx files
* Confidential data or script containing passwords

IF you push confidential data to GitHub, you cannot remove it without removing the commit history!  



If you need a laugh
========================================================
Your commits will look more glorious scrolling by Star Wars style:

- http://starlogs.net
- http://starlogs.net/#melmonk/Rmarkdown_workshop_2016


How to make a new repo on GitHub
========================================================
Go to <https://github.com> and make sure you are logged in.

Click green "New repository" button. Or, if you are on your own profile page, click on "Repositories", then click the green "New" button.

Repository name: `myrepo` (or whatever you wish, we will delete this)  
**Public  
**YES Initialize this repository with a README

Click big green button "Create repository."

Copy the HTTPS clone URL to your clipboard via the green "Clone or Download" button. Or copy the SSH URL if you chose to set up SSH keys.


