---
layout: page
title: Managing dates and times in spreadsheets
---
Correct handling of dates and times in a spreadsheet can be done with little to no hassle if we use the correct functions. Spreadsheet programs are designed to be able to handle different conventions in use around the world, since the work is already done, we might as well use it to our advantage. 
Please remember that functions that are valid for a given spreadsheet program (be it excel, open/libre office, gnumeric, etc) are usually guaranteed to be compatible only within the same famly of products. If you will later need to export the data and need to conserve the timestamps you are better off handling them using custom solutions.   


> ## Prerequisites {.prereq}
>
> Only basic knowledge of spreadsheets is required; you must be able to:
>
>* reference a cell
>* change the format type of a cell
>* add a function to a cell 



## Topics
1. Overview
2. Working with dates and times
3. Final notes

## Overview
Please dowload and open the reference spreadsheet to follow along the lesson, it is available in both excel ([date.time.xls](../data/biology/date.time.xls)) and OpenDocument ([date.time.ods](../data/biology/date.time.ods)) format.

## Working with dates and times
Current time and date are best retrieved using the functions NOW() and TODAY(), the results will be formatted according to your computer's settings.

```
NOW()   # returns the current date and time

TODAY() # returns the current date

`# current time is derived from these 2 functions  `
NOW()-TODAY()
```

Single bits of information can be extracted from any date string using the appropriate function:

```
YEAR()      # extracts the year

MONTH()     # extracts the month

DAY()       # extracts the day

HOUR()      # extracts the hour

MINUTE()    # extracts the minute

SECOND()    # extracts the second
```

> ### Exercise
> Try to extract the year, month and day from the current date and time string returned by the NOW() function.
> Try to extract the hour and minute from the same string (press F9 to force the spreadsheet to recalculate the NOW() function).
>

### Adding days, months or years to dates
By using the above functions we can easily add days, months or years to a given date. Month and year rollovers are internally tracked and applied.
To add a finite number of days, just add the to the date.

Adding years and months and days is slightly trickier because we need to make sure that we are adding the amount to the correct entity.

- First we extract the single entities (day, month or year)
- We can then add values to to that
- Finally the complete date string is reconstructed using the DATE() function.


As for dates, times are handled in a similar way; seconds cam be directly added but to add hour and minutes we need to make sure that we are adding the quantities to the correct entities 

## Final notes
As already noted, these data formats do not export easily, if the data is to be exported in any other format a different solution is needed.
A simple alternative is to convert the the date string in a single string using the format YYYYMMDDhhmmss, where:

```
For example the date March 24, 2015 17:25:35 would become: 20150324172535
YYYY:   the full year i.e. 2015
MM:     the month, i.e. march would be 03
DD:     the day of month, i.e. 24
hh:     hour of day, i.e 17
mm:     minutes, i.e 25
ss:     seconds, i.e. 35
```
This strings will sort correctly in ascendng or descending order and by knowing the format it can then be correctly managed by the receiving software.
