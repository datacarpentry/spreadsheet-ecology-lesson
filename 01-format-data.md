---
layout: lesson
title: Formatting data tables in Spreadsheets
root: .
---

Authors: **Christie Bahlai**, **Aleksandra Pawlik**<br>
Contributors: **Jennifer Bryan**, **Alexander Duryee**, **Jeffrey Hollister**, **Daisie Huang**, **Owen Jones**, 
**Ben Marwick** and **Sebastian Kupny**.

## Learning Objectives
* Learning best practices for recording and formatting data in spreadsheets
* Understanding the correspondence between columns and rows in spreadsheets 
and data structure
* Understanding the correspondence between spreadsheet cells, columns and rows 
and data observations and values


The most common mistake made is treating the 
program like it is a lab notebook- that is, relying on context, notes in the 
margin, spatial layout of data and fields to convey information. As humans, 
we can (usually) interpret these things, but computers are dumb, and unless 
we explain to the computer what every single thing means, it will not be able 
to see how our data fit together.

Using the power of computers, we can manage and analyze data in much more 
effective and faster ways, but to use that power, we have to set up
our data for the computer to be able to understand it (and computers are very 
literal).

This is why it’s extremely important to set up well-formatted tables from the 
outset- before you even start entering data from your very first preliminary 
experiment. **Data organization is the foundation of your research project.**
It can make it easier or harder to work with your data throughout your
analysis, so it's worth thinking about when you're doing your data
entry or setting up your experiment. You can set things up in a different
way in spreadsheets, but it limits your ability to work with the data
in other programs or have the you-of-6-months-from-now or your collaborator
work with the data. 


###Structuring data in spreadsheets

There are two rules you should keep in mind when entering your data 
into any spreadsheet:

1. Each data cell is an observation that must have all the relevant information 
connected to it for it to stand on its own.

2. You must make it clear to the computer how the data cells relate to the 
relevant information and each other.

For instance, we have data from a survey of small mammals in a desert ecosystem.
Different people have gone to the field and entered data in to a spreadsheet.
They keep track of things like species, plot, weight, sex and date collected. 

If they were to keep track of the data like this:

![multiple-info example](fig/multiple-info.png)

the problem is that species and sex are in the same field. So, if they wanted to 
look at all of one species or look at different weight distributions by sex, 
it would be hard to set up the data to do this. If instead we put sex and species 
in different columns, you can see that it would be much easier. 

###Columns for variables and rows for observations

The rule of thumb, when setting up a datasheet, is columns= variables, 
rows = observations, cells=data (values).

So, instead we should have:

![single-info example](fig/single-info.png)

## Exercise

We're going to take a messy version of the survey data and clean it up.

- Download the data by clicking on [https://github.com/tracykteal/excel-ecology/blob/gh-pages/data/biology/survey_data_tabs.xls](https://github.com/tracykteal/excel-ecology/blob/gh-pages/data/biology/survey_data_tabs.xls)

- Open up the data in a spreadsheet program 

- You can see that there are two tabs. Two field assistants conducted the surveys, one
in 2013 and one in 2014, and they both kept track of the data in their own way. Now
you're the person in charge of this project and you want to be able to start doing
statistics with the data. 

- With the person next to you, work on the messy data so that a computer will
be able to understand it. Clean up the 2013 and 2014 tabs, and put them all together
in one spreadsheet. 

After you go through this exercise, we'll discuss as a group what you think was wrong
with this data and how you fixed it. 

*Instructors see notes in 'instructors_notes.md' on this exercise.*

Previous: [Introduction](00-intro.html)  Next: [Formatting problems](02-common-mistakes.html)
