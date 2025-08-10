---
layout: default
title: Playwright Reports
---

# Playwright Test Reports

<table>
  <thead>
    <tr>
      <th>Date</th>
      <th>Passed</th>
      <th>Failed</th>
      <th>Total</th>
      <th>Link</th>
    </tr>
  </thead>
  <tbody>
  {% for run in site.data.runs reversed %}
    <tr {% if run.failed > 0 %}style="background-color:#ffe5e5"{% endif %}>
      <td>{{ run.date }}</td>
      <td style="color:green">{{ run.passed }}</td>
      <td style="color:red">{{ run.failed }}</td>
      <td>{{ run.total }}</td>
      <td><a href="{{ run.link }}">Run #{{ run.run }}</a></td>
    </tr>
  {% endfor %}
  </tbody>
</table>
