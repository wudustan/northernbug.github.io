---
layout: page
title: Meetings
permalink: /meetings/
---


# Future Meetings

<table>
<thead>
<th>Meeting</th>
<th>Theme</th>
<th>Date</th>
<th>Institute</th>
<th>City</th>
</thead>
{% for meeting in site.data.meetings %}
{% if meeting.day == 'TBD' %}
{% capture day %}1{% endcapture %}
{% else %}
{% capture day %}{{meeting.day}}{% endcapture %}
{% endif %}
{% capture event_date %}{{ meeting.year }}-{{ meeting.month }}-{{day}} {% endcapture %}
{% capture current_date %}{{ site.time | date: '%Y-%B-%d' }}{% endcapture %}
{% if event_date > current_date %}
<tr>
<td>{{ meeting.meeting }}</td>
<td>{{ meeting.theme }}</td>
<td>{{ meeting.day }} {{ meeting.month }} {{ meeting.year }}</td>
<td>{{ meeting.institute }}</td>
<td>{{ meeting.city }}</td>
</tr>
{% endif %}
{% endfor %}
</table>

# Past Meetings

<table>
<thead>
<th>Meeting</th>
<th>Theme</th>
<th>Date</th>
<th>Institute</th>
<th>City</th>
</thead>
{% for meeting in site.data.meetings %}
{% if meeting.day == 'TBD' %}
{% capture day %}1{% endcapture %}
{% else %}
{% capture day %}{{meeting.day}}{% endcapture %}
{% endif %}
{% capture event_date %}{{ meeting.year }}-{{ meeting.month }}-{{day}} {% endcapture %}
{% capture current_date %}{{ site.time | date: '%Y-%B-%d' }}{% endcapture %}
{% if event_date < current_date %}
<tr>
<td>{{ meeting.meeting }}</td>
<td>{{ meeting.theme }}</td>
<td>{{ meeting.day }} {{ meeting.month }} {{ meeting.year }}</td>
<td>{{ meeting.institute }}</td>
<td>{{ meeting.city }}</td>
</tr>
{% endif %}
{% endfor %}
</table>
