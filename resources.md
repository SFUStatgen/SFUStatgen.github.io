---
layout: default
title: Resources
---
# Research and Computing Resources

## General Computing

* These days we do most of our computationally-demanding work on [Compute Canada](https://computecanada.ca).
See our [Getting started](resources/computecan.html) page for information on registering with Compute Canada and accessing their resources.
* See the Department's webpage on <a href="https://www.sfu.ca/stat-actsci/research/research-resources/computing-research.html">computing</a> for information on getting help, access to the Unix network and software available to SFU faculty, staff and students
* Some useful <a href="http://biostat.mc.vanderbilt.edu/wiki/Main/ProgrammingTipsForStatisticians">programming tips for statisticians.</a>
* General <a href="http://cscs.umich.edu/%7Ecrshalizi/weblog/593.html">advice</a> about how to approach programming.


## Simulating Genomic Data

* Dick Hudson's [ms program](http://home.uchicago.edu/rhudson1/source/mksamples.html)
* [fastsimcoal2](http://cmpg.unibe.ch/software/fastsimcoal2)
* [msprime](https://tskit.dev/msprime/docs/stable/intro.html): a Python package for simulation
that uses a novel "succinct tree sequences" data structure to efficiently
store the ancestral history of a set of DNA sequences. See also:
    * Payman Nickchi's [tutorial materials](https://github.com/paymannickchi/msprime) 
    on GitHub and [command-line demo](https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/mspcommands.txt)
    * Documentation for the [tskit](https://tskit.dev/tskit/docs/stable/) Python package that implements the "succinct tree sequences" data structure that underlies msprime.
* [SLiM](https://messerlab.org/slim/)

## Computing with R

* <a href="https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/DIYRpackage.pdf">Creating R packages with RStudio and roxygen2</a>, by Christina Nieuwoudt, based on the evolving online textbook [R packages](https://r-pkgs.org/) by Hadley Wickham and Jenny Bryan. 
* <a href="https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/ParallelComputing_inR_CC.pdf">Parallel Computing in R with WestGrid</a>, by Bhagya Karunarathna.
* Hadley Wickham's online [Advanced R](https://adv-r.hadley.nz/) textbook includes useful information on
    * [debugging](https://adv-r.hadley.nz/debugging.html)
    * [profiling](https://adv-r.hadley.nz/perf-measure.html)
    * [optimizing](https://adv-r.hadley.nz/perf-improve.html) and
    * [integrating C++](https://adv-r.hadley.nz/rcpp.html) using [Rcpp](http://www.rcpp.org/). 

## Computing with C/C++

Our group uses the GNU tools, such as the gcc C compiler and the g++ C++ compiler, for software development
* How you [access these tools](resources/Ctools.html) depends on your operating system
* The [GNU Scientific Library](https://www.gnu.org/software/gsl/) includes implementations of **many** common scientific functions that you can include in your C or C++ programs. This extensive library includes functions for summary statistics, vectors and matrices, random number generation, linear algebra, Monte Carlo integration and more.
    

<h2>TeX/LaTeX<br>
</h2>
<ul>
<li>Templates for SFU Master's projects and PhD theses in LaTeX.<ul>
<li>&nbsp;<a href="http://www.lib.sfu.ca/help/publish/thesis/templates#latex-template">LaTeX template</a> from the SFU Library.<br>
</li>
<li>A BibTeX sytle file forwarded by Flora Qu: <a href="/content/dam/sfu/stat/documents/Statgen/jasasty-ay.bst">jasasty-ay.bst</a>. The &quot;ay&quot; in the name appears to refer to &quot;author-year&quot; style references [e.g. Qu (2009)], rather than numeric citations in the text. Flora reports having had trouble with other bibtex style files, but that this one works. She notes: &quot;When you use this bib style file, you need to add \usepackage{natbib} in the main tex file.&quot;</li>
<li>In addition to the LaTeX files, MSc students may be interested in looking at a few recent projects from the department to get sense of the scope and size of a typical MSc project: (i) <a href="http://www.sfu.ca/content/dam/sfu/stat/alumnitheses/2015/chenlu%20shi_finalproject.pdf">Chenlu Shi</a>, (ii) &nbsp;<a href="http://www.sfu.ca/content/dam/sfu/stat/alumnitheses/2014/MSc%20Project%20Report%20-%20Kunasekaran%20Nirmalkanna.pdf">Kunasekaran Nirmalkanna</a>, (iii) &nbsp;<a href="http://www.sfu.ca/content/dam/sfu/stat/alumnitheses/2014/RachelLipson%20Final%201141.pdf">Rachel Lipson</a></li>
</ul>
</li>
<li>LaTeX posters:<ul>
<li>The package tizkposter is popular these days.<ul>
<li>Download the LaTeX package <a href="http://mirrors.ctan.org/graphics/pgf/contrib/tikzposter.zip">zipfile</a>,</li>
<li>use unzip to unpack it into its own directory,</li>
<li>change to this directory and run &quot;latex tikzposter.ins&quot; to generate the class files and examples.</li>
<li>The documentation file is tikzposter.pdf. An example poster is in the file tikzposter-example.tex. A template that you can use as a starting point for your own posters is in the file tizkposter-template.tex.</li>
</ul>
</li>
<li>Another possibility is the beamerposter package, which you may prefer over tikzposter if you use beamer for presentations.<ul>
<li>Downoad the LaTeX package <a href="http://mirrors.ctan.org/macros/latex/contrib/beamerposter.zip">zipfile</a>,</li>
<li>use unzip to unpack it into its own directory and change to this directory.</li>
<li>The documentation is in the file beamerposter.pdf, and an example is in the file example.tex.</li>
</ul>
</li>
</ul>
</li>
<li>Information from Jean Shin (Dated Nov. 3, 2010) on poster printing places @ SFU and costs:<ul>
<li>School of Resource and Environmental Management (REM) [updated by Elena Szefer, Apr. 2015]:<ul>
<li>Regular paper only; $48 for an A0 poster.<br>
</li>
<li>If you send a pdf file to Laurence Lee (laurence_lee@sfu.ca) by 11AM, you can have the poster by 2 or 3PM in the same day</li>
<li>You can send the grant account number to be charged to Laurence. Charlene can provide the account number that is required.&nbsp;<br>
</li>
<li>Before they release your poster to you, your supervisor needs to sign an invoice to agree to have their account charged.&nbsp; You need to return this invoice to the REM office.&nbsp; It's also possible to pick up a hard copy of the invoice before your poster is done printing to have signed by your supervisor.</li>
<li>I'm not sure which option is best, but it would be a good idea to ask about the invoice with Laurence when you place your order to make sure that you will be able to get your poster in time.</li>
</ul>
</li>
<li>Cornerstone:<br>
<ul>
<li>$3.99/ sq. ft (regular paper) and $5.99/ sq. ft (thicker glossy paper)</li>
<li>they need 1 business day</li>
<li>Bhagya Karunarathna (Apr. 2015) reports a cost of about $40 for an A0 poster on regular paper, but no invoicing.</li>
</ul>
</li>
<li>IRMACS:<ul>
<li>$6 per square-foot (white background) or $7 (dark background)</li>
<li>they need at least 24 hours</li>
</ul>
</li>
</ul>
A typical sized poster (4ft-by-3ft) costs $48 (REM), $48~$72 (cornerstone) and $72 ~ $84 (IRMACS).</li>
</ul>

## Old documents and resources

* See [here](resources/olddocs.html) for other, possibly out-dated, resources
