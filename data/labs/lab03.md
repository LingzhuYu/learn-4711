
#Lab #3 - Website Conversion
COMP4711 - BCIT - Fall 2016

##Lab Goals

Last week, you practiced collaborative workflow. 

This week, using that workflow, you will gain some exposure to CodeIgniter
and the architecture of a typical small webapp, by converting a static
website into a CodeIgniter one.

I have setup a [starter repository](https://github.com/jedi-academy/starter-gallery) 
for you to work from, and this lab will walk you through
making it into a dynamic CI-driven website, in three steps.

##Lab Teams

Similar to last week, this is a pair lab, sharing a single team repository, but with each team member using 
their own github account and computer. I would like you to use different teams
than last week, and for each of you to have a different role.

Teams of one are *not* acceptable. This is partly about collaboration, after all.
If a set has an odd number of students, see me during lab and I will override
the team membership, adding a third member.

If you miss the lab, you will end up being a defacto team of one, completing
the tasks yourself before the submission deadline.
This will let you earn some of the lab marks, but none of those for collaboration.

Team members will each have a role to play:
- One member will be the creator and maintainer of the team repo - he/she will be designated the CAPTAIN
- The second member of the team will be a contributor - designated the FIRST MATE
- If a team has a third member, they will also be a contributor - designated the SECOND MATE

Most of the lab tasks are meant to be done using pair programming, i.e. with 
one person "driving", and the other(s) "navigating". 
Team members should use their own computer when "driving", to ensure that
you do not work with the same local repository.


##Lab Submission

Your lab will result in a github repository for your team, as well as one for each team
member.

Submit a readme *text* file, or a submission comment, to the lab dropbox. 
It should contain a link to your **team**'s github repository. 

Due: in theory, this should be completed during the lab period,
but some teams will need a bit more time.  
I have set the deadline to this Sunday at 17:30.

##Lab Marking Guideline

A marking rubric has been attached to the lab 3 dropboxes, similar to our
first lab. The labs will be weighted equally in the marks worksheet,
even if some of them have different raw scores because of their rubric.

I will be looking at the features in your submitted webapp, to see if you
succeeded at enhancing it per spec, in spite of the process; and I will
be looking at the repository, its forks, and commit history, to
determine how well you followed the collaboration process.

#The Lab:

##Team Setup

-    Choose partners
-    Select one of you to be CAPTAIN (who wasn't one last week)
-    The CAPTAIN should join a D2L group for lab 3
-    The MATE(s) should join the same group
-    If the group membership gets messed up, see me to fix it

##Team Repository Setup (CAPTAIN)

-    Create a github organization for your team
-    Fork the lab starter repo into that organization, using a name of your choice
-	Add a changelog file to the project root, and insist that team members update it with their contributions
-    Create a new branch "develop"
-    Make "develop" the default branch

##Member Repository Setup (All)

-    Configure your git client to use signing for this project too, if not already setup globally
-    Fork the team repository to your personal github account (including the CAPTAIN)
-    Clone your repository locally, using a name/location of your choice
-    If using an IDE, "git ignore" the IDE's metadata folder, so you don't inflict it on your teammates.
-    If you want to keep this separate from last week's, add a new local domain, eg "gallery.local"
-    Map the virtual domain you will use to the "public" folder inside your local repo for this lab
-    Restart Apache
-    Make sure that your project serves correctly, eg. using "gallery.local" or the local domain that you setup.


##Static to Trivial Website Conversion (FIRST MATE)
    
**Caution**

	Some of the student Apache installations in lab on Thursday were not
	handling redirection properly - they were not injecting index.php, per
	your public/.htaccess.

	The symptom: you get a 404 trying to link to the /gallery or /about pages,
	but the pages kinda show, without images, if you manually inject index.php
	into the browser location field.

	The fix: Modify your httpd.conf ... line 265 has "AllowOverride None" and that
	should be "AllowOverride All", and the "LoadModule rewrite..." directive needs to
	be uncommented. See me in lab if you have questions.

-    Synchronize your repo with the team repo, if needed
-    Complete the first tutorial for this week's lab, [Static to Trivial Website Conversion](http://comp4711.jlparry.com/show/tutorial/ci-basic01)
-    Commit &amp; push your feature branch (you did remember to use one, right?) and submit a pull request to the team repo
-    [CAPTAIN] if ok, you can merge the PR

##Trivial to Basic Website Conversion (CAPTAIN)

-    Synchronize your repo with the team repo, if needed
-    Complete the second tutorial for this week's lab, [Trivial to Basic Website Conversion](http://comp4711.jlparry.com/show/tutorial/ci-basic02)
-    Commit &amp; push your feature branch (you did remember to use one, right?) and submit a pull request to the team repo
-    [CAPTAIN] if ok, you can merge the PR

##Basic to Good Website Conversion (SECOND MATE, FIRST MATE if none)

-    Synchronize your repo with the team repo, if needed
-    Complete the third tutorial for this week's lab, [Basic to Good Website Conversion](http://comp4711.jlparry.com/show/tutorial/ci-basic02)
-    Commit &amp; push your feature branch (you did remember to use one, right?) and submit a pull request to the team repo
-    [CAPTAIN] if ok, you can merge the PR
    
##Lab Conclusion (CAPTAIN)

-    Tidy up any loose ends in the repo
-    Merge the develop branch into the master branch, in the team repo
-    You are ready to submit the repo link to your dropbox for the lab

