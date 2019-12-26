---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: content
title: syllabus
---

# {{ site.short-title }} Syllabus {{ site.semester }} <a href="{{ site.baseurl }}/assets/docs/{{ site.short-semester }}_Stat100_Syllabus.pdf" target="\_blank">(View PDF)</a>

## Instructor Contact Information
[//]: # (Loops through instructor contact information)
<ul>
{% for instructor in site.data.info.contact %}
  <li>
     <b>{{ instructor.section }} Instructor: {{ instructor.name }}</b><br>
     Email: <b><a href="mailto:{{ instructor.email }}">{{ instructor.email }}</a></b>
   </li>
{% endfor %}
<b>* Please do not send emails to our illinois.edu accounts.</b>
</ul>

## Course Webpage
  * <b><a href="{{ site.data.info.course-link1 }}" target="\_blank">{{ site.data.info.course-link1 }}</a></b>
    <br>(short URL: <b><a href="{{ site.data.info.course-link2 }}" target="\_blank">{{ site.data.info.course-link2 }}</a></b>)
    <br>You can also google "stat 100" :)

## Course Materials
* **Required Workbook: {{ site.data.info.textbook.name }} {{ site.data.info.textbook.edition }} by {{ site.data.info.textbook.authors}}.**
    1. Available at the Illini Union Bookstore for {{ site.data.info.textbook.price }}.
    2. We will fill out this notebook together in class for extra credit.
    3. Only the {{ site.data.info.textbook.edition }} will be accepted for extra credit (no previous versions).
* **Required Calculator:** Any non-programmable calculator is accepted (no phones, graphing calculators, etc.) I recommend <b><a href="{{ site.data.info.calculator }}" target="\_blank">this one!</a></b>
* **Optional iClicker for in-person section:** Each day in class, a few iClicker questions will be asked and you can get extra credit for them.<br>
\*Online class - do not buy an iClicker, you'll get extra credit points in other ways (see bonus points).

## Class Times
<ul>
{% for class in site.data.info.classes %}
  <li>
    <b>{{ class.type }} {{ class.name }}:</b> {{ class.time }} {{ class.place }}
  </li>
{% endfor %}
</ul>

## Office Hours
* <b>{{ site.short-title }} Office Hours in {{ site.data.info.office-hours.room }} <a href="{{ site.data.info.office-hours.map }}" target="\_blank">{{ site.data.info.office-hours.building }}</a>:</b> {{ site.data.info.office-hours.days }} from {{ site.data.info.office-hours.times }}
* This room is a computer lab where you can come to ask questions, get help from the instructors and CAs, or do your homework. Feel free to stop by anytime If you are unavailable during these times and want to meet, send us an email and we will set up a time!

## Technical Issues
* If you experience a glitch in Lon Capa/Compass, first, try logging out and logging back in. If this doesn't work, send an email to our tech doc, {{ site.data.info.technical.name }} <b><a href="mailto:{{ site.data.info.technical.email }}">{{ site.data.info.technical.email }}</a></b> describing the problem. Please make sure to include a screenshot of the error in your e-mail. You can also stop by office hours and get help in person!

## Homework Schedule
* Homework is due {{ site.data.info.hw-duedates }} (see <b><a href="{{ site.baseurl }}/pages/calendar.html">calendar</a></b>) on <b><a href="http://www.lon-capa.illinois.edu/" target="\_blank">Lon-Capa</a></b>. You can ask questions on the Lon Capa discussion boards and stop by office hours any time to get homework help!
* <b style="color:red;">We do NOT accept late hw, but we do drop your 3 lowest HW scores. This means you can miss 3 HW assignments without any penalty!</b>

## Exam Schedule
* There will be 3 evening exams and a cumulative final. See the <b><a href="{{ site.baseurl }}/pages/exams.html">Exam Schedule</a></b> for dates, times, and locations.

## Grade for Required Work

