---
layout: ieeevr-default
title: "Reviewers"
subtitle: "IEEE VR 2024"
title_separator: "|"
---

<link rel="stylesheet" href="{{ '/assets/css/tableStyles.css' | relative_url }}">

<div>
    <h1> IEEE VR 2024 Reviewers for Papers </h1>
    <table class="styled-table" style="font-size: 0.8em; ">
    {% tablerow reviewer in site.data.reviewers cols:3 %}
        {{ reviewer.name }}{%if reviewer.affiliation %} - <i>{{ reviewer.affiliation }}</i>{% endif %}
    {% endtablerow %}
</table>
</div>
