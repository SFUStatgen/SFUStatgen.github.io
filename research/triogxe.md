---
layout: default
title: trioGxE
---

### An R package implementing a data smoothing approach to explore and test gene-environment interaction in case-parent trio data

Complex traits result from an interplay between genes and environment. A better understanding of their joint effects can help refine understanding of the epidemiology of the trait. Various tests have been proposed to assess the statistical interaction between genes and the environment (GxE) in case-parent trio data. However, these tests can lose power when the form of GxE departs from that for which the test was developed. To address this limitation, we developed and implemented a data-smoothing approach to estimate and test GxE between a single nucleotide polymorphism and a continuous environmental covariate. For estimating GxE, we fit a generalized additive model using penalized likelihood. The resulting point- and interval-estimates of GxE lead to a graphical display, which can serve as a visualization tool for exploring the form of interaction. A permutation test of GxE accounts for the extra uncertainty introduced by the smoothing process.

The [trioGxE](http://cran.r-project.org/package=trioGxE) R package is available on the Comprehensive R Archive Network <a href="http://cran.r-project.org">website</a>. The underlying statistical methods are described in <a href="http://dx.doi.org/10.1515/sagmb-2013-0023">Shin <i>et al.</i> (2014)</a>

You will have to have <a href="http://www.r-project.org">R</a> installed on your system to use it. To install trioGxE you can execute the following command in R:

<pre>install.packages(&quot;trioGxE&quot;)</pre>

The software is licenced under the <a href="http://www.gnu.org">GNU</a> <a href="http://www.gnu.org/licenses/gpl.html">General Public Licence</a>.