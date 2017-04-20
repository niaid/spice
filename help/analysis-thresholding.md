---
layout: help
title: Analysis (Thresholding)
---

## Thresholding

Negative values in datasets are common, even when the data is representational (i.e., fraction of a total). This is because we deal with imprecise measurements, and if the measurements need to be corrected (background subtraction), then normal errors in the measurement can lead some values to be measured at a value below the background - leading to negative corrected values. It is not reasonable to try to analyze the unsubtracted data, because those values are systematically biased by the background.

Generating meaningful pie charts is impossible when there are negative values in the data. The only option to handle the presence of negative values is to set these data values to zero before doing the calculations. However, this presents a similar problem to analyzing the data without background subtraction: there is a systematic bias introduced by zeroing only negative values. In other words, the total response (sum of all of the values) is increased by this operation, since you are only adding to data values (increasing negative values to zero) without subtracting from any others.

In addition, there will be small positive values that are also essentially background (and should be zero). The same error distribution leading to negative values will lead, as often, to values above zero for responses that are nonexistent. For example, if the average background measurement for a value is 5, then the measurements for nonresponsive tests will be centered around 5; sometimes, they will be 3 or 4, sometimes, 6 or 7. Thus, the distribution for nonresponding elements will range (after background subtraction) from -2 to +2.

A reasonable approach to analyzing such data is to set all values below some small positive amount to be zero. Thus, in this example, you might choose to set all values below 2 to be zero. This has two significant benefits to the analysis: first, it removes the systematic bias introduced by zeroing negative values: by reducing as many values (from small positive to zero) as increasing (from negative to zero), the total and mean response is unchanged in the data. Second, this process removes error introduced by including the small positive values in the representational analysis. Indeed, this can significantly clean up your analysis.

SPICE provides a set of controls at the bottom of the Query Structure panel where you can enable thresholding and specify the threshold below which values are set to zero. By default this is 0, but you should explore changing this value. If your data has many values that are close to background (noise), then this value becomes critical and can significantly affect your analysis.

How do you best determine what value to use here? That is a very difficult process to do rigorously. One approach would be to generate a histogram of all of your data values. Look at the extent of the distribution into negative values: it is reasonable to expect that the "noise" distribution is symmetric around zero, so you can choose a positive value that corresponds to the other side of this negative distribution.

To continue evaluating the appropriate threshold, you can also display the bar and pie charts for a threshold of zero. Now increase this threshold to small positive values, and observe how that affects the pie charts. As you step up above the noise level, you may see the pie charts adjust (if you don't, then your data is far above the noise level and you don't need to worry about this). Keep increasing the threshold until there is no significant change; this is a reasonable estimate of where you have eliminated the noise contribution. 

> Note: if you set the threshold so high as to eliminate true positive responses, you will start to significantly affect the distributions again.

[Return To Analysis Index](analysis)
