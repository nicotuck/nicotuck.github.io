---
layout: default
title: Projects
description: Making things, breaking things, just for me.
permalink: /projects/
usemathjax: true
---
# List of Projects
Some of my personal projects

<html>
{%- for project in site.projects -%}
    {%- assign item = project -%}  
    {%- include item-card-h.html item=item -%}  
{%- endfor -%}
</html>