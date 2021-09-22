---
layout: default
title: sampletrees
---
<p>A Markov chain Monte Carlo algorithm for sampling gene genealogies conditional on either phased or unphased SNP genotype data. The algorithm has been implemented in C++ by Kelly Burkett. For details, see <a href="https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/ws-procs_PostReview.pdf">Burkett <i>et al.</i> (2013a)</a> and <a href="https://www.degruyter.com/view/j/sagmb.2013.12.issue-5/sagmb-2012-0011/sagmb-2012-0011.xml">Burkett <i>et al.</i> (2013b)</a>. For an application to genetic association mapping, see <a href="http://www.frontiersin.org/Journal/10.3389/fgene.2013.00260/abstract">Burkett <i>et al</i>. (2013c)</a>.<br>
</p>
<p>In addition to the sampletrees C++ program, the <a href="http://www.r-project.org">R</a> package <a href="http://cran.r-project.org/web/packages/Rsampletrees/index.html">Rsampletrees</a> is available to assist users with (i) creating the input files needed by sampletrees, and (ii) processing and plotting the results of a sampletrees run. Most users of sampletrees will also want Rsampletrees.</p>
<p>The C++ program and R interface are described in <a href="https://academic.oup.com/bioinformatics/article/32/10/1580/1742656">Burkett <i>et al.</i> (2016)</a>.<br>
</p>
<h3>Installing sampletrees<br>
</h3>
<p>For the C++ program, Mac and Linux users need to install from source, but Windows users can download pre-compiled versions.</p>
<ul>
<li>From source: Download the C++ source code and documentation as a <a href="https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/sampletrees_2015-11-27.tar.gz">gzipped tar file</a> and follow the <a href="research/sampletrees/installfromsource.html">instructions for installing from source</a>.&nbsp;</li>
<li>Compiled versions for Windows: Download compiled versions for <a href="https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/sampletrees32.exe">32 bit Windows</a> or for <a href="https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/sampletrees64.exe">64 bit Windows</a>. (Note: Before using one of these pre-compiled versions you may wish to change its name from sampletreesXX.exe, where XX is 32 or 64, to sampletrees.exe to match the documentation.)<br>
</li>
</ul>
<h3>Installing Rsampletrees</h3>
<p><a href="http://cran.r-project.org/web/packages/Rsampletrees/index.html">Rsampletrees</a> is now available on CRAN. Install from within R using</p>
<pre>
install.packages(&quot;Rsampletrees&quot;)
</pre>
<h3>Documentation for sampletrees<br>
</h3>
<p>Documentation for the C++ program is available in the <a href="https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/sampletrees_Rsampletrees_documentation.pdf">combined sampletrees/Rsampletrees documentation.</a> Please be aware that the software is under active development, with improvements to the user interface in progress. As a result, the documentation may be out of date in some places.</p>
<h3>Documentation for Rsampletrees</h3>
<p>See the <a href="https://www.sfu.ca/content/dam/sfu/stat/documents/Statgen/sampletrees_Rsampletrees_documentation.pdf">combined sampletrees/Rsampletrees documentation.</a> In addition, the help pages for all functions in the package (also known as the reference manual) is available <a href="http://cran.r-project.org/web/packages/Rsampletrees/Rsampletrees.pdf">here</a>. A package vignette is currently under development.</p>
