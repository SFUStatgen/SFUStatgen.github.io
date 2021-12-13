---
layout: default
title: Running jobs on Compute Canada
---

### Batch scripts and schedulers

To run a job you must create what's called a "batch script" and submit it to a "scheduler". 

* See the [introduction to schedulers](https://docs.computecanada.ca/wiki/What_is_a_scheduler%3F) for background on schedulers and compute clusters.
* See the [running jobs](https://docs.computecanada.ca/wiki/Running_jobs) documentation for basic information on running jobs on Compute Canada.
* See the [array jobs](https://docs.computecanada.ca/wiki/Job_arrays) documentation to see how to run the same job multiple times, possibly with different inputs, random seeds, etc. We often use array jobs to run Monte Carlo simulations; e.g., for importance sampling or to get permutation/bootstrap distributions.
* See the [META](https://docs.computecanada.ca/wiki/META_package_for_serial_farming) documentation for an alternative to array jobs that requires less work for the scheduler. META is supposed to have several convenience features for users, such as the ability to automatically re-submit jobs from an initial submission that crashed or ran out of time. No one in our group has used META yet. You can watch a [webinar](https://www.youtube.com/watch?v=GcYbaPClwGE).  

### Running R in batch mode

* See the [Parallel Computing in R with WestGrid](https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/ParallelComputing_inR_CC.pdf)
 presentation by Bhagya Karunarathna. (Note: WestGrid is the western-Canada division of Compute Canada.)

