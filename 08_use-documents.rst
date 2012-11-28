.. _use_documents:

#############################
 Sample Documentation
#############################

This sample will create a new documentation project for a student Journal.

In GitHub Account
-----------------------------

Create a new repository in GitHub, naming it :file:`doc-journal`.

+ Initialize it with a :file:`readme` so it can be cloned.
+ Do not add a :file:`.gitignore` now.
+ Click :guilabel:`create repository`.

In Cloud9 Account
-----------------------------

+ At the top of the left menu, click on :guilabel:`Your Account`.
+ Expand :guilabel:`PROJECTS ON GITHUB` to show available projects.
+ Click :guilabel:`doc-journal` to select it.
+ Click the :guilabel:`CLONE TO EDIT` button.
+ In the :guilabel:`Clone from URL` dialog, click button :guilabel:`CREATE`.
+ Click the :guilabel:`START EDITING` button to open your project workspace.

Cloud9 Project Workspace
-----------------------------

Sphinxdoc documenation tools are installed using python package manager
``easy_install``. At the console command line, type::

  easy_install -U sphinx

Download Files to Include
-----------------------------

We wish to include a series of files in this project:

+ :download:`.gitignore for Sphinx projects <_downloads/.gitignore>`
+ :download:`Adding documentation to a code project <_downloads/docbranch-add.sh>`
+ :download:`Starting a documentation project <_downloads/docproject-start.sh>`
+ :download:`Deploy documentation to GitHub gh-pages <_downloads/github-deploy.sh>`

The web browser downloads files to a local device, not to the Cloud9 workspace. 
The Linux :command:`wget` command can return these files to Cloud9::

  wget http://vstem-davenport.github.com/doc-devcloud/_downloads/.gitignore
  wget http://vstem-davenport.github.com/doc-devcloud/_downloads/docbranch-add.sh
  wget http://vstem-davenport.github.com/doc-devcloud/_downloads/docproject-start.sh
  wget http://vstem-davenport.github.com/doc-devcloud/_downloads/github-deploy.sh

After getting the files, click the :guilabel:`gear icon` on top of the left 
sidebar, and choose :guilabel:`Refresh Project Tree`.