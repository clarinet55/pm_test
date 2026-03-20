---
layout: default
title: プロジェクト報告一覧
---

# プロジェクト報告書

<table style="width: 100%; border-collapse: collapse; margin-top: 20px;">
  <thead>
    <tr style="background-color: #f2f2f2;">
      <th style="border: 1px solid #ddd; padding: 8px;">日付</th>
      <th style="border: 1px solid #ddd; padding: 8px;">種別</th>
      <th style="border: 1px solid #ddd; padding: 8px;">タイトル</th>
      <th style="border: 1px solid #ddd; padding: 8px;">ステータス</th>
      <th style="border: 1px solid #ddd; padding: 8px;">概要</th>
    </tr>
  </thead>
  <tbody>
    {% for report in site.data.reports %}
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">{{ report.date }}</td>
      <td style="border: 1px solid #ddd; padding: 8px;">{{ report.type }}</td>
      <td style="border: 1px solid #ddd; padding: 8px;">{{ report.title }}</td>
      <td style="border: 1px solid #ddd; padding: 8px; text-align: center;">
        {% if report.status == "順調" %}
          <span style="color: green; font-weight: bold;">{{ report.status }}</span>
        {% elif report.status == "一部遅延" %}
          <span style="color: orange; font-weight: bold;">{{ report.status }}</span>
        {% else %}
          {{ report.status }}
        {% endif %}
      </td>
      <td style="border: 1px solid #ddd; padding: 8px;">{{ report.summary }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>
