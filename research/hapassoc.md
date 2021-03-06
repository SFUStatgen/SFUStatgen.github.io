---
layout: default
title: hapassoc
---

## hapassoc

<p><b>The hapassoc R package implementing likelihood inference of trait associations with SNP haplotypes and other attributes using the EM Algorithm.</b></p>
<p>The identification of genetic factors influencing susceptibility to complex disorders such as diabetes and cancer is important for improving understanding of disease pathways and for disease prevention. Associations between complex traits and single nucleotide polymorphisms (SNPs) in candidate genomic regions can provide a useful tool for such identification. However, analysis of trait associations with single SNPs ignores the potential for extra information from joint consideration of multiple SNPs on a haplotype. When haplotype phase can be resolved, regression models may be used to adjust associations between complex traits and haplotypes for the effects of nongenetic cofactors or attributes, and to investigate whether nongenetic cofactors modify haplotype associations. However, resolution of haplotype phase can be problematic, particularly when data are collected on unrelated subjects. We develop a likelihood approach to inference of haplotype and nongenetic effects and their interactions in generalized linear models of disease penetrance, when haplotype phase is unknown for some subjects. The likelihood is formulated assuming population Hardy-Weinberg equilibrium and independence of haplotype and nongenetic covariates. Parameter estimates are obtained by use of an expectation-maximization (EM) algorithm and standard errors are calculated using Louis' formula.</p>
<p>The hapassoc R package is <a href="http://cran.r-project.org/package=hapassoc">available</a> on the Comprehensive R Archive Network <a href="http://cran.r-project.org">website</a>. See the package <a href="https://cran.r-project.org/web/packages/hapassoc/vignettes/hapassoc.pdf">vignette</a> for a description of the underlying statistical methods and illustration of the use of hapassoc through examples.</p>
<p>You will have to have <a href="http://www.r-project.org">R</a> installed on your system to use it. To install hapassoc you can execute the following command in R:</p>
<p>install.packages(&quot;hapassoc&quot;)</p>
<p>Windows users can also install the package via the &quot;Packages&quot; menu item. hapassoc is part of the <a href="https://cran.r-project.org/view=Genetics">statistical genetics task view</a>, so if you have this task view installed, you already have hapassoc installed.</p>
<p>The software is licenced under the <a href="http://www.gnu.org">GNU</a> <a href="http://www.gnu.org/licenses/gpl.html">General Public Licence</a>.</p>
<p>For more details on the implementation, please see our <a href="https://cran.r-project.org/web/packages/hapassoc/vignettes/hapassoc.pdf">vignette</a>, or the earlier <a href="http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&amp;db=pubmed&amp;dopt=Abstract&amp;list_uids=15583426">paper</a> in Human Heredity.</p>

