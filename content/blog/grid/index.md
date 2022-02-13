---
title: Developing for GridPP - grid-analysis
date: 2017-03-24
---

Since getting access to the UK Grid, I've been starting to write some of my own software to run on it. Initially, I have been working on a simple analysis system, using lucid-utils for actual analysis, to run through a folder of XYC frames and output a CSV file that is similar to that of what TAPAS (https://starserver.thelangton.org.uk/tapas) produces - but designed for a much larger scale. 

The system uses Ganga to easily submit jobs to the GridPP DIRAC instance, requiring you to only enter a ZIP path and a couple of other options. 
You can even submit a job with a 'one-liner' really easily! The analysis software is avaliable on CVMFS at the following path: /cvmfs/researchinschools.egi.eu/software/grid-analysis
It can also be found on Github: https://github.com/willfurnell/grid-analysis