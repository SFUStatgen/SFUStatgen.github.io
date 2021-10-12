---
layout: default
title: Compute Canada
---

# Getting started with Compute Canada

### Registering for an account

Before you can use the Compute Canada resources you will need to register for an account. Your account will be linked to a "sponsor", 
so before you start the registration, send an email to your supervisor (Jinko or Brad) and ask them for their Compute Canada
user ID (CCRI).

Next, go to the Compute Canada login/registration page at

[https://ccdb.computecanada.ca/security/login](https://ccdb.computecanada.ca/security/login)

and click on "Register" near the bottom right. Fill out the following application pages. When asked about your "Position" say MSc or PhD 
student, as appropriate, under "Sponsored User". After you submit the form, the Compute Canada system should send your supervisor
an email to approve your request. Please let them know when you submit the form so that they can keep an eye out for the approval email.

### Getting to know Unix

The Compute Canada servers run the Unix operating system. If you are unfamiliar with Unix, you can consult an online tutorial, such as [this one](https://www.cs.sfu.ca/~ggbaker/reference/unix/).

### Logging in to cedar

The cluster that we use most is [cedar.computecanada.ca](https://docs.computecanada.ca/wiki/Cedar). You will need to log in to cedar
with an SSH client. See the Compute Canada [documentation on SSH](https://docs.computecanada.ca/wiki/SSH) for more information.

### Running your jobs

To run a job you must create what's called a "batch script" and submit it to a "scheduler". 

* See the [introduction to schedulers](https://docs.computecanada.ca/wiki/What_is_a_scheduler%3F) for background on schedulers and compute clusters.
* See the [running jobs](https://docs.computecanada.ca/wiki/Running_jobs) documentation for basic information on running jobs on Compute Canada.
* See the [array jobs](https://docs.computecanada.ca/wiki/Job_arrays) documentation to see how to run the same job multiple times, possibly with different inputs, randome seeds, etc. We often use array jobs to run Monte Carlo simulations; e.g., for importance sampling or to get permutation/bootstrap distributions.
* See the [META](https://docs.computecanada.ca/wiki/META_package_for_serial_farming) documentation for an alternative to array jobs that requires less work for the scheduler. META is supposed to have several convenience features for users, such as the ability to automatically re-submit jobs from an initial submission that crashed or ran out of time. No one in our group has used META yet. You can watch a [webinar](https://www.youtube.com/watch?v=GcYbaPClwGE).  

### Getting help

* WestGrid (the Western Canada division of Compute Canada) has its own [youtube channel](https://www.youtube.com/user/WGSeminarSeries) where they post videos of past seminars/webinars.
* Sharcnet (the Ontario division of Compute Canada) also has a [youtube channel](https://www.youtube.com/channel/UCCRmb5_GMWT2hSlALHlwIMg). Their "new users" webinars look useful.
* Contact [Compute Canada tech support](https://docs.computecanada.ca/wiki/Technical_support).

### Running R in batch mode

* See the [Parallel Computing in R with WestGrid](https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/ParallelComputing_inR_CC.pdf)
 presentation by Bhagya Karunarathna. (Note: WestGrid is the western-Canada division of Compute Canada.)

