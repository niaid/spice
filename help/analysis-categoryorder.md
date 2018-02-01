---
layout: help
title: Analysis (Category Order)
---

## Category Order

By default, each time a query is re-computed, SPICE will organize and draw the resulting categories in the "permuted order" defined by the order of the variables in the Query Structure, as well as the order of the parameters for each variable. In this case, "permuted order" means the order they would appear after permuting the parameters of all categorical variables, in the order they appear in the list.

The category order directly affects the order in which the slices of a Pie are drawn, the order of the bars in the bar chart, etc. The pie slices are drawn from the top ("12 o'clock position") in a clockwise direction; the bars are drawn left-to-right.

Re-ordering of categories (and variable values) is not a trivial operation. It can help you explore the data by sorting sets of categories together; this helps identify patterns of subsets in your data. You should routinely re-order the variable list in order to see if there are any major patterns that fall out of the data set (for example, with all of the biggest bars grouping together under certain sorting conditions).

### Specifying Category Order

You can reorder the result categories by either of the two methods below.

#### The Query Structure

You can directly specify the natural order of the categories (the order in which the variables' parameters are permuted to form the categories) by directly reordering them in the Query Structure list by drag and drop. Specifying the preferred natural order for the view is the easiest way to ensure any subsequent changes resulting in re-computation of your view will order the categories in a way that is meaningful to you.

#### The Category Sort Commands

You can also change the bar order by selecting the query group in the outline, then changing the *sort results by* control at the bottom of the Query Structure panel. The options are *permuted* (as defined by The Query Structure above) or *weighted*. The *weighted* option changes the order so that the categories are sorted by an algorithm that essentially sums the variable values. Thus, in the simple case where all variables have two values (e.g., "+" and "-"), the categories are sorted such that the category with all "+" is first, followed by those with all but one "+", etc.

>Note: Re-ordering categories does not affect the calculations of statistics for either the bar chart or the pie charts.

*****

[Return To Analysis Index](analysis) | [Previous](analysis) | [Next](analysis-thresholding)
