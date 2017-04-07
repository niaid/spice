---
layout: help
title: What's New
---

This document will outline the major differences between SPICE 5 and SPICE 6. Please read this carefully!

Given the changes, why should you upgrade? First of all, SPICE 5.x (like 4.x before it) will no longer be supported or developed. SPICE 6 is based on more modern technology, and has a much greater potential for development. SPICE 6 can handle much larger data sets and is often far faster through the more widespread use of multi-core support as well as more efficient memory management.

We greatly appreciate feedback. Please report bugs or unexpected behaviors as soon as possible by using the "Request Support" link found under SPICE's Help menu. SPICE 6 will evolve quickly to fix bugs and gain functionality beyond what 5.x accomplished.

## Mac OS X 10.9 Required

To take advantage of more recent advancements on the Mac platform, SPICE 6 requires Mac OS X (now *MacOS*) 10.9 or higher. SPICE 6 **will not run** on previous versions of Mac OS X. Compare this with SPICE 5's support of 10.5.

## Query Groups (Were Data Views)

Data Views in SPICE 5 are now called *Query Groups*. This is because SPICE 6 now groups all figures belonging to a query together in the user interface, which better represents the hierarchical relationship between figure and query. The query group holds the query settings. Select the query group in the Outline View (see below) to edit its query settings.

Query group result data can be exported as a tab-separated text file by dragging the query group from the Outline View to the Finder (including the Desktop) or by using the Export toolbar button.

## Figures

Plots and Charts are now called *Figures*.

v6 offers several new figure (plot) types in the form of Category, Overlay, Group, and Query Description legends. Statistical tests (Permutation, Wilcoxon Rank Sum, and Student's t) are now standalone figures - that is, they're no longer bound to Pie and Bar  figures as in v5.

Within each Query Group, you can now have more than one figure of a given type. That is, you can have multiple Pie figures, each with its own settings, or multiple Bar figures, etc. This avoids the duplication of Data Views that was necessary in v5 to have more than one figure of a type with different visual attributes but sharing the same query.

As always, exported figures (via copy/paste, the Export toolbar button, or by drag and drop to an application or the Finder/Desktop) are PDF vector graphics, which are decomposable and editable in any vector graphics editor.

All figures (even existing ones such as Pie and Bar) have many new formatting options. See the documentation or explore on your own to discover them.

## Canvases

A new concept has been added in v6 called a *Canvas*. A canvas can consist of any number of figures, spatially arranged any way you wish. This includes figures from multiple query groups in a single canvas. This gives you the freedom to compose multiple related figures into a single graphic for export. An exported canvas behaves like any other figure - that is, it's a decomposable PDF vector graphic that is editable in any vector graphics editor application. You can create, manage, and edit canvases in the Canvas View (see below).

## Outline View vs. Canvas View

v6 now has two basic view modes: Outline View and Canvas View. Most of your work will be done in Outline View. The view mode can be changed via the View Mode toolbar button. 

Outline mode allows you to define query groups and add figures to them, to edit their settings, and to export them individually or in a group. To rename query groups and figures in Outline mode, click to select the item, then click the caption (title) to reveal an editor.

Canvas mode allows you to compose multiple figures created in Outline mode into one or more canvases, as well as to tweak figure settings and export the selected canvas. To rename a canvas, select it, then click the caption (title) to reveal an editor.

## Adding Assets

To add query groups, figures, and canvases ("assets") to your SPICE document, you can use the Add button in the toolbar or the Query or Figure menues in the main menu. In v5, you would create a data view and "turn on" various plots in the data view's formatting panel; in v6 all assets are added, removed, or duplicated using the same toolbar control. The Add menu is contextual depending on the view mode (Outline or Canvas) and the current selection. 

## Styles

v6 introduces a new concept called *Styles*. Each figure by default has its own formatting "style". Styles can be copied and pasted onto other figures of the same type, even across multiple documents. 

This is taken one step further with the concept of *Shared Styles*. A regular figure style can be promoted to a shared style, which can then be used by any figure of the same type, across any query group, within the same document. This overrides the figure's own style and when a shared style is changed in any participating figure, all participating figures will be immediately updated with the same settings. The style controls can be found at the top of the formatting panel on the right side of the document window when a figure is selected.

## Colors

The behavior of colors and color schemes has changed somewhat in v6. 

In v5, you could choose a custom color scheme or an automatically-maintained scheme. This caused some usability problems. For example, with large numbers of categories, the individual slices in a Pie figure could be difficult to distinguish. To simplify this behavior, color schemes are now to be considered all "custom". You predefine how many colors your scheme should hold, and whether or not to repeat the pattern. You can apply a color *function* (such as Rainbow or Blue-To-Red) to the existing colors in your scheme at any time but this is no longer done automatically across the full number of colors needed. Clicking the "details" button (•••) in any color control reveals a popover with the full color settings. Clicking individual colors allows you to edit just that color.

The new system also allows for single-color schemes to be defined, which allows the same familiar user interface to be used in all color management actions.

Additionally, color schemes can be copied and pasted in much the same way as figure styles can, using the same color management user interface. The copy/paste control for schemes is found in the details button (•••). To transfer a scheme from one place to another, click the details button in the source color control, then click the Copy button. Click the details button on the target color control and click Paste.

## File Format

The file format in SPICE 6 has changed. In order to differentiate between the documents of either version, SPICE 6.x documents bear the extension `.spice6doc` (versus the SPICE 4.x extension `.spd`, and version 5's `.spicedoc` and `.spicedocument`).

SPICE 4 used a text-based file format that you could edit if you wished. For performance and data integrity reasons, this is no longer the case. The data in SPICE 6 is stored in a binary format for better performance and expandability (with future features in mind). These files cannot be modified or viewed outside of SPICE 6. *Modifying these files with an application other than SPICE 6 will damage the file.*

However, SPICE 6 can import SPICE 4 documents (with the exception of previously-saved views as well as SPICE 5 documents, which are not imported), and delimited text data files (comma-separated, tab-separated, etc.). Thus, if you create the SPICE file using Pestle, you can still edit that file and re-import it into SPICE 6.

For importing data from tabular data files, provided the files are properly formatted, we recommend [Excel](http://microsoft.com/office/excel) or [XTabulator](http://bartastechnologies.com/xtabulator) for formatting and editing tabular data files (`CSV`, `TAB`/`TSV`, `.txt`, `.dat`, etc.).

## Thresholding

Thresholding is now a one-time operation that occurs after all other computation is done.

## Licensing

SPICE 6 is now individually licensed. You will need to obtain a serial number to run the program, which is specific to each user. Serial numbers are free (SPICE is free of charge), but the licensing scheme is used so that we can manage upgrades and keep track of usage as well as ensuring that users have agreed to the terms of the program. When unregistered, users are prompted when the application launches to fill out a simple form an accept the agreement. Once the form is completed and submitted, the application obtains a license over the Internet automatically. **You must have an active Internet connection to register SPICE 6.**
