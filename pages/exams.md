---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: content
title: Exams
---

# {{ site.short-title}} Exam Schedule {{ site.semester }}
##### <b style="color:red;">Important Info:</b> There will be three midterm exams and a comprehensive final exam. There will be NO makeup exams and NO formula sheets may be used on any exam. If you miss an exam and have written proof of a valid reason, then we will substitute your final exam score for the missed exam.

{% for exam in site.data.info.exams %}
##  {{ site.short-title }} {{ exam.name }}
##### **Date:** {{ exam.date }}
##### **Time:** {{ exam.time }}
##### **Covers:** {{ exam.content }}
##### **Locations:** {{ exam.locations }}
{% if exam.show-schedule == "T" %}
{% include {{ exam.base-name }}-schedule.html %}
{% endif %}
##### **Conflict Exam:** {{ exam.conflict }}
{% endfor %}
