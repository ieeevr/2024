---
layout: ieeevr-default
title: "Workshop Program"
subtitle: "IEEE VR 2024"
title_separator: "|"
---

<link rel="stylesheet" href="{{ '/assets/css/tableStyles.css' | relative_url }}">

<!-- <div>
    <p>
        More information coming soon, please watch this space.
    </p>
</div> -->

<div>
    <h1 id="call-for-workshop-papers"> Workshops </h1>
    <!-- <p>
        IEEE VR 2024 seeks high-quality contributions to the following 18 workshops. 
        For more details, see each workshop's Call for Papers below.
    </p> -->
    <table class="styled-table">
        <tr>
            <th>Workshops</th>
        </tr>
        {% for workshop in site.data.workshops %}
        <tr>
            <td style="font-size: 0.9em;"><a href="#{{ workshop.id }}">{{ workshop.title }}</a></td>
        </tr>
        {% endfor %}
    </table>

<div>
    {% for workshop in site.data.workshops %}
            <!-- Workshop title matter -->
            <h2 id="{{ workshop.id }}">Workshop: {{ workshop.title }}</h2>
            <!-- <p><strong>{{ workshop.day }}, {{ workshop.starttime }}, {{ workshop.timezone }}</strong></p> -->
            {% if workshop.organiser %}
                <p><small><b style="color: black;">Principal Organiser:</b> {{ workshop.organiser }}</small></p>
            {% endif %}
            {% if workshop.videourl %}
                <div class="video-container">
                    <iframe src="{{workshop.videourl}}" title="YouTube video player" frameborder="0" 
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                </div>
            {% endif %}
            <p>
            {% if workshop.url %}
                <small><b style="color: black;">Website:</b> <a href="{{ workshop.url }}" target="_blank">{{ workshop.url }}</a></small>
            {% endif %}
            {% if workshop.discordurl %}
                <p><small><b style="color: black;">Discord URL:</b> <a href="{{ workshop.discordurl }}" target="_blank">{{ workshop.discordurl }}</a></small>
            {% endif %}
            {% if workshop.slideurl %}
                <p><small><b style="color: black;">Slides:</b> <a href="{{ workshop.discordurl }}" target="_blank">{{ workshop.slideurl }}</a></small>
            {% endif %}
            </p>
            {% if workshop.abstract %}
                <div id="{{ workshop.id }}" class="wrap-collabsible"> <input id="collapsible{{ workshop.id }}" class="toggle" type="checkbox"> <label for="collapsible{{ workshop.id }}" class="lbl-toggle">Workshop Description</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ workshop.abstract }}</p>
                        </div>
                    </div>
                </div>
            {% endif %}
            <!-- TAKE ME TO THE EVENT START -->
            <!--{% for event in site.data.events %}
                {% if event.id == workshop.id %}
                    {% if event.location %}
                    <div class="notice--info">
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
                        </p>
                    </div>
                    {% endif %}
                {% endif %}
            {% endfor %}-->
            <!-- TAKE ME TO THE EVENT END-->
            <!-- Only show the 'workshop papers' toggle if there's actually something to show -->
            {% assign papers_in_session = false %}
            {% for paper in site.data.workshoppapers %}
                {% if workshop.id == paper.workshop %}
                    {% assign papers_in_session = true %}
                {% endif %}
            {% endfor %}
            <!-- Show a hideable list of all papers in this workshop -->
            {% if papers_in_session == true %}
            <div id="{{ workshop.id }}2" class="wrap-collabsible"> <input id="collapsible{{ workshop.id }}2" class="toggle" type="checkbox"> <label for="collapsible{{ workshop.id }}2" class="lbl-toggle">Workshop Papers</label>
                <div class="collapsible-content">
                    <div class="content-inner">
                        {% for paper in site.data.workshoppapers %}
                            {% if workshop.id == paper.workshop %}
                                <h4 id="{{ paper.id }}">{{ paper.title }}</h4>
                                {% if paper.authors %}
                                    <p><i>{{ paper.authors }}</i></p>
                                {% else %}
                                    <p><i>Author information coming soon</i></p>
                                {% endif %}
                                {% if paper.url %}
                                    <p><small>URL: <a href="{{ paper.url }}" target="_blank">{{ paper.url }}</a></small></p>
                                {% endif %}
                                {% if paper.abstract %}
                                    <div id="{{ paper.id }}" class="wrap-collabsible"> <input id="collapsible{{ paper.id }}" class="toggle" type="checkbox"> <label for="collapsible{{ paper.id }}" class="lbl-toggle">Abstract</label>
                                        <div class="collapsible-content">
                                            <div class="content-inner">
                                                <p>{{ paper.abstract }}</p>
                                            </div>
                                        </div>
                                    </div>
                                {% endif %}
                            {% endif %}
                        {% endfor %}
                    </div>
                </div>
            </div>
            {% endif %}
    {% endfor %}
</div>
</div> 