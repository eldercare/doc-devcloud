.. _use_heroku:

#############################
 Using Heroku
#############################

Heroku provides a free web application deployment services, integrated with 
the Cloud9 development environment through Git and GitHub. Following is a 
brief outline for configuring and deploying a project on Heroku.

Add Heroku Server to Project
=============================

+ Open a project in Cloud9
+ In the Cloud9 Project, choose :menuselection:`View --> Console` from the menu
+ At the console command line, type::
  
    git remote add heroku git@heroku.com:__heroku-server__.git
  
  where ``__heroku-server__`` is replaced with your heroku server name

+ To see the new git heroku deployment branch, type::

    git remote -v

+ After making changes to the project in Cloud9 and pushing to the GitHub 
  repository, deploy changes on Heroku with the additional command::

    git push heroku master

