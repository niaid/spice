---
layout: help
title: Analysis (Summing &amp; Averaging vs. Grouping)
---

## Summing &amp; Averaging vs. Grouping

SPICE has three roles for variables, "Sum", "Average", and "Group". In general, you will only use the "Sum" or "Average" role when you want to collapse some of the complexity in your data set, otherwise use the "Group" role.

When you assign a variable to have a "Sum" or "Average" role, then all data that come from different values of the summed or averaged variable (but have identical values for the categorical variables) will be summed or averaged together prior to being used by SPICE in any calculations or displays. Use this role when you have split your data into more categories than you want to display. For example, if you have divided responses into multiple functions, gIFN and IL2 as in other examples here, and you only wish to do an analysis on the gIFN response, then you should "Sum" the IL2 variable. This would be the same as if you had only collected the data for gIFN: i.e., the IL2+, gIFN- values would have been included in the gIFN- values; the IL2+gIFN+ values would have been included in the gIFN+ values.

Consider another example. In general, if you are analyzing an experiment in which you have three cohorts of subjects, with different numbers of subjects in each cohort, then you should assign a "Group" role to the "Subject" variable when you compare the cohorts. This will instruct SPICE to show you the mean response for a subject in each of the cohorts. If you were to choose "Sum", then each cohort would have the total response, summed over all of the patients ("Average" role would average over all the patients). But, this sum will depend on the number of patients as well as the responses of the patients, and therefore may not be a meaningful value to compare.

*****

[Return To Analysis Index](analysis) | [Previous](analysis-addingvariables) | [Next](analysis-relativeversusabsolutescaling)