* **Grade for required work**
  1. 3 Exams: 60% (each worth 20%)
  2. Homework: 15%
  3. Final Exam: 25%{% if site.data.info.grade-calc == "T" %}
  4. [Click here for a grade calculator](http://www.stat.illinois.edu/courses/stat100/computegrade.html)
{% endif %}



**Overall Grade is Translated into a Letter Grade as follows:**

{% include grade.html %}

## Bonus Work
**Bonus Points — You may earn between 0 and 100 Bonus Points.**
* **Everyone may earn between 0 and 100 Bonus Points.** Every bonus point earned helps your overall grade, but even if you do no bonus work, you can still get 100% for the course. In other words, bonus points can only help you. Bonus points are extra credit.
* **IN PERSON CLASS ({% assign in_person = site.data.info.classes | where: 'type', 'In Person Section' %}{% if in_person.size == 2 %}{% for class in in_person %}{% if class == in_person.first %}{{ class.name }} & {% else %}{{ class.name }}{% endif %}{% endfor %}{% elsif in_person.size > 2 %}{% for class in in_person %}{% if class == in_person.first %}{{ class.name }}{% elsif class == in_person.last %} & {{ class.name }}{% else %}, {{ class.name }}{% endif %}{% endfor %}{% else %}{% for class in in_person %}{{ class.name }}{% endfor %}{% endif %}) Bonus Points (100 total bonus points)**
  1. **Pre-Lecture bonus points**--20 bonus points
  2. **iClickers**--30 bonus points
  3. **Lon Capa Surveys**--20 bonus points
  4. **Completed Notebook**--30 bonus points
* **ONLINE CLASSES ({% assign online = site.data.info.classes | where: 'type', 'Online Section' %}{% if online.size == 2 %}{% for class in online %}{% if class == online.first %}{{ class.name }} & {% else %}{{ class.name }}{% endif %}{% endfor %}{% elsif online.size > 2 %}{% for class in online %}{% if class == online.first %}{{ class.name }}{% elsif class == online.last %} & {{ class.name }}{% else %}, {{ class.name }}{% endif %}{% endfor %}{% else %}{% for class in online %}{{ class.name }}{% endfor %}{% endif %}) Bonus Points (100 total bonus points)**
  1. **Pre-Lecture bonus points**--40 bonus points
  2. **Lon Capa Surveys**--20 bonus points
  3. **Completed Notebook**--40 bonus points
* <b><u>Descriptions</u></b>
  1. **Pre-Lecture bonus points**<br>
  Each class there will be a short pre-lecture videos posted on Lon Capa followed by a few questions. The pre-lectures are designed to give you a preview of the basic concepts you'll see in the actual lectures.
  2. **Lon Capa Surveys**<br>
  There will be 5 surveys due on the first Friday of each month (see the course calendar). Each survey is worth 4 bonus points. The surveys are all anonymous. Lon Capa just records whether or not you submitted a survey, not who submitted which answer. You must answer every question on the survey to get the 4 points.
  3. **Completed Notebook**<br>
  We will look over your notebook at the final. You'll get full credit if you have all the pages from lecture filled in. You may skip ALL the practice exams and summary pages. If you're missing more than 3 required pages don't bother to turn in the notebook because you will receive negative bonus points. You may pick up your notebook at the end of your exam to keep forever.
  4. **iClickers (in person class only!)**<br>
  iClicker questions will be asked each day in class. You will get 1 bonus point per class period if you answer all of the iClicker questions. You can skip 2 days and still get full iClicker points.
  5. <b><u>* Bonus points can only help you.</u> You can still get 100% in this class without doing any bonus work.</b>
* **Bonus points are figured into your grade as follows:**
<img src="{{ site.baseurl }}/assets/img/BonusGrade.png" style="width:100%;">
  * Suppose at the end of the semester you have a 75% average and you did 100% of the bonus work.
<img src="{{ site.baseurl }}/assets/img/BonusExample.png" style="width:100%;">
  * So your grade would be raised from a **75% (C) to an 80% (B-)**.

## Course Outline
* **Study Design**: observational studies vs. randomized experiments, why randomized controls are key, confounders in observational studies, Simpson's paradox, intent to treat analysis, etc.
* **Descriptive Statistics**: mean, median, SD, histograms, box plots, normal curve, etc.
* **Linear Regression**: correlation coefficient, simple linear regression, the RMSE, etc.
* **Probability**: chance, multiplication rule, addition rule, conditional probability, Bayes rule, etc.
* **Statistics for Random Variables**: expected value and standard error of chance processes, probability histograms and the Central Limit Theorem, developing simple chance models box models that more complicated sampling processes can be translated into, the Law of Averages, etc.
* **Sampling and Statistical Inference**: using sample means and percents to estimate population means and proportions, attaching margins of errors to our estimates by computing confidence intervals, why randomized sampling is key, etc.
* **Significance Tests**: one sample and two sample z-tests, t-tests, and chi-square tests for goodness of fit and independence, the focus is on understanding how these tests depend on chance models.
* **Limits of Significance Tests**: understanding what the p-value means and under what circumstances it is valid (for example, hypotheses must be stated before looking at the data, the total number of experiments before significant results were found must be reported, etc.)

## LON-CAPA Site
* <b><a href="http://www.lon-capa.uiuc.edu" target="\_blank">http://www.lon-capa.uiuc.edu</a></b><br>
All homework and bonus work is submitted and graded immediately on Lon Capa.

## Compass Site
* <b><a href="https://compass2g.illinois.edu" target="\_blank">https://compass2g.illinois.edu</a></b><br>
We're using Compass 2g to post announcements and display grades.<br>
(Lon Capa's gradebook is too confusing, so check your grades on Compass.)

## Academic Integrity
* If you cheat on an exam in this class you're very likely to get caught and the consequences will be <b>SEVERE</b>. See the <b><a href="https://studentcode.illinois.edu/" target="\_blank">University Student Code of Conduct</a></b>.
* The Stat 100 Team has a group of highly trained students who know every trick in the book for catching cheaters. We hand grade each of the exams and have multiple versions of all exams. They may look identical at first glance, but they are not. Bottom line is, please don't cheat. It's not worth risking your entire college career and you will get caught. If you are caught, you will get a 0 on the exam and be reported to the university.

## Accommodations
* I am happy to offer accommodations for disabilities verified through DRES (<b><a href="http://www.disability.illinois.edu/" target="\_blank">http://www.disability.illinois.edu/</a></b>). Please email me a copy of your letter during week 1. Students taking their exams at DRES can take them anytime on Wed. or Thurs. during exam weeks. Students taking their final exam at DRES can take them any time during finals week.
