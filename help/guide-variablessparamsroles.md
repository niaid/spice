---
layout: help
title: User Guide (Variables / Parameters / Roles)
---

## Variables / Parameters / Roles

### Variables & Parameters

Data loaded into SPICE is comprised of data values (or measurements), all of which have the same units. For example, you might create a data file of immune responses, measured as the percentage of a subset that expresses one or more cytokines. Or a data file could contain viral loads, measured on different individuals enrolled in different treatment trials in a longitudinal study. The data values must be a continuous measurement (i.e., real or integer numbers).

Each data value is described by one or more variables. Each variable is of a nominal type (in other words, it takes on a limited set of discrete parameters, typically, `Yes` or `No`; `High`, `Medium`, or `Low`; `+` or `-`; etc.). The parameters of these variables describe the data value with which they are associated; you will group together and discriminate among variable parameters in order to analyze the data. For example, you may use one variable that identifies all of the data values that should be averaged together to generate a summary report; another variable might identify how to discriminate values that are to be compared against each other.

### Roles

Variable roles form an important part of a query group's query structure as they dictate how your data set is transformed and computed into the desired "view". In SPICE 6, variables can take on one of five different roles: Category, Overlay, Average, Sum or Group. Each role is described below. To learn how to change a variable's role, see the [Managing Query Groups](guide-managingquerygroups) section of this guide.

#### Category Role

Categorical variables identify how to generate the categories of values over which to generate bar charts and pie charts. SPICE will generate categories for every possible combination of all categorical variables (variables with a role of Category). By default, all variables in a query group's query structure are categorical.

If you have three Category variables, each of which can have three values, then you will have up to 27 (33) categories ("empty" categories - categories for which there are no corresponding values - are not displayed). For example, a bar figure will have one set of bars for each category and a pie figure will have one slice for each category. When SPICE needs to normalize data to show a fraction of the total (for example, for pies or for bars that are not shown with absolute scaling), then the normalization value (total) is the sum of all of the computed values for all categories.

#### Overlay

Overlaid variables also subdivide data to allow you to compare distributions directly. In effect, this produces one data set for each parameter in the overlay variable (though overlaying two variables, each with two parameters would produce a total of four data sets). SPICE will generate one pie chart and one set of bars (in the bar chart), for every possible combination of all Overlay variable values.

For example, in a data set with a variable `Patient` with parameters `A`, `B`, and `C`, choosing to overlay by `Patient` will produce three pies and three sets of bars, one for each patient (`A`, `B`, and `C`).

#### Sum & Average Roles

Summed and averaged variables are those which reduce the data set. Both create computed values that are the average or sum of all of the data values which fit the specified category and overlay criteria. A full discussion on when to average and when to sum is found in [Data Analysis](analysis-summingandaveragingversusgrouping).

#### Group Role

Grouped variables, like summed and averaged variables, reduce the data set. The distinction, however, is that the values are not summed or averaged into a single computed value but rather a vector of the multiple values (or data points) are preserved. This allows for a variety of formatting options for bar and coolplot figures.

For example, if a variable `Patient` has the parameters `A` and `B`, all the values for patients `A` and `B` are combined. In a bar figure, the values will be displayed as multiple data points within each category.

*****

[Return to Guide Index](guide) | [Previous](guide-querystructurecontrols) | [Next](guide-managingfigures)
