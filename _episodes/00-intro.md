---
title: "Introduction"
teaching: 10
exercises: 0
questions:
- "What are the basic principles for using spreadsheets for good data organisation?"
objectives:
- "Describe best practices for organising data so that computers can make the best use of it
for data analysis."
keypoints:
- "Good data organisation is the foundation of any research project."
---

After this lesson, you will be able to:

* Implement best practices in organising tabular data (that is, data organised in rows and columns)
* Identify and address common formatting mistakes
* Understand approaches for handling dates in spreadsheets
* Utilise basic quality control to validate data on input and limit incorrect data entry
* Effectively export data from spreadsheet programs
* Know overall good data practices

In this lesson, however, you will *not* learn:
- How to use statistics and formulas in spreadsheets, or
- How to plot graphs using spreadsheets

There are many good tutorials available online on the topic of data analysis in spreadsheets. If you are looking
to learn any of the above, a good reference is [Head First Excel](https://www.amazon.com/Head-First-Excel-learners-spreadsheets/dp/0596807694/ref=sr_1_1?ie=UTF8&qid=1491594584&sr=8-1&keywords=head+first+excel), published by O'Reilly.

## Spreadsheet programs

Good data organisation is the foundation of any research project that relies on data analysis - it is of paramount
importance to get this first step right in order to avoid time-consuming "data wrangling" and "data cleaning"
further down the line. Most researchers have data in spreadsheets or use spreadsheets for data entry. Spreadsheet programs are good for data
entry and provide very useful graphical interfaces for handling basic data quality control functions. Spreadsheets can provide a lot of functionality that researchers need:

- Data entry
- Organising data
- Subsetting and sorting data
- Statistics
- Plotting

Many spreadsheet programs are available. Most researchers utilise Excel as their primary spreadsheet program (this
lesson will make use of Excel examples and data in Excel's `xlsx`/`xls` formats), but free spreadsheet programs exist, including LibreOffice,
Gnumeric, OpenOffice.org or Google Spreadsheets. Commands may differ a bit between programs, but the general idea
is the same.

## What's wrong with spreadsheets?

The intricacies of spreadsheets make it hard to reproduce analysis and very difficult to
spot and correct errors. Sometimes this is due to human error (you will learn how to avoid some of them);
at other times it is due to the spreadsheet program itself: how many times have you accidentally done something in
a spreadsheet that caused a problem (or just made you frustrated)? You are not alone! For example,
[20% of genetics papers contain errors due to Excel converting gene names to calendar dates](https://www.theverge.com/2020/8/6/21355674/human-genes-rename-microsoft-excel-misreading-dates).

* Data analysis in spreadsheets requires a lot of manual work. If you change a parameter or want to use a new dataset,
you have to reproduce every action by hand or meticulously copy all the formulas to a new spreadsheet.
This is laborious and error-prone. (You can shortcut some of this work with macros... but see the next point.)
* There is no natural “starting point” for an analysis in a spreadsheet as it can happen in any cell. Some formulas
depend on formulas in other cells being evaluated and values calculated prior to their execution. This makes it difficult to
follow, track or reproduce analysis in spreadsheets.
* The reasoning behind the analysis is opaque in spreadsheets, which becomes a problem if someone asks to reproduce your
analysis, if you inherit someone else’s spreadsheet, or even if you want to go back to review your own work in a
spreadsheet.
* There are better tools for data analysis, e.g. writing a Python or an R script. While these are not
error-proof (nothing is!), they are much more readable and easier to analyse, test and verify by yourself and others.

## Using spreadsheets for data entry and cleaning

We will show you how to use some features of spreadsheet programs to check your data quality and how to clean your
data before importing it into a statistical analysis program.

Click the arrow in the bottom right of the page to proceed to the next lesson.
