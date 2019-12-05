---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: content
title: Exams
---

<h1>{{ site.short-title}} Exam Schedule {{ site.semester }}</h1>
<h4><b style="color:red;">Important Info:</b> There will be three midterm exams and a comprehensive final exam. There will be NO makeup exams and NO formula sheets may be used on any exam. If you miss an exam and have written proof of a valid reason, then we will substitute your final exam score for the missed exam.<h4>

{% for exam in site.data.info.exams %}
<h2>{{ site.short-title }} {{ exam.name }}</h2>
<h4><b>Date: {{ exam.date }}</b></h4>
<h4><b>Time: {{ exam.time }}</b></h4>
<h4><b>Covers: {{ exam.content }}</b></h4>
<h4><b>Locations: {{ exam.locations }}</b></h4>
{% if exam.base-name == 'Exam1' %}
{% include Exam1-schedule.html %}
{% endif %}
<h4><b>Conflict Exam: {{ exam.conflict }}</b></h4>
{% endfor %}

<h2>Final Exam</h2>
<ul>
<li>
 I use the final exam time assigned to our class by the university.<br>
</li>
<li>
See <b><a href="{{ site.data.info.uiucfinals }}" target="\_blank">Official University Final Exams Schedules and Policies</a></b>.<br>
</li>
<li>
The final cumulative for Chapters 1-24 <b>(ALL chapters in notebook)</b><br>
</li>
</ul>

{% include final-schedule.html %}

<h1>Practice Exams from Past Semesters</h1>

{% include practice-exams.html %}

<h2>Final Exams</h2>
<p style="color:red;">***Warning***
None of the practice finals have box plot questions.
There WILL be some on the final! Please study accordingly.
You can practice box plots by doing the practice homework on box plots.
There are also box plot questions on all exam 2 practice exams.</p>

{% include practice-finals.html %}
