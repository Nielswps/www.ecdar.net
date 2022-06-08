---
title: "History"
date: 2021-11-18
draft: false
menu: "main"
weight: 82
showpagemeta: false
---

This is a short outline of the history of the development of the different parts of the Ecdar tools.

## Uppaal TIGA versions  - 2010 - 2013
<a href="http://people.cs.aau.dk/~adavid/ecdar/">The first version of the tool (0.6 to 0.10)</a>  was based on the GUI and verification engine of <a href="http://people.cs.aau.dk/~adavid/tiga/">Uppaal TIGA</a>. Efter this it was released as part of Uppaal TIGA in version 0.17.

These versions all had the problem that the GUI was designed for the Uppaal TIGA semantics and thus did not match the Ecdar Timed Input/Output Automata (TIOA) semantics. This version also inherited most of the extension of Timed Automata (TA), including a lot of features that did not have defined semantics in the <a href="http://ulrik.blog.aau.dk/ecdar/">associated papers</a>. Uses the .xml file format.

## PyEcdar - 2013
<a href="https://project.inria.fr/pyecdar/">PyEcdar</a> was a partial implementation of the TIOA semantics implemented by Louis-Marie Traonouez while at INRIA in France. As the name suggests this version was implemented in Python. It was built using the <a href="https://github.com/UPPAALModelChecker/UDBM">Uppaal Difference Bound Matrix (UDBM) library</a>, which is licensed under <a href="https://www.gnu.org/licenses/old-licenses/gpl-2.0.html">GPL 2.0</a>.  Uses the .xml file format.

 	* In 2020 <a href="https://vbn.aau.dk/da/persons/139233">Florian Lorber</a> managed to make the source code compile, but on closer inspection certain important features that we assumed where implemented were not actually implemented in the code base.

## Ecdar GUI - 2017
The <a href="http://ulrik.blog.aau.dk/ecdar/ecdar-gui/">Ecdar GUI</a> is built on the <a href="http://ulrik.blog.aau.dk/h-uppaal/">H-Uppaal</a> GUI that was developed the year before. This GUI is written in JavaFX and is the base for the current version of the <a href="https://github.com/Ecdar/Ecdar-GUI">Ecdar GUI (github)</a>. Uses the .json file format as introduced by H-Uppaal.

This version contained a <a href="http://people.cs.aau.dk/~ulrik/ecdar/StudentReports/Ecdar-VisualSimulator.pdf"> simulator</a> that linked with the old Ecdar TIGA based verification engine. And a <a href="http://eptcs.web.cse.unsw.edu.au/paper.cgi?GandALF18.11">mutation based conformance testing tool</a>.

Simultaneously a tool for <a href="http://ulrik.blog.aau.dk/ecdar/ecdar-gui/">visualizing zones</a> in three dimensions was developed, but not integrated with the other tools.

## j-Ecdar - 2018
Implementation of part of the TIOA theory in Java (<a href="https://projekter.aau.dk/projekter/files/305757029/JECDAR_0.2.pdf">JECDAR 0.2.pdf</a>), also using the <a href="https://github.com/UPPAALModelChecker/UDBM">UDBM library</a>. Can input and output both .json and .xml file formats.

As of the spring of 2021 this code is being worked on to make it feature complete and enable research based on this tool. (<a href="https://github.com/Ecdar/j-Ecdar">j-Ecdar on github</a>)

## Reveaal - 2020
An implementation in Rust of the same features as the j-Ecdar engine. This code base also uses the <a href="https://github.com/UPPAALModelChecker/UDBM">UDBM library</a>. (<a href="https://github.com/Ecdar/Reveaal">Github link</a>) Based on the tool <a href="http://ulrik.blog.aau.dk/hmk/">HMKaal</a> that was also written in Rust, but used a different semantics of the models.

