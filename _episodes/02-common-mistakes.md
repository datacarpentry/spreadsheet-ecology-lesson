---
title: "Formatting problems"
teaching: 20
exercises: 0
questions:
- "What are some common challenges with formatting data in spreadsheets and how can we avoid them?"
objectives:
- "Recognize and resolve common spreadsheet formatting problems."
keypoints:
- "Avoid using multiple tables within one spreadsheet."
- "Avoid spreading data across multiple tabs."
- "Record zeros as zeros."
- "Use an appropriate null value to record missing data."
- "Don't use formatting to convey information or to make your spreadsheet look pretty."
- "Place comments in a separate column."
- "Record units in column headers."
- "Include only one piece of information in a cell."
- "Avoid spaces, numbers and special characters in column headers."
- "Avoid special characters in your data."
- "Record metadata in a separate plain text file."
---

## Common Spreadsheet Errors

This lesson is meant to be used as a reference for discussion as learners identify issues with the messy dataset discussed in the
previous lesson. Instructors: don't go through this lesson except to refer to responses to the exercise in the previous lesson.

There are a few potential errors to be on the lookout for in your own data as well as data from collaborators or the Internet. If you are aware of the errors and the possible negative effect on downstream data analysis and result interpretation, it might motivate yourself and your project members to try and avoid them. Making small changes to the way you format your data in spreadsheets can have a great impact on efficiency and reliability when it comes to data cleaning and analysis.

