---
layout: default
title: Install sampletrees from source
---

<h2>Prerequisites</h2>
<h4>A C++ compiler.</h4>
<ul>
<li>Linux users automatically have access to the GNU C++ compiler, g++.</li>
<li>For Mac users, a C++ compiler is included in the Command Line Tools package. The recommended way to install Command Line Tools is to type the following from a Terminal window:<pre>
xcode-select --install</pre>
If this installation method does not work for you, this <a href="http://stackoverflow.com/questions/9329243/xcode-4-4-and-later-install-command-line-tools">thread on Stackexchange</a> may be helpful for providing a work-around.<br>
</li>
</ul>
<h4>The GNU Scientific Library (GSL).<br>
</h4>
<p>The program is dependent on the <a href="https://www.gnu.org/software/gsl/">gsl (gnu scientific library)</a> being installed. This library is used by other programs, so it may already be installed. Check in /usr/include or usr/local/include for a directory called gsl. This is the most likely place to find gsl. If not already installed, download the latest release from the <a href="https://www.gnu.org/software/gsl/">gsl</a> website and follow the installation instructions in the README and INSTALL files. You will need root access to put the files in /usr/include. If this is not possible, then the directions to install it in a different directory, such as the home directory are given below.<br>
</p>
<ul>
<li>&nbsp;Move the directory that was created by unpacking the tar file. It will be called gsl-X where X is the version number.</li>
<li>&nbsp;At prompt, run configure with the prefix option as shown below. The path specified should be the path where you would like gsl installed, e.g.:<br>
./configure --prefix=/home/kellyb/GSL</li>
<li>&nbsp;At prompts run the following three commands in turn<br>
make<br>
make check<br>
make install</li>
<li>To ensure it has installed, move to the directory you specified in prefix. There should subdirectory named include/. In include/gsl/ there should be a number of .h files.</li>
</ul>
<h2>Compiling sampletrees</h2>
<ul>
<li>Unpack the gzipped tar file (tar xzvf sampletrees_&lt;version&gt;.tar.gz) and change to the sampletrees/src/ directory. In the sampletrees/src directory there should be a makefile.<br>
</li>
<li>Run the makefile from the src/ directory by typing &quot;make&quot; at the prompt. Provided the gsl library can be found there should be no issues compiling the program. The name of the executable is sampletrees.</li>
<li>Note: if you installed gsl somewhere other than /usr/include, you will have to pass the path to gsl to the makefile. Directions for how to pass the path to the makefile are in the comments in the makefile.<br>
<br>
</li>
</ul>
