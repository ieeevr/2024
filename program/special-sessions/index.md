---
layout: ieeevr-default
title: "Special Sessions"
subtitle: "IEEE VR 2024"
title_separator: "|"
---

<h1>Special Sessions</h1>
<div>
    <table class="styled-table">
        <tr>
            <th colspan="2">&nbsp;</th>
        </tr>
        {% for special-session in site.data.specialsessions %}
            <tr>            
                <td><a href="#{{ special-session.id }}">{{ special-session.title }}</a></td>
                <td style="font-size: 0.875em;">{{ special-session.day }}, {{ special-session.start }} - {{ special-session.end }} ({{ special-session.timezone }})<br>Room: {{ special-session.room }}</td>
            </tr>
        {% endfor %}
    </table>
</div>
<div>
{% for special-session in site.data.specialsessions %}
    <br />
    <div id="{{ special-session.id }}">
        <div style="padding-bottom:10px;"><center><strong><big>{{ special-session.title }}</big></strong></center></div>
        <center>{{ special-session.moderator }}</center>    
        <center><small>{{ special-session.day }}, {{ special-session.start }} - {{ special-session.end }} ({{ special-session.timezone }})<br>Room: {{ special-session.room }}</small></center>    
        <p>
            <strong>Session Topic</strong><br />
            {{ special-session.topic }}
        </p> 
        {% if forloop.last == false %} 
            <hr>
        {% endif %}
    </div>
{% endfor %}
</div>

