---
layout: ieeevr-default
title: "Papers"
---

<link rel="stylesheet" href="{{ '/assets/css/tableStyles.css' | relative_url }}">

<h1>Papers -- Tentative Program</h1>

<div>
    <table class="styled-table" style="font-size: 0.9em; ">
        <tr>
            <th>Monday, March 27, 2024, Shanghai UTC+8</th>
            <th></th>
        </tr>
        {% for session in site.data.sessions %}
        {% if session.day == 'Monday, March 27, 2024' %}
        <tr>
            <td style="font-size: 0.9em;"><a href="#{{ session.id }}">{{ session.name }}</a></td>
            <td>{{ session.starttime }} - {{ session.endtime }}</td>
            <td>{{ session.room }}</td>
        </tr>
        {% endif %}
        {% endfor %}
    </table>
</div>
<div>
    <table class="styled-table" style="font-size: 0.9em; ">
        <tr>
            <th>Tuesday, March 28, 2024, Shanghai UTC+8</th>
            <th></th>
        </tr>
        {% for session in site.data.sessions %}
        {% if session.day == 'Tuesday, March 28, 2024' %}
        <tr>
            <td style="font-size: 0.9em;"><a href="#{{ session.id }}">{{ session.name }}</a></td>
            <td>{{ session.starttime }} - {{ session.endtime }}</td>
            <td>{{ session.room }}</td>
        </tr>
        {% endif %}
        {% endfor %}
    </table>
</div>
<div>
    <table class="styled-table" style="font-size: 0.9em; ">
        <tr>
            <th>Wednesday, March 29, 2024, Shanghai UTC+8</th>
            <th></th>
        </tr>
        {% for session in site.data.sessions %}
        {% if session.day == 'Wednesday, March 29, 2024' %}
        <tr>
            <td style="font-size: 0.9em;"><a href="#{{ session.id }}">{{ session.name }}</a></td>
            <td>{{ session.starttime }} - {{ session.endtime }}</td>
            <td>{{ session.room }}</td>
        </tr>
        {% endif %}
        {% endfor %}
    </table>
</div>

<!-- 
INVITED MISSING
-->


{% for day in site.data.days %}
<div>
    {% for session in site.data.sessions %}
    {% if session.day == day.day' %}
    <h2 id="{{ session.id }}">Session: {{ session.name }}</h2>
    <p><strong>{{ session.day }}, {{ session.starttime }}, {{ session.timezone }}, {{ session.room }}</strong></p>
    {% if session.sessionchair %}
    <p><small>Session Chair: <b style="font-family: 'Courier New', monospace; color: black;">{{ session.sessionchair }}</b></small></p>
    {% endif %}
   
    {% for paper in site.data.papers %}
    {% if session.id == paper.session %}
    <h4 id="{{ paper.id }}">{{ paper.title }}</h4>
    <p><strong><small>{{ paper.type }}</small></strong></p>
    {% if paper.type == 'Journal' %}
    {% assign source = site.data.journalpapers %}
    {% endif %}
    {% if paper.type == 'Conference' %}
    {% assign source = site.data.conferencepapers %}
    {% endif %}
    {% if paper.type == 'Invited Journal' %}
    {% assign source = site.data.invitedjournalpapers %}
    {% endif %}
    {% for p in source %}
    {% if p.id == paper.id %}
    {% assign authornames = p.authors | split: ";" %}
    <p><i>
    {% for name in authornames %}
    {% assign barename = name | split: ":" %}
    {% if name == authornames.last %}
    {{ barename.first | strip }}
    {% else %}
    {{ barename.first | strip }}, 
    {% endif %}
    {% endfor %}
    </i></p>
    <div id="{{ paper.id }}" class="wrap-collabsible"> <input id="collapsible{{ paper.id }}" class="toggle" type="checkbox"> <label for="collapsible{{ paper.id }}" class="lbl-toggle">Abstract</label>
        <div class="collapsible-content">
            <div class="content-inner">
                <p>{{ p.abstract }}</p>
            </div>
        </div>
    </div>
    {% endif %}
    {% endfor %}

    {% endif %}
    {% endfor %}

    {% endif %}
    {% endfor %}
</div>
{% endfor %}




<!--
<div id="S1">
    {% for session in site.data.sessions %}
    {% if session.id == 'S1' %}
    <h2>{{ session.name }}: {{ session.title }}</h2>
    {% endif %}
    {% endfor %}

    {% for paper in site.data.papers %}
    {% if paper.session == 'S1' %}

    <div>
        {% for demo in site.data.demos %}

        <h3 id="{{ paper.id }}">{{ paper.title }}</h3>
        <p><i>{{ paper.authors }}</i></p>
        <div id="{{ paper.id }}" class="wrap-collabsible"> <input id="collapsible{{ paper.id }}" class="toggle" type="checkbox"> <label for="collapsible{{ paper.id }}" class="lbl-toggle">Abstract</label>
            <div class="collapsible-content">
                <div class="content-inner">
                    <p>{{ paper.abstract }}</p>
                </div>
            </div>
        </div>
        {% endfor %}
    </div>

    {% endif %}
    {% endfor %}
</div>
-->
