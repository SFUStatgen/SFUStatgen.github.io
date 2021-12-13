---
layout: default
title: Working with files and disk quotas on Compute Canada
---
# Working with files and disk quotas on Compute Canada

## Compute Canada Filespace

* We can think of the filespace on cedar.computecanada.ca as three *separate* disks named '/home', '/project', and '/scratch'.
* When you log in to cedar.computecanada.ca 
as user '<user>' you will be in the '/home/<user>' directory.
* When you list the contents of '/home/<user>' you will see 'project' and 'scratch, which are
"softlinks", or short-cuts. Changing directory ('cd') to these 
will take you to '/project/def-<sponsor>/<user>' and '/scratch/<user>', respectively, where '<sponsor>' is your account sponsor (jgraham or mcneney).
    * Aside: Ignore 'projects' (plural) -- this is only useful for people
    who work with multiple sponsors
* Files in '/home' and '/project' stay permanently. By contrast, files in '/scratch' are deleted about once a month. 


## Disk quotas

* You have quotas on each disk. 
* On '/home' you have about 50GB, on '/project' you have about 2GB and on '/scratch' you have about 20TB. 
* In addition to your 2GB on /project, your sponsor (jgraham or mcneney) has a 1TB quota. 
* Files count towards quotas according to (i) which disk they are on and (ii) which "group owner" they have (see below for information on Unix groups). * 
* Files that reside *anywhere* on /project with group ownership '<user>' count towards the user's personal /project quota, files on /project with group ownership def-jgraham count towards Jinko's 1TB /project quota and files on /project with group ownership def-mcneney count towards Brad's 1TB /project quota.


## Shared space

* shared space between two sponsors is ...
* Use cp and rm, not mv, to move files from home or scratch to project.
cp first, then rm old copy, sets group ownership to def-<sponsor>

* home scratch project , getfacl, setfacl
for a directory called Testing, execute the following from the 
parent directory:
'''setfacl -R -m g:sfu-statgen:rwX Testing'''
To set the permissions for 

## Unix groups 

On Unix, files have two levels of ownership, the "owner" (user who created it) and the "group" (the Unix group . are given directories within each one. For a user named <user> sponsored by <sponsor> they are
  /home/<user>
 /project/def-<sponsor>/<user>
 /scratch/def-<sponsor>/<user>

