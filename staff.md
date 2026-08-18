---
layout: page
title: Staff
nav_order: 3
description: A listing of all the course staff members.
---

# Staff

Append `@berkeley.edu` to all email addresses. **For personal circumstances or sensitive matters,** please use the staff email address **[data140@berkeley.edu](mailto:data140@berkeley.edu)**, which is monitored only by the professor and a few TAs.

{% assign professors = site.staffers | where: 'role', 'Professor' | reverse %}
{% assign num_professors = professors | size %}
{% if num_professors != 0 %}
## Professors

<div class = "role flex">
    {% for staffer in professors %}
    {{ staffer }}
    {% endfor %}
</div>
{% endif %}
    
{% assign instructors = site.staffers | where: 'role', 'Instructor' | reverse %}
{% assign num_instructors = instructors | size %}
{% if num_instructors != 0 %}
## Instructors

{% for staffer in instructors %}
{{ staffer }}
{% endfor %}
{% endif %}

{% assign staff = site.staffers | where: 'team', 'Staff' %}
{% assign num_staff = staff | size %}
{% if num_staff != 0 %}
## Course Staff

<div class = "role flex">
    {% for staffer in staff %}
    {{ staffer }}
    {% endfor %}
</div>
{% endif %}

