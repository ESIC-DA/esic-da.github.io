---
layout: post
title: Reducing Attack Surface
date: 2019-10-23 00:00
description: Case study of how to use AHA-Project to decrease vulnerable attack surface.
toc: true
tags: AHA-GUI CaseStudy
---

This document is a simple example and/or case study of how to use AHA-GUI to aid in reducing attack surface of a scanned host.

[![Comparison-Img](https://aha-project.github.io/images/CaseStudy1/Comparison.png)](https://aha-project.github.io/images/CaseStudy1/Comparison.png)

Understanding attack surface is a key in reducing system complexity and exploitability. In combination with standard attack surface reduction techniques, AHA-Project tools can help identify, understand, and reduce attack surface.

[![Pre-Scan](https://aha-project.github.io/images/CaseStudy1/PreScan.png)](https://aha-project.github.io/images/CaseStudy1/PreScan.png)

This image above shows a VM prior to any common attack surface reduction practices being employed. We can see there are many processes on the machine, lots of system processes, and several application processes.

Two hardening techniques will be applied here:
 - One Application per VM
     - The suite of applications being studied allows for them to be easily split between VMs. In this case, some of the companion applications should be moved to other VMs, to reduce attack surface and provide isolation between the different application functions should it be compromised.
 - Removal / reduction of superfluous operating system processes
     - Uninstall/Removal of svchost based services that are not needed
     - Removal of the print spooler

[![Post-Scan](https://aha-project.github.io/images/CaseStudy1/PostScan.png)](https://aha-project.github.io/images/CaseStudy1/PostScan.png)

After applying the stated methods, we can re-scan using AHA-Scraper and view in AHA-GUI to see that the number of processes has been dramatically reduced.

