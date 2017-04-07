---
layout: help
title: Overview
---

## Introduction

SPICE (Simplified Presentation of Incredibly Complex Evaluations) can help you navigate through complex datasets, revealing potential correlations between sets of values measured on individual samples and other aspects of those samples (for example, treatment, cohort, etc.). SPICE was written to analyze data from multifunctional flow cytometry experiments where different kinds of cells are stimulated under different conditions and multiple different measurements are made on each cell. However, SPICE can be used for any kind of multivariate dataset for which you have a series of nominal or ordinal measurements and a single continuous measurement.

Put another way, SPICE is a data mining and visualization application, a tool with which to explore your data. SPICE is meant to convey qualitative information and to reveal patterns. It enables you to explore and compare different views (different orders of variables; different chart presentations; different roles for different variables). It may even reveal a new way of thinking about your existing data.

Finally, SPICE is complex. This means there is a learning curve associated with understanding how to use it. Nonetheless it can do things no other program can do and can significantly speed the presentation of data.

## Conceptual Model

In the following subsections, we'll step through the SPICE 6 conceptual model. This will give you working knowledge of how the application is organized and will define some terminology you'll need to be familiar with.

### Query Group

A Query Group is a "container" in which you specify your view into your data and in which the associated Figures (charts, tables, etc.) are stored. All figures belonging to a Query Group share the results of the same query (and changing that query affects all Figures in the Query Group). Every analysis in SPICE begins with creating a Query Group and adding at least one Figure. Its query is specified by assigning roles and sort order to the Variables (and inclusion and sort order) to the Parameters of each Variable.

### Figure

A Figure is a chart or a table associated with a Query Group. One or more Figures are the ultimate output of SPICE. Figures are exported as print-quality vector graphics (PDF by default) that can be further manipulated in the vector graphics program of your choice, or directly imported into your desktop publishing software (such as Word, PowerPoint, Pages, Keynote, etc.) for publication. Each Figure can have its own unique Style (its individual range and display options) or "share" a Style in common with other figures of its kind.

### Style

A Style is the collection of range and display settings available to a given kind of Figure. A Style can be unique to its Figure or promoted to a "Shared Style", which makes it available to any Figure of the same type (that is, a Pie Figure can use a Shared Style for Pie Figures). When a Shared Style is modified, the change is instantly applied to all Figures that use it.

### Canvas

A Canvas is a container that behaves like an "art board" for laying out multiple Figures any way you wish. The figures can be from any Query Group in the document. As an example, this is useful for creating a single graphic containing a Bar Figure from two different Query Groups for comparison. When a Canvas is exported, it is (like a Figure) a print-quality vector graphic that can be edited in any vector graphics program or imported directly into desktop publishing software for publication.

## Workflow

The input, as mentioned above, is a series of continuous categorical measurements imported into SPICE. Currently, SPICE can import either a specialized text file for importing data or delimited data files (such as .csv, .tab/.tsv, etc.). The formats are explained in detail in the [Data File Format](dataformat) section. Future versions will provide more import options. Alternatively, you can create a new SPICE document and edit its source data directly. For bulk data, however, it's easiest to create a delimited data file and import it into a SPICE document.

Most of your time will be spent manipulating your data set to create Query Groups and Figures. This is done by arranging and assigning roles to Variables, and ignoring or showing Parameters, and changing their order. Changes to your data set require the Query Group to be recomputed, which can take time depending on the complexity of your data. The rest is spent formatting the resulting Figures to suit your needs, or composing them into one or more Canvases for higher-level organization of exported graphics.

The output of SPICE are the various Figures and Canvases (as well as the result data as tab-separated text if desired). The Bar and Pie Figures are both useful graphical outputs for conveying information about data. The NPlot Figures are useful for identifying outliers. The Pie Figures in particular are easily understood and can convey pattern information quickly. The Bar Figures can show individual data points as well as ranges (with error bars and more). There are few statistics available in SPICE; it is primarily designed to create graphic representations of data for exploration as well as illustration in presentation, publication, etc.

### Legacy Support

Users of previous versions can open existing `.spd` and `.spicedoc` / `.spicedocument` files in the current version (they will be saved into a new, upgraded file when opened).
