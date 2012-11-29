.. _use_sphinxdoc:

#############################
 Documentation Sample Project
#############################

This exercise will create a new documentation project for a student Journal.

Create a Project Workspace
=============================

In Your GitHub Account
-----------------------------

Create a new repository in GitHub, naming it :file:`doc-journal`.

+ Initialize it with a :file:`readme` so it can be cloned.
+ Do not add a :file:`.gitignore` now.
+ Click :guilabel:`create repository`.

In Your Cloud9 Account
-----------------------------

+ At the top of the left menu, click on :guilabel:`Your Account`.
+ Expand :guilabel:`PROJECTS ON GITHUB` to show available projects.
+ Click :guilabel:`doc-journal` to select it.
+ Click the :guilabel:`CLONE TO EDIT` button.
+ In the :guilabel:`Clone from URL` dialog, click button :guilabel:`CREATE`.
+ Click the :guilabel:`START EDITING` button to open your project workspace.

Install Sphinxdoc in Cloud9
-----------------------------

Sphinxdoc documenation tools are installed using python package manager
``easy_install``. At the console command line, type::

  easy_install -U sphinx

Download Files to Include
-----------------------------

We wish to include some files in this project which are downloadable from the 
following links:

+ :download:`gitignore for Sphinx projects <_downloads/.gitignore>`
+ :download:`Adding documentation to a code project <_downloads/docbranch-add.sh>`
+ :download:`Starting a documentation project <_downloads/docproject-start.sh>`
+ :download:`Deploy documentation to GitHub gh-pages <_downloads/github-deploy.sh>`

Now here is the problem: the web browser downloads files to a local device, not 
to the Cloud9 workspace. To return files to Cloud9, use the Linux 
:command:`wget` command instead. Copy and paste the following commands into the 
console command line::

  wget http://vstem-davenport.github.com/doc-devcloud/_downloads/.gitignore
  wget http://vstem-davenport.github.com/doc-devcloud/_downloads/docproject-start.sh
  wget http://vstem-davenport.github.com/doc-devcloud/_downloads/github-deploy.sh

After getting the files, click the :guilabel:`gear icon` on top of the left 
sidebar, and choose :guilabel:`Refresh Project Tree` to see the additions.

Initialize Sphinxdoc
=============================



