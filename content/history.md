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
[The first version of the tool (0.6 to 0.10)](http://people.cs.aau.dk/~adavid/ecdar/) was based on the GUI and verification engine of [Uppaal TIGA](http://people.cs.aau.dk/~adavid/tiga/). Efter this it was released as part of Uppaal TIGA in version 0.17.

These versions all had the problem that the GUI was designed for the Uppaal TIGA semantics and thus did not match the Ecdar Timed Input/Output Automata (TIOA) semantics. This version also inherited most of the extension of Timed Automata (TA), including a lot of features that did not have defined semantics in the [associated papers](http://ulrik.blog.aau.dk/ecdar/). Uses the .xml file format.

## PyEcdar - 2013
[PyEcdar](https://project.inria.fr/pyecdar/) was a partial implementation of the TIOA semantics implemented by Louis-Marie Traonouez while at INRIA in France. As the name suggests this version was implemented in Python. It was built using the [Uppaal Difference Bound Matrix (UDBM) library](https://github.com/UPPAALModelChecker/UDBM), which is licensed under [GPL 2.0](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html).  Uses the .xml file format.

 * In 2020 [Florian Lorber](https://vbn.aau.dk/da/persons/139233) managed to make the source code compile, but on closer inspection certain important features that we assumed where implemented were not actually implemented in the code base.

## Ecdar GUI - 2017
The [Ecdar GUI](http://ulrik.blog.aau.dk/ecdar/ecdar-gui/) is built on the [H-Uppaal](http://ulrik.blog.aau.dk/h-uppaal/) GUI that was developed the year before. This GUI is written in JavaFX and is the base for the current version of the [Ecdar GUI (github)](https://github.com/Ecdar/Ecdar-GUI"). Uses the .json file format as introduced by H-Uppaal.

This version contained a <a href="http://people.cs.aau.dk/~ulrik/ecdar/StudentReports/Ecdar-VisualSimulator.pdf"> simulator</a> that linked with the old Ecdar TIGA based verification engine. And a <a href="http://eptcs.web.cse.unsw.edu.au/paper.cgi?GandALF18.11">mutation based conformance testing tool</a>.

Simultaneously a tool for [visualizing zones](http://ulrik.blog.aau.dk/ecdar/ecdar-gui/) in three dimensions was developed, but not integrated with the other tools.

## J-Ecdar - 2018

Implementation of part of the TIOA theory in Java ([JECDAR 0.2.pdf](https://projekter.aau.dk/projekter/files/305757029/JECDAR_0.2.pdf)), also using the [UDBM library](https://github.com/UPPAALModelChecker/UDBM). Can input and output both .json and .xml file formats.

As of the spring of 2021 this code is being worked on to make it feature complete and enable research based on this tool. ([j-Ecdar on github](https://github.com/Ecdar/j-Ecdar))

## Reveaal - 2020

An implementation in Rust of the same features as the j-Ecdar engine. This code base also uses the [UDBM library](https://github.com/UPPAALModelChecker/UDBM). Based on the tool [HMKaal](http://ulrik.blog.aau.dk/hmk/) that was also written in Rust, but used a different semantics of the models.

