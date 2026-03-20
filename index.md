---
layout: default
title: プロジェクト報告一覧
---

# プロジェクト報告書

| 日付 | 種別 | タイトル | ステータス | 概要 |
| :--- | :--- | :--- | :--- | :--- |
{% for report in site.data.reports %}
| {{ report.date }} | {{ report.type }} | {{ report.title }} | {{ report.status }} | {{ report.summary }} |
{% endfor %}
