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
date: October 2016
autosize: true

Workshop Goals
========================================================
Become familiar with the Assessment Document Template and Git

- Getting started with Git and examples
- R markdown basics and examples
- Assessment Document Template 

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

- Even for private solo projects, it's a good idea to push your work to a remote location for peace of mind. Why? f you've recently pushed your work to GitHub, it's easy to grab a fresh copy, patch things up with the changes that only exist locally, and get on with your life.




Is it going to hurt?
========================================================
You have to install Git, get local Git talking to GitHub, and make sure RStudio can talk to local Git (and, therefore, GitHub). This is one-time or once-per-computer pain.

For new or existing projects, you will:

  * Dedicate a directory (a.k.a "folder") to it.
  * Make it an RStudio Project.
  * Make it a Git repository.
  * Go about your usual business. But instead of only *saving* individual files, periodically you make a **commit**, which takes a multi-file snapshot of the entire project.
  * Push commits to GitHub periodically.
  
It feels weird at first but quickly becomes second nature. 

More bad news.  Do you use GitHub to work with other people or to coordinate your own work from multiple computers? If so, after you recover from the initial setup, Git will crush you again with **merge conflicts**. And this is not one-time pain, this could be a dull ache for a long time. The best remedy is prevention, but also understanding how to back out of tricky situations and tackle them on your own terms.


Who can do what?
========================================================
A public repository is readable by the world. The owner can grant higher levels of permission to others, such as the ability to push commits.

A private repository is invisible to the world. The owner can grant read, write (push), or admin access to others.

There is also a formal notion of an organization, which can be useful for managing repository permissions for entire teams of people.



Installation pain
========================================================
Getting all the necessary software installed, configured, and playing nicely together is honestly half the battle here. Brace yourself for some pain. The upside is that you can give yourself a pat on the back once you get through this. And you WILL get through this.

You will find far more resources for how to *use Git* than for installation and configuration. Why? The experts ...

  * Have been doing this for years. It's simply not hard for them anymore.
  * Probably use some flavor of Unix. They may secretly (or not so secretly) take pride in neither using nor knowing Windows.
  * Get more satisfaction and reward for thinking and writing about Git concepts and workflows than Git installation.

In their defense, it's hard to write installation instructions. Failures can be specific to an individual OS or even individual computer.



Register a GitHub account
========================================================
Register an account with GitHub. It's free!

  * <https://github.com>
  
  
Install software if needed
========================================================
   * RStudio
   * Update R packages
   * Git (see Section 7 http://happygitwithr.com/install-git.html)
   * Jenny Bryan reccommends installing a Git client (we aren't going to today, but the instructions are available)
   * We also aren't going to set up keys for SSH, but directions are available
   
**Get current, people.** You don't want to adopt new things on day one. But at some point, running old versions of software adds unnecessary difficulty.



Connect RStudio to Git and GitHub
========================================================
Here we verify that RStudio can issue Git commands on your behalf. Assuming that you've gotten local Git to talk to GitHub, this means you'll also be able to pull from and push to GitHub from RStudio.

If you succeed here, your set up is DONE.

Make a new repo on GitHub
========================================================
Go to <https://github.com> and make sure you are logged in.

Click green "New repository" button. Or, if you are on your own profile page, click on "Repositories", then click the green "New" button.

Repository name: `myrepo` (or whatever you wish, we will delete this)  
**Public  
**YES Initialize this repository with a README

Click big green button "Create repository."

Copy the HTTPS clone URL to your clipboard via the green "Clone or Download" button. Or copy the SSH URL if you chose to set up SSH keys.

Clone the new GitHub repository to your computer via RStudio
========================================================
In RStudio, start a new Project:

  * *File > New Project > Version Control > Git*. In the "repository URL" paste the URL of your new GitHub repository. It will be something like this `https://github.com/melmonk/myrepo.git`.
  * Take charge of -- or at least notice! -- the local directory for the Project. A common rookie mistake is to have no idea where you are saving files or what your working directory is. Pay attention. Be intentional. Personally, I would do this in `~/tmp`.
  * I suggest you check "Open in new session", as that's what you'll usually do in real life.
  * Click "Create Project".

This should download the `README.md` file that we created on GitHub in the previous step. Look in RStudio's file browser pane for the `README.md` file.

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

Were you challenged for GitHub username and password?
========================================================
If you somehow haven't done so yet, now is the perfect time to make sure you don't need to keep providing username and password on each push.

Pick one:

  * Credential caching for HTTPS access, chapter \@ref(credential-caching).
  * Set up SSH keys, chapter \@ref(ssh-keys).

Now is the perfect time to do this, since you have a functioning test repo.

Clean up
========================================================
**Local** When you're ready to clean up, you delete the local repo any way you like. It's just a regular directory on your computer.

**GitHub** In the browser, go to your repo's landing page on GitHub. Click on "Settings".

Scroll down, click on "delete repository," and do as it asks.

