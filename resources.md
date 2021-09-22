---
layout: default
title: Resources
---
# Research and Computing Resources

<h2><b>General Computing</b></h2>
<ul>
<li>A recent overview of the computing resources in Statistics and Actuarial Science from the <a href="https://stat.sfu.ca/content/dam/sfu/stat/documents/comp2014.pdf">2014 computing seminar</a>.</li>
<li>The Departmental webpage on <a href="https://stat.sfu.ca/research/computing.html">computing</a>, including information on the <a href="https://www.rcg.sfu.ca/documentation/#_the_colony_hpc_cluster">Colony cluster</a>, the computing cluster used by members of the Department.<br>
</li>
<li>Some useful <a href="http://biostat.mc.vanderbilt.edu/wiki/Main/ProgrammingTipsForStatisticians">programming tips for statisticians.</a></li>
<li>General <a href="http://cscs.umich.edu/%7Ecrshalizi/weblog/593.html">advice</a> about how to approach programming.</li>
</ul>
## Simulating Genomic Data

* Dick Hudson's [ms program](http://home.uchicago.edu/rhudson1/source/mksamples.html)
* [fastsimcoal2](http://cmpg.unibe.ch/software/fastsimcoal2)
* [msprime](https://tskit.dev/msprime/docs/stable/intro.html): a Python package for simulation. See also:
that uses a novel "succinct tree sequences" data structure to efficiently
store the ancestral history of a set of DNA sequences. See also:
    * Payman Nickchi's [tutorial materials](https://github.com/paymannickchi/msprime) 
    on GitHub and [command-line demo](https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/mspcommands.txt)
    * Documentation for the [tskit](https://tskit.dev/tskit/docs/stable/) Python package that implements the "succinct tree sequences" data structure that underlies msprime.
<h2><b>Computing with R</b></h2>
<ul>
<li>Configuring the necessary <a href="/content/sfu/stat/statgen/resources/r-tools-for-building-packages-on-windows.html">R tools to allow you to build your own R packages on Windows</a>.</li>
<li><a href="https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/DIYRpackage.pdf">Creating R packages with RStudio and roxygen2</a>, by Christina Nieuwoudt.</li>
<li><a href="https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/ParallelComputing_inR_CC.pdf">Parallel Computing in R with WestGrid</a>, by Bhagya Karunarathna.</li>
<li><a href="https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/RcppandR.pdf">Integrating R with C++ and C</a>, by Biljana&nbsp; Stojkova and Edouard Djeutem, as part of their course on Statistical Computing. Biljana has also provided a link to her <a href="https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/FinalReport.pdf">final proje</a>ct from Stat Computing, including the <a href="https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/R%20Functions%20and%20Data%20supporting%20Final%20Report.rar">R scripts and other fil</a>es that support the project.</li>
</ul>
<h2>Computing with C/C++</h2>
<p>Our group uses the GNU tools, such as the gcc C compiler and the g++ C++ compiler, for software development. How you access these tools depends on your operating system.</p>
<h3>Linux</h3>
<ul>
<li>GNU tools come with any Linux distribution (Linux itself is GNU) and are available on the Department Linux servers such as queen.rcg.sfu.ca, oak.fas.sfu.ca,&nbsp;rcg-linux-ts1.rcg.sfu.ca and dumbcane.fas.sfu.ca<br>
</li>
</ul>
<h3>Windows</h3>
<p>Windows users will have to install the tools themselves. Two options are<a href="http://cygwin.com"></a> <a href="www.mingw.org">MinGW</a> and <a href="http://cygwin.com">cygwin.</a><br>
</p>
<ul>
<li>MinGW is a contraction of &quot;minimalist GNU for Windows&quot;. Though not as full-featured a toolset as cygwin (see below) MinGW has the advantage that it is able to compile binary executable files that do not rely on any system-specific libraries, making these binary executables portable across systems.<ul>
<li>Complete installation instructions from the <a href="http://mingw.org">MinGW website</a> are available on their <a href="http://www.mingw.org/wiki/Getting_Started">Getting Started</a> page.</li>
</ul>
</li>
<li>Cygwin provides a complete Unix-like environment for Windows computers.&nbsp; &nbsp;Binary executables compiled under cygwin rely on cygwin-specific libraries and hence can only be run by users with the same system as the one on which the binary file was compiled.<br>
<ul>
<li>Full cygwin installation instructions are available at <a href="https://cygwin.com/cygwin-ug-net/setup-net.html">here</a>.</li>
</ul>
</li>
</ul>
<h3>Mac</h3>
<p>The development tools for Mac are part of a package called the &quot;Xcode command line tools&quot;. Apple does not include this tool set by default.</p>
<ul>
<li>The recommended way to install Command Line Tools is to type the following from a Terminal window:<pre>
xcode-select --install
</pre>
If this installation method does not work for you, this <a href="http://stackoverflow.com/questions/9329243/xcode-4-4-and-later-install-command-line-tools">thread on Stackexchange</a> may be helpful for providing a work-around.<br>
</li>
</ul>
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
<li>You can send the grant account number to be charged to Laurence. Sadika can provide the account number that is required.&nbsp;<br>
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
<h2><b>Old Documents <br>
</b></h2>
<p>&nbsp;</p>
<ul>
<li>Templates for LaTeX posters:<ul>
<li>A template for a 2-column poster, courtesy of Kelly Burkett, is available as a <a href="/content/dam/sfu/stat/documents/Statgen/poster_2column.tar.gz">gzipped tar file</a> (for Unix -- unpack with with tar xzvf poster_2column.tar.gz) or as a <a href="/content/dam/sfu/stat/documents/Statgen/poster_2column.zip">zip file</a> (for Windows). The archive includes a template .tex file and a complete poster.</li>
<li>A template for a 3-column poster, courtesy of Jean Shin, is available as a <a href="/content/dam/sfu/stat/documents/Statgen/poster_3column.tar.gz">gzipped tar file</a> (for Unix -- unpack with with tar xzvf poster_3column.tar.gz) or as a <a href="/content/dam/sfu/stat/documents/Statgen/poster_3column.zip">zip file</a> (for Windows). The archive includes a template .tex file and a complete poster.</li>
</ul>
</li>
<li><b>R Graphics using the Grid Package</b><br>
by Sigal Blay, January 2006.<br>
The grid package provides a low-level graphics system to produce reusable, editable graphical components.<br>
<b>Formats:</b> <a href="http://www.sfu.ca/%7Esblay/R/grid.ppt">PowerPoint</a><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <a href="http://www.sfu.ca/%7Esblay/R/grid.txt">Text file</a></li>
<li><p><b><a href="http://www.sfu.ca/%7Esblay/R#docs">How to Inspect R package documentation </a></b><br>
by Sigal Blay, 2005.</p>
</li>
<li><p><b>Using the 'snow' R package </b><br>
by Sigal Blay, January 2005.<br>
The 'snow' package provides a high-level interface for using a workstation cluster for parallel computations in R. <b>snow Simplified</b> is a friendly user guide.<br>
<b>Formats:</b> <a href="http://www.sfu.ca/%7Esblay/R/snow.html">HTML</a><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <a href="http://www.sfu.ca/%7Esblay/R/snow.txt">Text file</a></p>
</li>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p><b>&nbsp;</b></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
</ul>