- [Using multiple tables](#tables)
- [Using multiple tabs](#tabs)
- [Not filling in zeros](#zeros)
- [Using problematic null values](#null)
- [Using formatting to convey information](#formatting)
- [Using formatting to make the data sheet look pretty](#formatting_pretty)
- [Placing comments or units in cells](#units)
- [Entering more than one piece of information in a cell](#info)
- [Using problematic field names](#field_name)
- [Using special characters in data](#special)
- [Inclusion of metadata in data table](#metadata)
- [Date formatting](../03-dates-as-data/)


## <a name="tables"></a> Using multiple tables

A common strategy is creating multiple data tables within
one spreadsheet. This confuses the computer, so don't do this!
When you create multiple tables within one
spreadsheet, you’re drawing false associations between things for the computer,
which sees each row as an observation. You’re also potentially using the same
field name in multiple places, which will make it harder to clean your data up
into a usable form. The example below depicts the problem:

![multiple tabs](../fig/2_datasheet_example.jpg)

In the example above, the computer will see (for example) row 4 and assume that all columns A-AF 
refer to the same sample. This row actually represents four distinct samples 
(sample 1 for each of four different collection dates - May 29th, June 12th, June 19th, and June 26th), 
as well as some calculated summary statistics (an average (avr) and standard error of measurement (SEM)) for two of those samples. Other rows are similarly problematic.

## <a name="tabs"></a> Using multiple tabs

But what about workbook tabs? That seems like an easy way to organize data, right? Well, yes and no. When you create extra tabs, you fail to allow the computer to see connections in the data that are there (you have to introduce spreadsheet application-specific functions or scripting to ensure this connection). Say, for instance, you make a separate tab for each day you take a measurement.

This isn't good practice for two reasons:
1) you are more likely to accidentally add inconsistencies to your data if each time you take a measurement, you start recording data in a new tab, and
2) even if you manage to prevent all inconsistencies from creeping in, you will add an extra step for yourself before you analyze the
data because you will have to combine these data into a single datatable. You will have to explicitly tell the computer how to combine
tabs - and if the tabs are inconsistently formatted, you might even have to do it manually.

The next time you’re entering data, and you go to create another tab or table, ask yourself if you could avoid adding this tab by adding another column to your original spreadsheet. We used multiple tabs in our example of a messy data file, but now you've seen how you can reorganize your data to consolidate across tabs.

Your data sheet might get very long over the course of the experiment. This makes it harder to enter data if you can’t see your headers
at the top of the spreadsheet. But don't repeat your header row. These can easily get mixed into the data, 
leading to problems down the road.

Instead you can freeze the column headers so that they remain visible even when you have a spreadsheet with many rows.

[Documentation on how to freeze column headers in MS Excel](https://support.office.com/en-ca/article/Freeze-column-headings-for-easy-scrolling-57ccce0c-cf85-4725-9579-c5d13106ca6a)

## <a name="zeros"></a> Not filling in zeros

It might be that when you're measuring something, it's
usually a zero, say the number of times a rabbit
is observed in the survey. Why bother
writing in the number zero in that column, when it's mostly zeros?

However, there's a difference between a zero and a blank cell in a spreadsheet. To the computer, a zero is actually data. You measured
or counted it. A blank cell means that it wasn't measured and the computer will interpret it as an unknown value (otherwise known as a
null value). 

The spreadsheets or statistical programs will likely mis-interpret blank cells that you intend to be zeros. By not entering the value of
your observation, you are telling your computer to represent that data as unknown or missing (null). This can cause problems with 
subsequent calculations or analyses. For example, the average of a set of numbers which includes a single null value is always null
(because the computer can't guess the value of the missing observations). Because of this, it's very important to record zeros as zeros and truly missing data as nulls.


## <a name="null"></a> Using problematic null values
**Example**: using -999 or other numerical values (or zero) to represent missing data. 

**Solutions**: 

There are a few reasons why null values get represented differently within a dataset.
Sometimes confusing null values are automatically recorded from the measuring device. If that's the case, there's not much you can do, but it can be addressed in data cleaning with a tool like [OpenRefine](http://www.datacarpentry.org/OpenRefine-ecology-lesson/) before analysis. Other times different null values are used to convey different reasons why the data isn't there. This is important information to capture, but is in effect using one column to capture two pieces of information. Like for [using formatting to convey information](#formatting) it would be good here to create a new column like 'data_missing' and use that column to capture the different reasons. 

Whatever the reason, it's a problem if unknown or missing data is recorded as -999, 999, or 0.
Many statistical programs will not recognize
that these are intended to represent missing (null) values. How these values are interpreted will depend on the software you use to
analyze your data. It is essential to use a clearly defined and consistent null indicator.
Blanks (most applications) and NA (for R) are good choices. White et al, 2013, explain good choices for indicating null values for different software applications in their article:
[Nine simple ways to make it easier to (re)use your data.](https://peerj.com/preprints/7/) Ideas in Ecology and Evolution.

![White et al.](../fig/3_white_table_1.jpg)


## <a name="formatting"></a> Using formatting to convey information 

**Example**: highlighting cells, rows or columns that should be excluded from an analysis, leaving blank rows to indicate separations in data.

![formatting](../fig/formatting.png)

**Solution**: create a new field to encode which data should be excluded.

![good formatting](../fig/good_formatting.png)


## <a name="formatting_pretty"></a> Using formatting to make the data sheet look pretty

**Example**: merging cells.

**Solution**: If you’re not careful, formatting a worksheet to be more aesthetically pleasing can compromise your computer’s ability to
see associations in the data. Merged cells will make your data unreadable by statistics software. Consider restructuring your data in
such a way that you will not need to merge cells to organize your data.


## <a name="units"></a> Placing comments or units in cells

**Example**: Your data was collected, in part, by a summer student who you later found out was mis-identifying some of your species, some
of the time. You want a way to note these data are suspect.

**Solution**: Most analysis software can't see Excel or LibreOffice comments, and would be confused by comments placed within your data
cells. As described above for formatting, create another field if you need to add notes to cells. Similarly, don’t include units in
cells: ideally, all the measurements you place in one column should be in the same unit, but if for some reason they aren’t, create
another field and specify the units the cell is in.


## <a name="info"></a> Entering more than one piece of information in a cell

**Example**: You find one male, and one female of the same species. You enter this as 1M, 1F.

**Solution**: Don't include more than one piece of information in a cell. This will limit the ways in which you can analyze your data. 
If you need both these measurements, design your data sheet to include this information. For example, include one column for number of
individuals and a separate column for sex.

## <a name="field_name"></a> Using problematic field names
Choose descriptive field names, but be careful not to include spaces, numbers, or special characters of any kind. Spaces can be
misinterpreted by parsers that use whitespace as delimiters and some programs don’t like field names that are text strings that start
with numbers.  

Underscores (`_`) are a good alternative to spaces. Consider writing names in camel case (like this: ExampleFileName) to improve
readability. Remember that abbreviations that make sense at the moment may not be so obvious in 6 months, but don't overdo it with names
that are excessively long. Including the units in the field names avoids confusion and enables others to readily interpret your fields.

**Examples**  

<table align = "left" style = "width =50%; border: 1px solid black;">
<tr>
	<td> <b>Good Name</b></td> <br />
	<td> <b>Good Alternative </b> </td><br />
	<td> <b>Avoid </b></td><br />
</tr>
<tr>
	<td> Max_temp_C</td>
	<td> MaxTemp </td>
	<td> Maximum Temp (°C) </td>
</tr>
<tr>
	<td> Precipitation_mm</td>
	<td> Precipitation</td>
	<td> precmm </td>
</tr>	
<tr>
	<td> Mean_year_growth</td>
	<td> MeanYearGrowth </td>
	<td> Mean growth/year</td>	
</tr>	
<tr>
	<td> sex </td>
	<td> sex </td>	
	<td> M/F </td>
</tr>
<tr>	
	<td> weight </td>
	<td> weight </td>	
	<td> w.</td>	
</tr>
<tr>	
	<td> cell_type </td>
	<td> CellType </td>
	<td> Cell Type </td>
</tr>
<tr>
	<td> Observation_01 </td>
	<td> first_observation</td>
	<td> 1st Obs</td>
</tr>
</table>

## <a name="special"></a> Using special characters in data

**Example**: You treat your spreadsheet program as a word processor when writing notes, for example copying data directly from Word or
other applications.

**Solution**: This is a common strategy. For example, when writing longer text in a cell, people often include line breaks, em-dashes,
etc in their spreadsheet.  Also, when copying data in from applications such as Word, formatting and fancy non-standard characters (such
as left- and right-aligned quotation marks) are included.  When exporting this data into a coding/statistical environment or into a
relational database, dangerous things may occur, such as lines being cut in half and encoding errors being thrown.

General best practice is to avoid adding characters such as newlines, tabs, and vertical tabs.  In other words, treat a text cell as if
it were a simple web form that can only contain text and spaces.


## <a name="metadata"></a> Inclusion of metadata in data table

**Example**: You add a legend at the top or bottom of your data table explaining column meaning, units, exceptions, etc.

**Solution**: Recording data about your data (“metadata”) is essential. You may be on intimate terms with your dataset while you are 
collecting and analysing it, but the chances that you will still remember that the variable "sglmemgp" means single member of group, for
example, or the exact algorithm you used to transform a variable or create a derived one, after a few months, a year, or more are slim.  

As well, there are many reasons other people may want to examine or use your data - to understand your findings, to verify your findings,
to review your submitted publication, to replicate your results, to design a similar study, or even to archive your data for access and 
re-use by others. While digital data by definition are machine-readable, understanding their meaning is a job for human beings. The 
importance of documenting your data during the collection and analysis phase of your research cannot be overestimated, especially if your
research is going to be part of the scholarly record.  

However, metadata should not be contained in the data file itself. Unlike a table in a paper or a supplemental file, metadata (in the 
form of legends) should not be included in a data file since this information is not data, and including it can disrupt how computer 
programs interpret your data file. Rather, metadata should be stored as a separate file in the same directory as your data file, 
preferably in plain text format with a name that clearly associates it with your data file. Because metadata files are free text format,
they also allow you to encode comments, units, information about how null values are encoded, etc. that are important to document but can
disrupt the formatting of your data file.  

Additionally, file or database level metadata describes how files that make up the dataset relate to each other; what format are they are 
in; and whether they supercede or are superceded by previous files. A folder-level readme.txt file is the classic way of accounting for 
all the files and folders in a project.  

(Text on metadata adapted from the online course Research Data [MANTRA](http://datalib.edina.ac.uk/mantra) by EDINA and Data Library, University of Edinburgh. MANTRA is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).)
