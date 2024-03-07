---
layout: ieeevr-default
title: "Papers"
subtitle: "IEEE VR 2024"
title_separator: "|"
---
<h1>Papers</h1>
<div>
    {% for day in site.data.days %}
        <div>
            <div>
                <table class="styled-table">
                    <tr>
                        <th colspan="4">{{ day.day }} (Timezone: {{ day.timezone }})</th>
                    </tr>
                    {% for session in site.data.sessions %}
                        {% if session.day == day.day %}
                            <tr>
                                <td class="medLarge"><a href="#{{ session.id }}">{{ session.id }}</a></td>
                                <td class="medLarge"><a href="#{{ session.id }}">{{ session.name }}</a></td>
                                <td class="medLarge">{{ session.starttime }}&#8209;{{ session.endtime }}</td>
                                <td class="medLarge" class="text-nowrap">{{ session.room }}</td>
                            </tr>
                        {% endif %}
                    {% endfor %}
                </table>
            </div>
        <div>
    {% endfor %} 
</div>

<div>
     {% for day in site.data.days %}
        <div>
            {% for session in site.data.sessions %}
                {% if session.day == day.day %}
                    <h2 id="{{ session.id }}" class="pink" style="padding-top:25px;">Session: {{ session.name }} ({{ session.id }})</h2>
                    <p class="small">{{ session.day }}, {{ session.starttime }}-{{ session.endtime }} ({{ session.timezone }}), Room: {{ session.room }}</p>
                    {% if session.sessionchair %}
                        <p><small>Session Chair: <b style="font-family: 'Courier New', monospace; color: black;">{{ session.sessionchair }}</b></small></p>
                    {% endif %}    
                        {% for paper in site.data.papers %}                
                            {% if session.id == paper.session %}                            
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
                                        <p id="{{ paper.id }}" style="margin-bottom: 0.3em;">
                                            <strong>{{ paper.type }}: <i>{{ paper.title }} (ID: {{ paper.id }})</i></strong>
                                        </p>
                                        <p class="small" style="margin-left: 25px;">
                                            {% assign authornames = p.authors | split: ";" %}
                                            {% for name in authornames %}
                                                {% assign barename = name | split: ":" %}
                                                {% for n in barename %}
                                                    {% if n == barename.last %}
                                                        <i>{{ n | strip }}{% if name == authornames.last %}{% else %};{% endif %}</i>
                                                    {% else %}                            
                                                        <span class="bold">{{ n | strip }},</span>
                                                    {% endif %}
                                                {% endfor %} 
                                            {% endfor %}
                                        </p>
                                        {% if p.abstract %}
                                            <div id="{{ paper.id }}" class="wrap-collabsible"  style="margin-left: 25px;"> <input id="collapsible{{ paper.id }}" class="toggle" type="checkbox"> 
                                                <label for="collapsible{{ paper.id }}" class="lbl-toggle">Abstract</label>
                                                <div class="collapsible-content">
                                                    <div class="content-inner">
                                                        <p>{{ p.abstract }}</p>
                                                    </div>
                                                </div>
                                            </div>                                                                     
                                        {% endif %}
                                    {% endif %}
                                {% endfor %}
                            {% endif %}
                        {% endfor %}
                {% endif %}
            {% endfor %}
        </div>
    {% endfor %}
</div>
