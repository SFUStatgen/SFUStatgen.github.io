---
layout: default
title: GNU C and C++
---

# Access to the GNU C and C++ compilers

How you access the GNU C and C++ compilers depends on your operating system. 

<h3>Linux</h3>
<ul>
<li>GNU tools come with any Linux distribution (Linux itself is GNU) and are available on the Department Linux servers such as rcga-linux-ts1.dc.sfu.ca.
</li>
</ul>
<h3>Windows</h3>
<p>Windows users will have to install the tools themselves. Two options are <a href="https://sourceforge.net/projects/mingw/">MinGW</a> and <a href="https://www.cygwin.com/">cygwin.</a><br>
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
