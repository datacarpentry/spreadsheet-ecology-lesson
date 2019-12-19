---
title: "Introduction"
teaching: 15
exercises: 3
questions:
- "What are basic principles for using spreadsheets for good data organization?"
objectives:
- "Describe best practices for organizing data so computers can make the best use of data sets."
keypoints:
- "Good data organization is the foundation of any research project."
---

Good data organization is the foundation of your research
project. Most researchers have data or do data entry in
spreadsheets. Spreadsheet programs are very useful graphical
interfaces for designing data tables and handling very basic data
quality control functions.

### Spreadsheet outline

After this lesson, you will be able to:
- Implement best practices in data table formatting  
- Identify and address common formatting mistakes
- Understand approaches for handling dates in spreadsheets
- Utilize basic quality control features and data manipulation practices
- Effectively export data from spreadsheet programs

*Overall good data practices*

Spreadsheets are good for data entry. Therefore we have a lot of data
in spreadsheets. 
Much of your time as a researcher will be spent in this 'data wrangling' stage.
It's not the most fun, but it's necessary. We'll teach you how to think
about data organization and some practices for more effective data wrangling.

### What this lesson will not teach you

- How to do *statistics* in a spreadsheet
- How to do *plotting* in a spreadsheet
- How to *write code* in spreadsheet programs

If you're looking to do this, a good reference is
[Head First Excel](https://www.amazon.com/Head-First-Excel-learners-spreadsheets/dp/0596807694/), published by O'Reilly.

---

### Why aren't we teaching data analysis in spreadsheets

- Data analysis in spreadsheets usually requires a lot of manual
  work. If you want to change a parameter or run an analysis with a
  new dataset, you usually have to redo everything by hand. (We do
  know that you can create macros, but see the next point.)

- It is also difficult to track or reproduce statistical or plotting
  analyses done in spreadsheet programs when you want to go back to
  your work or someone asks for details of your analysis.

### Spreadsheet programs

Many spreadsheet programs are available. Since most participants utilize Excel as their primary spreadsheet program, this lesson will make use of Excel examples.

A free spreadsheet program that can also be used is LibreOffice.

Commands may differ a bit between programs, but the general idea
is the same.

> ## Exercise
> - How many people have used spreadsheets in their research?
> - How many people have accidentally done something that made them
> frustrated or sad?
{: .callout}

Spreadsheets encompass a lot of the things we need
to be able to do as researchers. We can use them for:

- Data entry
- Organizing data
- Subsetting and sorting data
- Statistics
- Plotting

We do a lot of different operations in spreadsheets. What kind of operations do you do in spreadsheets? Which ones do you think spreadsheets are good for?


## Problems with Spreadsheets

Spreadsheets are good for data entry, but in reality we tend to
use spreadsheet programs for much more than data entry. We use them
to create data tables for publications, to generate summary
statistics, and make figures.

Generating tables for publications in a spreadsheet is not
optimal - often, when formatting a data table for publication, we’re
reporting key summary statistics in a way that is not really meant to
be read as data, and often involves special formatting
(merging cells, creating borders, making it pretty). We advise you to
do this sort of operation within your document editing software.

The latter two applications, generating statistics and figures, should 
be used with caution: because of the graphical, drag and drop nature of 
spreadsheet programs, it can be very difficult, if not impossible, to 
replicate your steps (much less retrace anyone else's), particularly if your 
stats or figures require you to do more complex calculations. Furthermore, 
in doing calculations in a spreadsheet, it’s easy to accidentally apply a 
slightly different formula to multiple adjacent cells. When using a 
command-line based statistics program like R or SAS, it’s practically 
impossible to apply a calculation to one observation in your 
dataset but not another unless you’re doing it on purpose. 

### Using Spreadsheets for Data Entry and Cleaning

However, there are circumstances where you might want to use a spreadsheet 
program to produce “quick and dirty” calculations or figures, and data 
cleaning will help you use some of these features. Data cleaning also
puts your data in a better format prior to importation into a 
statistical analysis program. We will show you how to use some features of 
spreadsheet programs to check your data quality along the way and produce 
preliminary summary statistics.

In this lesson, we will assume that you are most likely using Excel as
your primary spreadsheet program - there are others (gnumeric, Calc
from OpenOffice), and their functionality is similar, but Excel seems
to be the program most used by biologists and ecologists.

In this lesson we're going to talk about:

1. [Formatting data tables in spreadsheets](../01-format-data/)
2. [Formatting problems](../02-common-mistakes/)
3. [Dates as data](../03-dates-as-data/)
4. [Quality control](../04-quality-control/)
5. [Exporting data](../05-exporting-data/)

