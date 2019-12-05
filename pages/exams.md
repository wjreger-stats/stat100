---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: content
title: Exams
---

# {{ site.short-title}} Exam Schedule {{ site.semester }}
##### <b style="color:red;">Important Info:</b> There will be three midterm exams and a comprehensive final exam. There will be NO makeup exams and NO formula sheets may be used on any exam. If you miss an exam and have written proof of a valid reason, then we will substitute your final exam score for the missed exam.

**Exam schedule section is under repair at this time**

{% for exam in site.data.info.exams %}
##  {{ site.short-title }} {{ exam.name }}
##### **Date:** {{ exam.date }}
##### **Time:** {{ exam.time }}
##### **Covers:** {{ exam.content }}
##### **Locations:** {{ exam.locations }}
{% if exam.base-name == 'Exam1' %}
{% include Exam1-schedule.html %}
{% endfor %}
##### **Conflict Exam:** {{ exam.conflict }}
{% endfor %}

## Final Exam

* I use the final exam time assigned to our class by the university.<br>
* See <b><a href="{{ site.data.info.uiucfinals }}" target="\_blank">Official University Final Exams Schedules and Policies</a></b>.<br>
* The final cumulative for Chapters 1-24 <b>(ALL chapters in notebook)</b><br>

{% include final-schedule.html %}

# Practice Exams from Past Semesters

{% include practice-exams.html %}

## Final Exams
<p style="color:red;">***Warning***
None of the practice finals have box plot questions.
There WILL be some on the final! Please study accordingly.
You can practice box plots by doing the practice homework on box plots.
There are also box plot questions on all exam 2 practice exams.</p>

{% include practice-finals.html %}
