---
layout: default
title: Alliance Canada files and quotas
---

# Alliance Canada files and quotas

This information is specific to the cluster fir.alliancecan.ca 
that we use.

## Alliance Canada Filespace

* The filespace on fir.alliancecan.ca is comprised of three separate disks named `/home`, `/project`, and `/scratch`. Each disk is organized to host separate users.
* When you log in to fir.alliancecan.ca 
as user `<user>` you will be in the `/home/<user>` directory.
* When you list the contents of `/home/<user>` you will see `project` and `scratch`, which are "softlinks", or short-cuts. Changing directory (`cd`) to these will take you to `/project/def-<sponsor>`, your group's project directory (a communal space for the group of your account sponsor `<sponsor>`)  and `/scratch/<user>`, your personal scratch directory.
    * Aside: When you list the contents of `/home/<user>` you will also see a `projects` (plural) directory and a `nearline` directory. Ignore these for now; `projects` is only useful for people
    who work with multiple sponsors and  `nearline` is for archival storage, which we haven't been using.
* Files you put in `/home` and `/project` stay until you delete them, but files in `/scratch` are automatically deleted by the system about once a month. 

## Purpose of each disk

Roughly speaking
* `/home` is for code and other files that you work with but don't need to share with anyone.
    * Note: You should plan to share **everything** you do that leads
    to research output, such as a thesis or a paper. Fully reproducible research is a basic
    requirement of open science.
* `/project` is for files that need to be stored long-term and shared with others.
    * Scripts and data needed to reproduce your research findings should go here. 
 <!--   * Most of the research we do should be saved in the Graham and McNeney group's shared directory. See the **sfu-statgen datasharing group** below. -->
* `/scratch` is where you will do most of your computing. 
    * Copy scripts and data needed for your jobs from `/home` or `/project` to your `/scratch/<user>` directory (or a sub-directory) and submit your job scripts from there. 
    * Output files will end up in the same directory you run from. 
    * After the job finishes, copy any output you need back to `/project` or `/home`, depending on whether or not they're to be shared, respectively. (See **Copying to `/project`** below for tips on copying.)

## Disk quotas

* You have quotas on each disk. 
* On `/home` you have 50GB, on `/project` you have 2GB and on `/scratch` you have 20TB. 
* In addition to your personal 2GB quota on `/project`, your sponsor (jgraham or mcneney) has a 1TB `/project` quota. 
* Files count towards quotas according to (i) which disk they are on and (ii) which "group owner" they have (see the **Unix groups** section below for information on Unix groups).
* Files in `/home/<user>` and `/scratch/<user>` should always have group ownership `<user>` and will count towards the user's quota on those disks.
* Files in `/project` with group ownership `<user>` count towards the user's 2GB personal `/project` quota, files in `/project` with group ownership `def-jgraham` count towards Jinko's 1TB `/project` quota and files in `/project` with group ownership `def-mcneney` count towards Brad's 1TB `/project` quota.
* Important: As far as quotas on `/project` go, it doesn't 
    matter where a file is, only
    its group ownership. For example, if Jinko gives Brad permission to 
    write files to `/project/def-jgraham/` and he moves a file there 
    that has group ownership `def-mcneney`, the file counts against 
    **his** `def-mcneney` `/project` quota, not Jinko's.


## Copying files to/from `/project`

* Be careful about using the Unix `mv` command to copy files you own to `/project`. Since `mv` preserves file ownership, using it to move a file you own to the communal `/project` directory will mean that the file counts against your 2GB `<user>` quota rather than the communal 1TB quota of `def-<sponsor>`. 
* Instead, use `cp` to copy directories and files into the communal `/project` space.
* For example, say you want to copy `TestDir` from your `/scratch/<user>`
directory to `/project/def-jgraham/share`. First change directory to
`/scratch/<user>`
and then type `cp -r TestDir /project/def-jgraham/share/.` (The `-r` 
is to recursively copy sub-directories.)
* The copy of  `TestDir` in `/project/def-jgraham/shares/` will
automatically have group ownership `def-jgraham`.
* If you won't need `TestDir` in your scratch directory any more, remove it 
by typing `rm -r TestDir`.


## The sfu-statgen data-sharing group

* The group communal space in `/project` is good for sharing files between
sponsored users of the same project, but not between different projects.
* Since project members of def-jgraham and def-mcneney frequently share data,  
we've set up a data-sharing group of Share, `sfu-statgen`.
<!--* Using special tools developed by Alliance Canada we can set 
the file permissions of files that we'd like to share between
groups.-->
* The place to share files between groups is `/project/def-mcneney/share`.
* Use `cp` to copy directories and files to an appropriate 
sub-directory of the share space. 
* By default, the directories and files you copy to the Share  `/project/def-mcneney/share` will have group ownership `def-mcneney`, 
but nobody but you will be able to read, write and execute them.
* To allow other users to read, write and execute the files you copy into the Share, you need to take two more steps.
* Suppose you copied the directory `TestDir` into `/project/def-mcneney/share`. Change to this directory in the Share
and execute the following two commands
```
setfacl -d -m g:sfu-statgen:rwx TestDir
```
```
setfacl -R -m g:sfu-statgen:rwX TestDir
```

(note the capital X in the second `setfacl` command).  Other members of the `sfu-statgen` data-sharing
group can now work with `TestDir` and its contents as if they were their own.

## Unix groups 

On Unix, directories and files have two levels of ownership, the "user" 
(the user who created it) and the "group" 
(the Unix group that the user belongs to). You can see 
the ownership of files using `ls -la`. For example, 
here is an excerpt of the listing of some of the sub-directories
of the `/project/def-jgraham` directory.
We are interested in the third and fourth columns of output.
```
drwx--S---    9 epasiedn def-jgraham   4096 Nov 17 06:58 epasiedn
drwx--S---    2 jgraham  def-jgraham   4096 Mar 17  2021 jgraham
```
For the first sub-directory, the user owner is `epasiedn` and the group owner is `def-jgraham`. 
For the second sub-directory, the user owner is `jgraham` and the group owner is `def-jgraham`. 
Since the group owner is `def-jgraham` for both directories, both count against the communal
quota of the def-jgraham project.

As another example, here is a partial listing of some of the sub-directories of `/home/jgraham`:
```
drwxr-x---      5 jgraham jgraham        4096 Mar 11  2021 msprime_env
drwxr-xr-x      2 root    jgraham        4096 May 15  2019 nearline
```
For the first sub-directory, the user owner and group owner are both `jgraham`. For the second
sub-directory, the user owner is `root` (the super-user) and the group owner is `jgraham`.
We can see that the second sub-directory was created by `root` but counts toward `jgraham`'s 50GB personal
quota on `/home`.
   
