---
layout: home
title: Home
nav_order: 1
description: A week-to-week description of the content covered in the course.
seo:
  type: Course
  name: Data 140
---

{: .warning }
⚠️ The content on this site is archived and retained exclusively for reference. Updates will be made when the course is offered in the future.


# Data 140: Probability for Data Science
UC Berkeley, Spring 2026
{: .mb-0 .fs-6 .text-grey-dk-000 }

{%- if site.enable_announcements -%}

    {% assign announcement = site.announcements | last %}
    {{ announcement }}
{%- endif -%}

# Calendar

<div>
{%- include schedule.html -%}
</div>
