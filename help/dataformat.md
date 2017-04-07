---
layout: help
title: Data Format
---

## Introduction

Before formatting data for entry into SPICE, you need to be familiar with what kind of data SPICE is expecting. All numerical values on which SPICE will do calculations or graphical display must have the same units. For example, all data values must be a percent (e.g., percent of a subset of cells), or an absolute count, or any given measurement. However, you cannot mix different kinds of measurements: for example, a single SPICE data file should not be used to simultaneously analyze viral loads and subset percentages. Rather, these data types should be entered into different data files.

### Basic Delimited Files

Files can be created most easily in Microsoft Excel, or in Word. In either case, make sure to save the file in "tab-delimited" format: Choose "Save As ...", and select "Tab-Delimited". Make sure the extension for tab-delimited files is `.tab` and for comma-separated value files, use, `.csv`.

The specifics of the delimited file format are discussed in the [Delimited (CSV/TAB) Format](delimitedformat) section.

### "Old SPICE" (SPD) Formats

SPICE relied on another program, *Pestle*, to format data automatically from FlowJo Table Editor outputs for input into SPICE (creating a file with a `.spd` extension). This program also automates other data manipulations like background subtraction, database merging, and multiplying certain values together. For more information, see the documentation for Pestle. These formats are no longer necessary, however, and users are encouraged to use a basic delimited file format as mentioned above.

The specifics of the SPD formats created by Pestle are detailed in the [Columnar SPD Format](columnarformat) and [Matrix SPD Format](matrixformat) sections.

    Note: If you can use Pestle for your data manipulation, then you do not need to read this section in great detail. However, it will be useful to read it and understand the format of the data in case you wish to make minor modifications or understand why there may be problems if the displays do not look like what you want!

***

The three primary data file formats are discussed in depth in the remaining sections of the Data Format guide.