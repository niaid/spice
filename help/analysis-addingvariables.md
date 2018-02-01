---
layout: help
title: Analysis (Adding Variables)
---

## Adding Variables

There are two reasons that you may wish to add additional variables to your data set. First, you may have replicate values that are not uniquely identified by the existing variables; and second, you may wish to explore other ways in which your data sorts out.

If your data set has data values with exactly the same combination of variable values assigned to them, SPICE will only select one of those for use. SPICE can only group or display multiple values based on variables assigned to a "Group" role. If you do an experiment where you have three animals per group, and want to use the average for each group in the SPICE analysis, you could average the data using Excel and then input that. However, it would be far better to add a new variable to the data, for example, "Animal ID". Once you launch SPICE, you can then assign this variable to be a "Group" variable. The advantage of this is that you can then use SPICE to see the variability in the data (showing, for example, error bars in the bar chart). In addition, you may find, after exploring your data, that one of the animals has anomalous results. Using SPICE, you can easily exclude a single animal (using the "Ignore" option next to the animal in the Variables & Parameters list) from all calculations.

You might also want to explore the role of other parameters on your data set. For example, in a clinical data set, you may have grouped subjects by cohort. But you might want to explore how the data is related to other demographic parameters, such as sex, age, clinical status, etc. Consider creating additional variables for each of these parameters, and adding them to the dataset.

>Note: For continuous measurements like age, you might want to create an age variable that has only a couple of values, such as "young", "old", and "senile" so that you can group subjects appropriately.

One way to accomplish this is with an application called [Pestle](http://drmr.com/pestle.zip) maintained privately by Dr. Mario Roederer. Pestle can be used to format tabular data (as output by [FlowJo's](https://www.flowjo.com) Table Editor, for example) into SPICE-ready data, as well as to merge in additional descriptive data as mentioned above. Please see the Pestle documentation for more information and please direct all support requests to Dr. Roederer; SPICE support cannot answer Pestle questions.

When you launch SPICE with datasets containing these additional variables, you will likely need to assign a "Group" role to these additional variables (when you are not analyzing by those variables). That way, SPICE does not try to show all possible categories of variable values (particularly useful when some combinations of variable values don't exist in the data set).

*****

[Return To Analysis Index](analysis) | [Previous](analysis-thresholding) | [Next](analysis-summingandaveragingversusgrouping)
