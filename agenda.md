---
layout: page
sidebar: true
icon: fa fa-calendar
order: 2
title: Agenda
---

## Tuesday, Sep 2nd, 2025

<table>
<tr>
<th>Time (CEST)</th><th>Type</th><th>Speaker</th><th>Title</th>
</tr>

{% for talk in site.data.speakers %}
<tr>
<td rowspan="2">{{ talk.time }}</td>
<td rowspan="2">{{ talk.type }}</td>
<td><strong>{{ talk.name }}</strong>{% if talk.affiliation %}, <em>{{ talk.affiliation }}</em>{% endif %}</td>
<td>{{ talk.title }}</td>
</tr>
<tr>
<td colspan="2"> 

{% if talk.desc %}
<em>Abstract:</em> <small>{{ talk.desc | markdownify }}</small>
{% endif %}

{% if talk.bio %}
<em>Bio:</em> <small>{{ talk.bio | markdownify }}</small>
{% endif %}

</td>
</tr>
{% endfor %}




</table>