---
layout: page
title: Discussion
---

### Dealing with commas as part of data values in `csv` files

When talking about [exporting data](../05-exporting-data/) we discussed how to export Excel file formats into `csv`. Comma Separated Value files are indeed very useful and allow for easily exchanging and sharing data. 

However, there are some significant problems with this particular format. Quite often the data values themselves may include commas (,). In that case, the software which you use (including Excel) will most likely incorrectly display the data in columns. This is because the commas which are a part of the data values will be interpreted as delimiters.

For example, our data might look like this:
	
		species_id,genus,species,taxa
		AB,Amphispiza,bilineata,Bird
		AH,Ammospermophilus,harrisi,Rodent-not,censused
		AS,Ammodramus,savannarum,Bird
		BA,Baiomys,taylori,Rodent

In the record `AH,Ammospermophilus,harrisi,Rodent-not,censused` the value for `taxa` includes a comma (`Rodent-not,censused`). 
If we try to read the above into Excel (or other spreadsheet program), we will get something like this:

![Issue with importing csv format](../fig/csv-mistake.png)

The value for `taxa` was split into two columns (instead of being put in one column `D`). This can propagate to a number of further errors. For example, the extra column will be interpreted as a column with many missing values (and without a proper header). In addition to that, the value in column `D` for the record in row 3 (so the one where the value for 'taxa' contained the comma) is now incorrect. 

If you want to store your data in `csv` format and expect that your data values may contain commas, you can avoid the problem discussed above by putting the values in quotes (""). Applying this rule, our data might look like this:

	species_id,genus,species,taxa
	"AB","Amphispiza","bilineata","Bird"
	"AH","Ammospermophilus","harrisi","Rodent-not, censused"
	"AS","Ammodramus","savannarum","Bird"
	"BA","Baiomys","taylori","Rodent"

Now opening this file as a `csv` in Excel will not lead to an extra column, because Excel will only use commas that fall outside of quotation marks as delimiting characters. However, if you are working with an already existing dataset in which the data values are not included in "" but which have commas as both delimiters and parts of data values, you are potentially facing a major problem with data cleaning.

If the dataset you're dealing with contains hundreds or thousands of records, cleaning them up manually (by either removing commas from the data values or putting the values into quotes - "") is not only going to take hours and hours but may potentially end up with you accidentally introducing many errors.

Cleaning up datasets is one of the major problems in many scientific disciplines. The approach almost always depends on the particular context. However, it is a good practice to clean the data in an automated fashion, for example by writing and running a script. The Python and R lessons will give you the basis for developing skills to build relevant scripts.

