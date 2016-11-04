---
layout: lesson
title: Instructor notes
root: .
---

## Instructor notes

### Lesson purpose

The purpose of this lesson is not to teach how to do data analysis in spreadsheets, 
but to teach good data organization and how to do some data cleaning and 
quality control checking in a spreadsheet program.

### Narrative

#### [Introduction](00-intro.html)

* Introduce that we're teaching data organization, and that we're using
spreadsheets, because most people do data entry in spreadsheets or 
have data in spreadsheets.
* Emphasize that we are teaching good practice in data organization and that
this is the foundation of their research practice. Without organized and clean
data, it will be difficult for them to apply the things we're teaching in the
rest of the workshop to their data.
* Much of their lives as a researcher will be spent on this 'data wrangling' stage, but
some of it can be prevented with good strategies for data collection up front.
* Tell that we're not teaching data analysis or plotting in spreadsheets, because it's
very manual and also not reproducible. That's why we're teaching SQL, R, Python!
* Now let's talk about spreadsheets, and when we say spreadsheets, we mean any program that
does spreadsheets like Excel, LibreOffice, OpenOffice. Most learners are probably using Excel.
* Ask the audience any things they've accidentally done in spreadsheets. Talk about an example of your own, like that you accidentally sorted only a single column and not the rest
of the data in the spreadsheet. What are the pain points!?
* As people answer highlight some of these issues with spreadsheets

#### [Formatting data](01-format-data.html)

* Go through the point about keeping track of your steps and keeping raw data raw
* Go through the cardinal rule of spreadsheets about columns, rows and cells
* Hand them a messy data file and have them pair up and work together to clean up the data.
*Give them 15 minutes to do this.*
* Ask for what people did to clean the data. As they bring up different points you can
refer to them in the 02-common-mistakes.md file, or expand a bit on the point they brought up.
If you are just teaching the lesson, it would be good to familiarize yourself with 
the set of mistakes in 02-common-mistakes. All these mistakes are present in the messy
dataset.
* If you get a response where they've fixed the date, you can pause and go to the
03-dates-as-data.md lesson. Or you can say you'll come back to dates at the end. 
There's an exercise in that file about how to change the
date in to three columns using Excel's built in MONTH, DAY, YEAR functions. Have them
run through that exercise. 

#### [Common formatting problems](02-common-mistakes.html)

* **Don't go through this chapter** except to refer to as responses to the exercise in
the previous chapter.

#### [Dates as data](03-dates-as-data.html)

* Do the exercise and make the point about dates either in reponse to a learner bringing
up date as an issue during the responses, or at the end of the response time.

#### [Quality control](04-quality-control.html)
*This lesson currently needs updating*  

* Go through the exercises on different strategies for quality control, including
sorting, conditional formatting and pivot tables. 

#### [Exporting data](05-exporting-data.html)

* Have the students export their cleaned data as csv. Reiterate again the need for
data in this format for the other tools we'll be using.

#### [Data Format Caveats](06-data-formats-caveats.html)

* This is mainly here as a reference if people have questions about different file formats.
You don't need to go through this. 

#### Concluding points

* Now your data is organized so that a computer can read and understand it. This
let's you use the full power of the computer for your analyses as we'll see in the
rest of the workshop. 
* While your data is now neatly organized, it still might have errors or missing data
or other problems. It's like you put all your data in the right drawers, but the
drawers might still be messy. The next lesson is going to teach you OpenRefine which 
is great for data cleaning and for some of the quality control checking that we touched on 
in this lesson. It also has the advantage that it automatically keeps track of the
steps you take. 

### Potential issues

#### Excel looks and acts different on different OSes

The main challenge with this lesson is that Excel looks very different and how you
do things is even different between Mac and PC, and between different versions of
Excel. So, the presenter's environment will only be the same as some of the learners. 

We need better notes and screenshots of how things work on both Mac and PC. But we
likely won't be able to cover all the different versions of Excel. 

If you have a helper who has experience with the other OS than you, it would be good
to prep them to help with this lesson and tell how people to do things in the other OS.

#### People are not interactive or responsive on the Exercise

This lesson depends on people working on the exercise and responding with things
that are fixed. If your audience is reluctant to participate, start out with
some things on your own, or ask a helper for their answers. This generally gets
even a reluctant audience started. 
