---
layout: default
title: Compute Canada files and quotas
---

# Compute Canada files and quotas

This information is specific to the cluster cedar.computecanada.ca 
that we use.

## Compute Canada Filespace

* We can think of the filespace on cedar.computecanada.ca as three *separate* disks named `/home`, `/project`, and `/scratch`.
* When you log in to cedar.computecanada.ca 
as user `<user>` you will be in the `/home/<user>` directory.
* When you list the contents of `/home/<user>` you will see `project` and `scratch`, which are "softlinks", or short-cuts. Changing directory (`cd`) to these will take you to `/project/def-<sponsor>/<user>` and `/scratch/<user>`, respectively, where `<sponsor>` is your account sponsor (jgraham or mcneney).
    * Aside 1: Ignore `projects` (plural) -- this is only useful for people
    who work with multiple sponsors.
    * Aside 2: The `nearline` directory is for archival storage. We haven't
    been using this.
* Files in `/home` and `/project` are permanent, until you delete them yourself, but files in `/scratch` are deleted by the system about once a month. 

## Purpose of each disk

Roughly speaking
* `/home` is for code and other files that you work with but don't need to share with anyone.
    * Note: You should plan to share **everything** you do that leads
    to research output, such as a thesis or a paper. This is a basic
    requirement of open science.
* `/project` is for files that need to be stored long-term and shared with others.
    * Scripts and data needed to reproduce your research findings should go here. 
    * Most of the research we do should be saved in the Graham and McNeney group's shared directory. See the **sfu-statgen datasharing group** below.
* `/scratch` is where you will do most of your computing. 
    * Copy scripts and data needed for your jobs from `/home` or `/project` to your `/scratch/<user>` directory (or a sub-directory) and submit your job scripts from there. 
    * Output files will end up in the same directory you run from. 
    * Copy any output you need back to `/project` or `/home`, depending on whether or not they are to be shared. (See **Copying to `/project`** below for tips on copying.)

## Disk quotas

* You have quotas on each disk. 
* On `/home` you have 50GB, on `/project` you have 2GB and on `/scratch` you have 20TB. 
* In addition to your personal 2GB quota on `/project`, your sponsor (jgraham or mcneney) has a 1TB `/project` quota. 
* Files count towards quotas according to (i) which disk they are on and (ii) which "group owner" they have (see below for information on Unix groups).
* Files in `/home/<user>` and `/scratch/<user>` should always have group ownership `<user>` and will count towards the user's quota on those disks.
* Files in `/project` with group ownership `<user>` count towards the user's 2GB personal `/project` quota, files in `/project` with group ownership `def-jgraham` count towards Jinko's 1TB `/project` quota and files in `/project` with group ownership `def-mcneney` count towards Brad's 1TB `/project` quota.
    * Important note: As far as quotas go, it doesn't 
    matter where on `/project` a file is, only
    its group ownership. For example, if Jinko gives Brad permission to 
    write files in `/project/def-jgraham/` and he moves a file there 
    that has group ownership `def-mcneney`, the file counts against 
    **his** `def-mcneney` `/project` quota, not Jinko's.


## Copying files to/from `/project`

* Avoid using the Unix `mv` command when copying files. `mv` preserves file ownership, and this is not what you want when copying files to/from
`/project`. 
* Instead, use `cp` and `rm` to copy directories as follows (copying individual files is similar).
* For example, say you want to copy `TestDir` from your `/scratch/<user>`
directory to `/project/def-mcneney/share`. First change directory to
`/scratch/<user>`
and then type `cp -R TestDir /project/def-mcneney/share/.` 
* Within `/project/def-mcneney/share`, the directory `TestDir` will
automatically have group ownership `def-mcneney`, inherited from 
its new parent directory ('project/def-mcneney/share`) when it was
copied.
* If you won't need `TestDir` in your scratch directory any more, remove it 
with `rm -R TestDir`. 


## SFU Statgen datasharing group

* shared space between two sponsors is ...
* Remember to cp, not mv files to here
* Share with the group with setfacl
for a directory called Testing, execute the following from the 
parent directory:
'''setfacl -R -m g:sfu-statgen:rwX Testing'''
To set the permissions for 

## Unix groups 

On Unix, files have two levels of ownership, the "owner" (user who created it) and the "group" (the Unix group . are given directories within each one. For a user named <user> sponsored by <sponsor> they are
  /home/<user>
 /project/def-<sponsor>/<user>
 /scratch/def-<sponsor>/<user>

