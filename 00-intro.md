---
layout: lesson
title: Using spreadsheet programs for scientific data
root: .
---

Authors:**Christie Bahlai**, **Aleksandra Pawlik**<br>
Contributors: **Jennifer Bryan**, **Alexander Duryee**, **Jeffrey Hollister**, **Daisie Huang**, **Owen Jones**, **Clare Sloggett**, **Harriet Dashnow** and
**Ben Marwick**

Spreadsheet programs are very useful graphical interfaces for designing data tables and handling very basic data quality control functions. 

---

### Spreadsheet programs

- LibreOffice - used in these lessons because it's a free, open source
spreadsheet program
- Microsoft Excel
- Gnumeric
- OpenOffice.org

Commands may differ a bit between programs, but general ideas
for thinking about spreadsheets is the same.

---

Spreadsheets encompass a lot of the things we need
to be able to do as researchers. We can use them for:

- Data entry
- Organizing data
- Subsetting and sorting data
- Statistics
- Plotting

---

How many people have used spreadsheets in their research?

Spreadsheets can be very useful, but they can also be
frustrating and even sometimes give us incorrect results.

What are some things that you've accidentally done in
a spreadsheet, or have been frustrated that you can't do
easily?

---

### Spreadsheet outline

In this lesson, we’re going to talk about:

- Good data entry practices - formatting data tables in spreadsheets
- How to avoid common formatting mistakes
- Dates as data - beware!
- Basic quality control and data manipulation in spreadsheets
- Exporting data from spreadsheets

*Overall good data practices*

---

### What this lesson will not teach you

- How to do statistics in a spreadsheet
- How to do plotting in a spreadsheet
- How to write code in spreadsheet programs

If you're looking to do this, a good reference is
Head First Excel by O'Reilly

---

### Why aren't we teaching this

- It is difficult to track or reproduce statistical
or plotting analyses done in spreadsheet programs

---


The cardinal rules of using spreadsheet programs for data:

	1. Put all your variables in columns
	2. Put each observation in its own row
	3. Leave the raw data raw - don’t mess with it!
	4. Export to a text based format like CSV.

In reality, though, many scientists use spreadsheet programs for much more 
than this. We use them to create data tables for publications, to generate 
summary statistics, and make figures. 
Generating tables for publications in a spreadsheet is not optimal- often, 
when formatting a data table for publication, we’re reporting key summary 
statistics in a way that is not really meant to be read as data, and often 
involves special formatting (merging cells, creating borders, making it 
pretty). We advise you to do this sort of operation within your document 
editing software.

The latter two applications,  generating statistics and figures,  should 
be used with caution: because of the graphical, drag and drop nature of 
spreadsheet programs, it can be very difficult, if not impossible, to 
replicate your steps (much less retrace anyone else's), particularly if your 
stats or figures require you to do more complex calculations. Furthermore, 
in doing calculations in a spreadsheet, it’s easy to accidentally apply a 
slightly different formula to multiple adjacent cells. When using a 
command-line based statistics program like R or SAS, it’s practically 
impossible to accidentally apply a calculation to one observation in your 
dataset but not another unless you’re doing it on purpose. 

HOWEVER, there are circumstances where you might want to use a spreadsheet 
program to produce “quick and dirty” calculations or figures, and some of 
these features can be used in data cleaning, prior to importation into a 
statistical analysis program. We will show you how to use some features of 
spreadsheet programs to check your data quality along the way and produce 
preliminary summary statistics.

In this lesson, we will assume that you are most likely using Excel as your 
primary spreadsheet program- there are others (gnumeric, Calc from OpenOffice),
 and their functionality is similar, but Excel seems to be the program most 
used by biologists and ecologists.

![Helpful clippy - img by @tim_yates](fig/1_helpful_clippy.jpg)

In this lesson, we’re going to talk about:

1. [Formatting data tables in spreadsheets.](01-format-data.html)
2. [Common formatting mistakes by spreadsheet users.](02-common-mistakes.html)
3. [Dates as data.](03-dates-as-data.html)
4. [Basic quality control and data manipulation in spreadsheets.](04-quality-control.html)
5. [Exporting data from spreadsheets.](05-exporting-data.html)
6. [Data export formats caveats](06-data-formats-caveats.html)

Next: [Formatting data tables in spreadsheets.](01-format-data.html)
