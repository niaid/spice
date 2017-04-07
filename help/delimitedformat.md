---
layout: help
title: Delimited Data Format
---

## Introduction

The "tab-delimited" and "comma-separated value" file formats are the most common plain text formats used to share data between different applications. There are a number of applications for the Mac (such as Excel, Numbers, and XTabulator), which can be used to manipulate tabular data files, saving them as `.tab` or `.csv` files automatically. Some of these tools allow you to specify any separator, character encoding, line ending type, and file extension, which can be useful for manipulating and massaging the data into the format you need for analysis. Of course you can create a simple tab-delimited or comma-separated file with a plain text editor like the built-in TextEdit application that ships with OS X.

The only caveat to using this loose format is that you must take care to follow [the generally-accepted rules](http://en.wikipedia.org/wiki/Comma-separated_values) (regarding "enquoting" your delimiter character if it's used in a field, making sure all rows have the same number of fields, etc.).

## Delimited Files for SPICE

### Overview

This format, which can be created by any spreadsheet application or even a plain text editor, consists of one header line (or row), followed by data rows. Each data value is on one line of the file with a list of the variable values that correspond to that data value. For example, *Figure A* shows a file with three lines: the header row and two data value rows. Note the specific formatting is different than what is shown here; note also this would be a small subset of the overall dataset.

<table border="1" align="center" cellspacing="0" cellpadding="3">
	<caption>Fig. A: Sample File Content</caption>
	<th>Subject</th>
	<th>Subset</th>
	<th>gIFN</th>
	<th>IL2</th>
	<th>Value</th>
	<tr>
		<td width="25%" align="center">01</td>
		<td width="25%" align="center">CD4</td>
		<td width="25%" align="center">+</td>
		<td width="25%" align="center">+</td>
		<td width="25%" align="center">0.05</td>
	</tr>
	<tr>
		<td width="25%" align="center">01</td>
		<td width="25%" align="center">CD8</td>
		<td width="25%" align="center">+</td>
		<td width="25%" align="center">-</td>
		<td width="25%" align="center">0.1</td>
	</tr>
</table>

The two lines in *Figure A* correspond to two measurements: one for subject 01, for CD4 cells that are gIFN+ and IL2+ with a value of 0.05 (perhaps this is a fraction of total CD4 cells). The second is also for subject 01 but for CD8 cells that are gIFN+ and IL2- with a value of 0.1 (perhaps a fraction of total CD8 cells). This list could be extended for all subsets, all subjects, and all cytokine combinations, with a single percentage on each line. SPICE can read data in this fashion.

### Requirements

The following requirements must be met for any tabular (delimited) data file to be readable by SPICE:

- The file must include a header row.
- There must be only one header row.
- The header row must be the very first row (line) of the file.
- All but the last field must contain the variable names you expect SPICE to use.
- The last field of the header row must be titled "Value" (not case-sensitive)
- There must be only one value for each row (and it must be the last field, as mentioned above).
- All rows (including the header) must contain the same number of fields.
- There must be no blank lines or comments anywhere in the file.

### Importing Into SPICE

To import a delimited file into SPICE, simply choose "Open" from the "File" menu, navigate to the desired file, and open it as usual. Note, SPICE expects a comma as the delimiter of a `.csv` file, and a tab as the delimiter of a `.tab` file. If you use a different character as a delimiter, you should give your file a `.txt` extension (SPICE will prompt you for the character when opening the file in this case).

### Data from FlowJo

FlowJo will output tabular data (for example, for arrays of Boolean gates) in matrix format. This data can therefore be imported into SPICE with relatively little rearrangement. Examples of this are provided in the following sections.

### Recommended Editors

It is not recommended to use a plain text editor when manipulating tabular data files. As a consequence of such an open text format, a single misplaced or stray character can cause everything after it to be misinterpreted. We recommend using [Excel](http://microsoft.com/office/excel) or [XTabulator](http://bartastechnologies.com/xtabulator) to format and edit tabular data files (CSV, TAB/TSV, etc.). When using Excel, take care not to select or edit cells to the right of actual data cells or Excel will automatically add extra fields to the end of the record when you save as CSV or TAB.