---
layout: ieeevr-default
title: "Keynote Speakers"
---

<h1>Keynote Speakers</h1>
<div>
    <table class="styled-table">
        <tr>
            <th colspan="3">Speakers</th>
        </tr>
        {% for keynote in site.data.keynotes %}
        <tr>
            <td><a href="#{{ keynote.id }}"><img src="{{ keynote.thumbnail }}" alt="Photo of {{ keynote.name }}"></a></td>
            <td><a href="#{{ keynote.id }}">{{ keynote.name }}</a></td>
            <td style="font-size: 0.875em;">{{ keynote.day }} - {{ keynote.start }} ({{ keynote.timezone }})</td>
        </tr>
        {% endfor %}
    </table>
</div>
{% for keynote in site.data.keynotes %}
<br />
<div id="{{ keynote.id }}">
    <center><strong><big>{{ keynote.name }}</big></strong></center>
    <center>{{ keynote.affiliation }}</center>
    <br />
    <center><img src="{{ keynote.photo }}" alt="Photo of {{ keynote.name }}" width="50%"></center>
    <br />
    <center><big><strong>{{ keynote.title }}</strong></big></center>
    <center><small>{{ keynote.day }} - {{ keynote.start }}, {{ keynote.timezone }}</small></center>
    {% if keynote.chair %}
    <center><small>Session Chair: <b style="font-family: 'Courier New', monospace; color: black;">{{ keynote.chair }}</b></small></center>
    {% endif %}
    <!-- TAKE ME TO THE EVENT START -->
    {% for event in site.data.events %}
    {% if event.id == keynote.id %}
    {% if event.location %}
    <div id="{{ keynote.id }}-program" class="notice--info">
        <strong style="padding-bottom: 5px;">Take me to the event:</strong>
        <p>
            <strong style="color: black;">Virbela Location:</strong> {{ event.location }} (<a href="/2021/attend/virbela-instructions/#map">MAP</a>)
            {% if event.stream-url %}
            <br />
            {% if event.aindanaoaconteceu %}
            <strong style="color: black;">Watch video stream live:</strong> <a href="{{ event.stream-url }}" target="_blank">HERE</a>
            {% else %}
            <strong style="color: black;">Watch the recorded video stream:</strong> <a href="{{ event.stream-url }}" target="_blank">HERE</a>
            {% endif %}
            {% endif %}
            {% if event.discordurl %}
            <br />
            <strong style="color: black;">Discord Channel:</strong> <a href="https://{{ event.discordurl }}" target="_blank">Open in Browser</a>, <a href="discord://{{ event.discordurl }}">Open in App</a> (Participants only)
            {% endif %}
            {% endif %}
        </p>
    </div>
    {% endif %}
    {% endfor %}
    <!-- TAKE ME TO THE EVENT END-->
    <p>
        <strong>Abstract</strong><br />
        {{ keynote.abstract }}
    </p>
    <p>
        <strong>Bio</strong><br />
        {{ keynote.bio }}
    </p>
    <hr>
</div>
{% endfor %}

