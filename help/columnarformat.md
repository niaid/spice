---
layout: help
title: Columnar SPD Format
---

Create a text file (using Word or Excel) that conforms to the following formatting rules. Note that you can insert comments in the file by starting any line with an asterisk ("*"); these lines are completely ignored irrespective of where they occur. The references to line numbers below are taken to indicate the line number ignoring any comments. Thus, "Line 1" means the first line of the file that does not contain a comment line.

    Line 1: The number of different variables in the data set ( = n)  
    Lines 2 through n+1: Variable definitions  
    Lines n+2 to end: Variable values and data value

A variable definition line contains the name of the variable (this can be any length, but should be kept short for legibility), followed by a list of possible values that this variable can take. This list must be tab-delimited. You do not have to specify all possible values; you can specify no values if you wish. The program will examine your data to determine what all possible values for each variable will be. The advantage to specifying values on this line is to control the order in which the values are displayed in the bar charts: they are listed in the same order as they are found on this line. The subset specification lines have n+1 columns separated by a tab; the first n columns are the exact specification of the subset, with the values for each phenotype. The last column has the display value.

<table border="1" align="center" cellspacing="0" cellpadding="3">
	<caption>Fig. A: Sample File Content</caption>
	<tr>
		<td colspan="5" align="left">* Sample data set</td>
	</tr>
	<tr>
		<td colspan="5" align="left">3</td>
	</tr>
	<tr>
		<td width="20%" align="center">Stimulation</td>
		<td width="20%" align="center">Env</td>
		<td width="20%" align="center">Gag</td>
		<td width="20%" align="center">Pol</td>
		<td width="20%" align="center">Nef</td>
	</tr>
	<tr>
		<td width="20%" align="center">CD107</td>
		<td width="20%" align="center">-</td>
		<td width="60%" align="center" colspan="3">+</td>
	</tr>
	<tr>
		<td width="20%" align="center">IFNg</td>
		<td width="20%" align="center">-</td>
		<td width="60%" align="center" colspan="3">+</td>
	</tr>
	<tr>
		<td colspan="5" align="left">* Data values follow</td>
	</tr>
	<tr>
		<td width="20%" align="center">Env</td>
		<td width="20%" align="center">+</td>
		<td width="20%" align="center">+</td>
		<td width="40%" align="center" colspan="2">0.2</td>
	</tr>
	<tr>
		<td width="20%" align="center">Env</td>
		<td width="20%" align="center">+</td>
		<td width="20%" align="center">-</td>
		<td width="40%" align="center" colspan="2">0.5</td>
	</tr>
	<tr>
		<td width="20%" align="center">Tat</td>
		<td width="20%" align="center">-</td>
		<td width="20%" align="center">+</td>
		<td width="40%" align="center" colspan="2">0.0017</td>
	</tr>
</table>

As an example, consider the data formatted as shown in *Figure A*. This data file begins with a comment that will be displayed in the Inspector Panel. The next line specifies that there are three variables recorded in the data set. These variables, found on the subsequent three lines, are named "Stimulation", "CD107", and "IFNg". The "stimulation" variable has 4 values specified; in bar charts, "Env" will be shown to the left of "Gag", "Pol", "Nef", and any other values in the data. CD107 and IFNg can take on two different values each, "+" or "-". You could choose "&middot;" and "&nbsp;" (space) if you wish; this makes for an attractive legend.

The first display value is for Stimulation: Env, CD107: +, and IFNg: +, and has a value of 0.2. There are two additional display values in this (trivial) data set.