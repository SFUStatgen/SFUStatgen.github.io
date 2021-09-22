---
layout: default
title: luca
---

<p>In genetic association studies, there is increasing interest in understanding the joint effects of genetic and nongenetic factors. For rare diseases, the case-control study is the standard design and logistic regression is the standard method of inference. However, the power to detect statistical interaction is a concern, even with relatively large samples. LUCA implements maximum likelihood inference under</p>
<ol>
<li>independence of the genetic factor and nongenetic attributes in the control population,</li>
<li>independence of the genetic factor and nongenetic attributes, plus Hardy-Weinberg proportions (HWP) in control genotype frequencies, or</li>
<li>simple dependence between the genetic and nongenetic covariates in the control population.</li>
</ol>
<p>Maximum likelihood under covariate assumptions offers improved precision of interaction estimators compared to the standard logistic regression approach which makes no assumptions on the distribution of covariates.</p>
<p>The luca R package is available on the Comprehensive R Archive Network <a href="http://cran.stat.sfu.ca">website</a> under &quot;contributed packages&quot;. You will have to have <a href="http://www.r-project.org">R</a> installed on your system to use it. To install luca you can execute the following command in R:</p>
<p>install.packages(&quot;luca&quot;)</p>
<p>Windows users can also install the package via the &quot;Packages&quot; menu item.</p>
<p>The software is licenced under the <a href="http://www.gnu.org">GNU</a> <a href="http://localhost:8080/statgen/research/luca/gpl.txt">General Public Licence</a>.</p>
