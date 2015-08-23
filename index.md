---
layout: lesson
root: .
lastupdated: August 18, 2015
contributors: ["Christie Bahlai", "Aleksandra Pawlik", "Jennifer Bryan", "Alexander Duryee", "Jeffrey Hollister", "Daisie Huang", "Owen Jones", "Ben Marwick", "Tracy Teal"]
maintainers: ["Aleksandra Pawlik", "Tracy Teal"]
domain: Ecology
topic: Spreadsheets
software: Spreadsheets
dataurl: https://www.dropbox.com/s/5ncuacnd3arjitc/survey_data_tabs.xls?dl=0
status: Teaching
---

<!-- USING THIS LESSON TEMPLATE -->
<!-- Lesson specific information is taken from the YAML header at the top of the page -->

<!-- THE LESSON INFORMATION -->


#Data Carpentry {{ page.topic }} for {{ page.domain }}
=======

Data Carpentry's aim is to teach researchers basic concepts, skills,
and tools for working with data so that they can get more done in less
time, and with less pain. The lessons below were designed for those interested
in working with {{page.domain %}} data in {{page.topic %}}.


**Content Contributors: {{page.contributors | join: ', ' %}}**


**Lesson Maintainers: {{page.maintainers | join: ', ' %}}**


**Lesson status: {{ page.status }}**

### Instructors
See [Instructor notes](http://datacarpentry.github.io/spreadsheet-ecology-lesson/instructor_notes.html) on how to teach this lesson.

<!--
  [Information on Lesson Status Categories]()
-->

<!-- ###### INDEX OF LESSONS ON THIS TOPIC ###### -->

## Lessons:

1. [Introduction](00-intro.html)
2. [Formatting data](01-format-data.html)
3. [Common formatting problems](02-common-mistakes.html)
4. [Dates as data](03-dates-as-data.html)
5. [Quality control](04-quality-control.html)
6. [Exporting data](05-exporting-data.html)
7. [Data Format Caveats](06-data-formats-caveats.html)



## Data

Data files for the lesson are available here: [{{page.dataurl %}}]({{page.dataurl %}})


### Requirements

Data Carpentry's teaching is hands-on, so participants are encouraged to use
their own computers to insure the proper setup of tools for an efficient workflow.
*These lessons assume no prior knowledge of the skills or tools*, but working
through this lesson requires working copies of the software described below.
To most effectively use these materials, please make sure to install everything
*before* working through this lesson.




{% if page.software == "Python" %}
{% include pythonSetup.html %}
{% elsif page.software == "Spreadsheets" %}
{% include spreadsheetSetup.html %}
{% elsif page.software == "R" %}
{% include rSetup.html %}
{% else %}
{% include anySetup.html %}
{% endif %}

<p><strong>Twitter</strong>: @datacarpentry
