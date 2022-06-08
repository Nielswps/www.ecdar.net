---
title: "Architecture"
date: 2022-04-09
draft: false
menu: "main"
weight: 80
showpagemeta: false
---

This page describes the Ecdar tool architecture as of spring 2022.

![Overview of the Architecture](/img/ArchOverview.png "Overview of the Architecture")

The general design intent of having two verification engines, is that it should make the whole platform more reliable.

## [j-Ecdar](https://github.com/Ecdar/j-Ecdar)

The intention of j-Ecdar is to be a form of reference implementation, where no effort is put into optimizing the code for speed, but rather for

 *	Correctness
 * Readability

## [Reveaal](https://github.com/Ecdar/Reveaal)

The intention of the Reveaal engine is to get a verification engine that is fast and parallelizable. Both over multiple cores, but also in the long run over multiple machines. The design goals for Reveaal are

 * Correctness
 * Speed
 * Remove dependency to UDBM

## [Ecdar GUI](https://github.com/Ecdar/Ecdar-GUI)

The intention of the GUI is be quick and usable to create and edit models. It should provide visual feedback on the verification.

 *	[Visualization of zones](https://github.com/Ecdar/VisualZone)
 *	Visualization of refinement relations
 *	Integration with revision control (Git)
 
## [Test framework](https://github.com/Ecdar/Ecdar-test)

Automated test of the two engines. This component is vital in order allow to obtain the ability to actually refactor code in the engines with confidence.

 *	Hand designed test cases with known results
 * Conformance testing between the two engines
 *	Automated performance testing


