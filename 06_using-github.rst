.. _use_github:

#############################
 Using GitHub
#############################

Create a New Repository
=============================

.. note:: Replace ``__username--`` with your **username** in following commands. 

.. sidebar:: GitHub user menu bar

  .. image:: _images/06_github-01.png

+ Visit the `GitHub website <https://github.com>`_ 
+ Click your name to go to your own page on GitHub
+ To the right of your name, click the **+** to start a new repository
+ Fill out **Repository name**, **Description**, and **.gitignore** entries
+ Click button :guilabel:`Create repository` to generate the repository

.. image:: _images/06_github-02.png

GitHub will make a fresh repository and open it for you.

Fork a Remote Project
=============================

There is no need to start from scratch when creating a documentation project. 
Instead, clone or fork someone else's open source work. With your GitHub 
account, 

+ visit the `GitHub page <https://github.com/Vstem-Davenport>`_ 
+ find the :kbd:`doc-devcloud` repository and click the name,
+ then click the :guilabel:`fork` button at the top right of the page.

.. image:: _images/06_github-1.png

GitHub will make a copy of the self-publish repository for you, and then switch 
to view your copy.

Clone a Remote Project
=============================

Once you own a repository on GitHub, you will want to clone it. The GitHub 
repository is remote, and cloning makes a local copy which you can edit. 
Here is the console command::
	 
	 git clone (link_to_your_project) ~/Projects/doc-publishself

There are two parameters to the :command:`git clone` command. First is your 
project name, which is the text following "Git Read-Only" in the image below. 
(But copy the text from your fork of the repository please, so it will have 
your name instead of mine.) The second parameter is the folder name to create 
for the project.

.. image:: _images/06_github-2.png

Ask Git a Question
=============================

Type the following commands to query git in the :file:`doc-publishself` 
project:: 
	 
	 cd ~/Projects/doc-publishself
	 git branch -a

Git shows two branches in this project, **gh-pages** and **master**, and 
**master** is active. If the source is in branch **master**, then what is in 
the **gh-pages** branch?

Git an Answer
=============================

The answer is, gh-pages contains HTML pages and other content for the website 
you are viewing. 

Now let's create a gh-pages branch for your doc-firsttask repository. Here are 
the commands::
	 
	 cd ~/Projects/doc-firsttask
	 git add .
	 git commit -m "Commit all current changes before branching"
	 git symbolic-ref HEAD refs/heads/gh-pages
	 rm .git/index
	 git clean -fdx
	 git branch master

Refer to the **Project Pages Manually** section of `GitHub help 
<http://help.github.com/pages/>`_ for more information.

Pushing to GitHub
=============================

You may have noticed: **doc-publishself** contains a repository from GitHub. 
Committed changes in the doc-publishself folder are updated to GitHub with the 
command :command:`git push`. 

Moving Projects to GitHub
=============================

On the other hand, the **doc-firsttask** repository is local to your 
workstation. To archive and share and existing project, you need to create a 
repository on GitHub. On your GitHub home page, click the 
:guilabel:`New repository` button, describe the repository, and then create it. 

.. image:: _images/06_github-3.png

.. image:: _images/06_github-4.png

Your new GitHub repository will display a remote link address, somewhat like 
:kbd:`git@github.com:__username__/__repositoryname__.git`. Using the following 
commands as a template, you can update your local repository to point to the 
new GitHub repository as a remote master::
	 
	 cd ~/Projects/doc-firsttask
	 git remote add -f -t master -m master origin git@github.com:_username_/_repository_.git
	 git merge origin

.. Warning::
	 Use the remote URL for your repository in the preceding commands, instead 
	 of pasting in :kbd:`git@github.com:_username_/_repository_.git`.
