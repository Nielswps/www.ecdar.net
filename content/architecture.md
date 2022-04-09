---
title: "Architecture"
date: 2021-11-18
draft: false
menu: "main"
weight: 80
showpagemeta: false
---

This page describes the intended Ecdar tool architecture as of spring 2021.

<a href="http://ulrik.blog.aau.dk/ecdar/ecdar-history/">The history of the tools can be seen here.</a>

<a href="../ArchOverview.png"><img class="alignnone wp-image-448" src="../ArchOverview.png" alt="" width="496" height="357" /></a>

The general design intent of having two verification engines, is that it should make the whole platform more reliable.
<h2><a href="https://github.com/Ecdar/j-Ecdar">j-Ecdar</a></h2>
The intention of j-Ecdar is to be a form of reference implementation, where no effort is put into optimizing the code for speed, but rather for
<ul>
 	<li>Correctness</li>
 	<li>Readability</li>
</ul>
<h2><a href="https://github.com/Ecdar/Reveaal">Reveaal</a></h2>
The intention of the Reveaal engine is to get a verification engine that is fast and parallelizable. Both over multiple cores, but also in the long run over multiple machines. The design goals for Reveaal is
<ul>
 	<li>Correctness</li>
 	<li>Speed</li>
 	<li>Remove dependency to UDBM</li>
</ul>
<h2><a href="https://github.com/Ecdar/Ecdar-GUI">Ecdar GUI</a></h2>
The intention of the GUI is be quick and usable to create and edit models. It should provide visual feedback on the verification.
<ul>
 	<li><a href="https://github.com/Ecdar/VisualZone">Visualization of zones</a></li>
 	<li>Visualization of refinement relations</li>
 	<li>Integration with revision control (Git)</li>
</ul>
<h2><a href="https://github.com/Ecdar/Ecdar-test">Test framework</a></h2>
Automated test of the two engines. This component is vital in order allow to obtain the ability to actually refactor code in the engines with confidence.
<ul>
 	<li>Hand designed test cases with known results</li>
 	<li>Conformance testing between the two engines</li>
 	<li>Automated performance testing</li>
</ul>
&nbsp;
