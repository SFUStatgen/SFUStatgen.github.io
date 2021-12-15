---
layout: default
title: Compute Canada files and quotas
---

# Compute Canada files and quotas

This information is specific to the cluster cedar.computecanada.ca 
that we use.

## Compute Canada Filespace

* The filespace on cedar.computecanada.ca is comprised of three separate disks named `/home`, `/project`, and `/scratch`. Each disk is organized to host separate users.
* When you log in to cedar.computecanada.ca 
as user `<user>` you will be in the `/home/<user>` directory.
* When you list the contents of `/home/<user>` you will see `project` and `scratch`, which are "softlinks", or short-cuts. Changing directory (`cd`) to these will take you to `/project/def-<sponsor>` (i.e. your group's project directory, a communal space)  and `/scratch/<user>` (i.e. your personal scratch directory), respectively, where `<sponsor>` is your account sponsor (jgraham or mcneney).
    * Aside: When you list the contents of `/home/<user>` you will also see a `projects` (plural) directory and a `nearline` directory. Ignore these. `projects` is only useful for people
    who work with multiple sponsors and  `nearline` is for archival storage, which we haven't been using.
* Files you put in `/home` and `/project` stay are there until you delete them yourself, but files in `/scratch` are automatically deleted by the system about once a month. 

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
    * After the job finishes, copy any output you need back to `/project` or `/home`, depending on whether or not they are to be shared. (See **Copying to `/project`** below for tips on copying.)

## Disk quotas

* You have quotas on each disk. 
* On `/home` you have 50GB, on `/project` you have 2GB and on `/scratch` you have 20TB. 
* In addition to your personal 2GB quota on `/project`, your sponsor (jgraham or mcneney) has a 1TB `/project` quota. 
* Files count towards quotas according to (i) which disk they are on and (ii) which "group owner" they have (see the **Unix groups** section below for information on Unix groups).
* Files in `/home/<user>` and `/scratch/<user>` should always have group ownership `<user>` and will count towards the user's quota on those disks.
* Files in `/project` with group ownership `<user>` count towards the user's 2GB personal `/project` quota, files in `/project` with group ownership `def-jgraham` count towards Jinko's 1TB `/project` quota and files in `/project` with group ownership `def-mcneney` count towards Brad's 1TB `/project` quota.
    * Important note: As far as quotas on `/project` go, it doesn't 
    matter where a file is, only
    its group ownership. For example, if Jinko gives Brad permission to 
    write files in `/project/def-jgraham/` and he moves a file there 
    that has group ownership `def-mcneney`, the file counts against 
    **his** `def-mcneney` `/project` quota, not Jinko's.


## Copying files to/from `/project`

* Avoid using the Unix `mv` command when copying files. `mv` preserves file ownership, and this is not what you want when copying files to/from
`/project`. 
* Instead, use `cp` and `rm` to copy directories and files.
* For example, say you want to copy `TestDir` from your `/scratch/<user>`
directory to `/project/def-mcneney/share`. First change directory to
`/scratch/<user>`
and then type `cp -r TestDir /project/def-mcneney/share/.` (The `-r` 
is to recursively copy sub-directories.)
* The copy of  `TestDir` in `/project/def-mcneney/shares/` will
automatically have group ownership `def-mcneney`.
* If you won't need `TestDir` in your scratch directory any more, remove it 
by typing `rm -r TestDir`.


## sfu-statgen datasharing group

* The communal space in `/project` is good for sharing files between
sponsored users of the same project, but not between projects.
* Since we need to share data between Jinko's and Brad's projects
we have what's called a datasharing group, called `sfu-statgen`. 
* Using special tools developped by Compute Canada we can set 
the file permissions of files that we'd like to share between
groups.
* The place to share files is `/project/def-mcneney/share`.
* Use `cp` to copy directories and files to an approprioate 
sub-directory of the share space. 
* The files you copy will have group ownership `def-mcneney`, 
but to share them there are two more steps to take.
* Suppose you copied the directory `TestDir` into
`/project/def-mcneney/share`. Change to this directory
and execute the following two commands

'''
setfacl -d -m g:sfu-statgen:rwx Testing
'''

'''
setfacl -R -m g:sfu-statgen:rwX Testing
'''

(note the capital X in the second `setfacl` command).

## Unix groups 

On Unix, files have two levels of ownership, the "owner" 
(the user who created it) and the "group" 
(the Unix group that the user belongs to).

```
[mcneney@cedar5 share]$ ls -la
total 36
drwxrws---+ 7 mcneney  def-mcneney  4096 Mar 20  2021 .
drwxrws--x+ 9 mcneney  def-mcneney  4096 Dec 13 17:00 ..
drwxrws---+ 3 mcneney  def-mcneney 12288 Jun  6  2020 1000g
drwxrws---+ 6 mcneney  def-mcneney  4096 Jun  9  2020 adni
drwxrws---+ 3 mcneney  def-mcneney  4096 Mar 20  2021 impute2
drwxrws---+ 6 bhagya85 def-mcneney  4096 Dec 13 09:49 PBJ
drwxrws---+ 2 mcneney  def-mcneney  4096 May  4  2021 simht
```


. are given directories within each one. For a user named <user> sponsored by <sponsor> they are
  /home/<user>
 /project/def-<sponsor>/<user>
 /scratch/def-<sponsor>/<user>

