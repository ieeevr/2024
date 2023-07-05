---
layout: ieeevr-default
title: "Conference Award Winners"
---
<link rel="stylesheet" href="{{ '/assets/css/tableStyles.css' | relative_url }}">

<h1>IEEE VR 2024 Conference Awards</h1>

<!-- <p> Awards presented at the annual IEEE VR 2024 are in two categories:</p>
<ul>
    <li>Awards sponsored by the Visualization and Graphics Technical Committee of the IEEE Computer
Society, and</li>
    <li>Awards sponsored by the conference itself.</li>
</ul>
    
<p>
    Award winners are selected by various means including people’s choice voting, invited judges, and
formal selection committees. That information is included in the award presentation materials that
follow.
</p> -->
    

<!-- <table class="styled-table" style="font-size: 0.9em; ">
    <tr>
        <th>VGTC Awards</th>
    </tr>
    <tr>
        <td><strong><a href="#journal-best">TVCG - Best Journal Papers</a></strong></td>
    </tr>
    <tr>
        <td><strong><a href="#journal-honorable">TVCG - Honorable Mentions</a></strong></td>
    </tr>
    <tr>
        <td><strong><a href="#journal-nominees">TVCG - Best Journal - Nominees</a></strong></td>
    </tr>
</table> -->

<table class="styled-table" style="font-size: 0.9em; ">
    <tr>
        <th>Papers</th>
    </tr>
    <tr>
        <td><strong><a href="#conference-best">Best Papers</a></strong></td>
    </tr>
    <tr>
        <td><strong><a href="#conference-honorable">Honorable Mentions</a></strong></td>
    </tr>
    <tr>
        <td><strong><a href="#conference-nominees">Nominees</a></strong></td>
    </tr>
    
</table>

<table class="styled-table" style="font-size: 0.9em; ">
    <tr>
        <th>Posters</th>
    </tr>
    <tr>
        <td><strong><a href="#best-poster">Best Poster</a></strong></td>
    </tr>
    <tr>
        <td><strong><a href="#poster-honorable">Honorable Mention</a></strong></td>
    </tr>
    
</table>

<table class="styled-table" style="font-size: 0.9em; ">
    <tr>
        <th>Demos</th>
    </tr>
    <tr>
        <td><strong><a href="#demo-best">Best Demo</a></strong></td>
    </tr>
    <tr>
        <td><strong><a href="#demo-honorable">Honorable Mention</a></strong></td>
    </tr>
</table>

<table class="styled-table" style="font-size: 0.9em; ">
    <tr>
        <th>3DUI Contest</th>
    </tr>
    <tr>
        <td><strong><a href="#3dui-best">Best 3DUI</a></strong></td>
    </tr>
    <tr>
        <td><strong><a href="#3dui-honorable">Honorable Mention</a></strong></td>
    </tr>
</table>

<table class="styled-table" style="font-size: 0.9em; ">
    <tr>
        <th>Doctoral Consortium</th>
    </tr>
    <tr>
        <td><strong><a href="#DC-best">Best Presentation</a></strong></td>
    </tr>
</table>

<table class="styled-table" style="font-size: 0.9em; ">
    <tr>
        <th>Paper Presentation</th>
    </tr>
     <tr>
        <td><strong><a href="#Paper-presentation-best">Best Paper Presentation</a></strong></td>
    </tr>
</table>

<!-- <table class="styled-table" style="font-size: 0.9em; ">
    <tr>
        <th>Ready Player 21</th>
    </tr>
     <tr>
        <td><strong><a href="#ready-player-21">Winner</a></strong></td>
    </tr>
</table> -->


<h2 id='conference-best' class="alignCenter">Best Papers</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == 'Journal' %}
        {% if item.award == 'Best Paper' %}
            {% for j in site.data.journalpapers %}
                {% if j.id == item.id %}
                {% assign authornames = j.authors | split: ";" %}
                <h4 id="JT{{ j.id }}">{{ j.Title }}</h4>
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
                <div id="J{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleJ{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleJ{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
    {% if item.type == 'Conference' %}
        {% if item.award == 'Best Paper' %}
            {% for j in site.data.conferencepapers %}
                {% if j.id == item.id %}
                {% assign authornames = j.authors | split: ";" %}
                <h4 id="CT{{ j.id }}">{{ j.Title }}</h4>
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
                <div id="C{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleC{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleC{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
{% endfor %}
</div>

<h2 id='conference-honorable' class="alignCenter">Paper - Honorable Mentions</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == 'Journal' %}
        {% if item.award == 'Honorable Mention' %}
            {% for j in site.data.journalpapers %}
                {% if j.id == item.id %}
                {% assign authornames = j.authors | split: ";" %}
                <h4 id="JT{{ j.id }}">{{ j.Title }}</h4>
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
                <div id="J{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleJ{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleJ{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
    {% if item.type == 'Conference' %}
        {% if item.award == 'Honorable Mention' %}
            {% for j in site.data.conferencepapers %}
                {% if j.id == item.id %}
                {% assign authornames = j.authors | split: ";" %}
                <h4 id="CT{{ j.id }}">{{ j.Title }}</h4>
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
                <div id="C{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleC{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleC{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
{% endfor %}
</div>

<h2 id='conference-nominees' >Paper - Nominees</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == 'Journal' %}
        {% if item.award == 'Nominee' %}
            {% for j in site.data.journalpapers %}
                {% if j.id == item.id %}
                {% assign authornames = j.authors | split: ";" %}
                <h4 id="JT{{ j.id }}">{{ j.Title }}</h4>
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
                <div id="J{{ j.id }}" class="wrap-collabsible"> <input id="collapsible1J{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsible1J{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
    {% if item.type == 'Conference' %}
        {% if item.award == 'Nominee' %}
            {% for j in site.data.conferencepapers %}
                {% if j.id == item.id %}
                {% assign authornames = j.authors | split: ";" %}
                <h4 id="CT{{ j.id }}">{{ j.Title }}</h4>
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
                <div id="C{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleC{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleC{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
{% endfor %}
</div>

<!-- <h2 id='conference-best' class="alignCenter">Best Conference Papers</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == 'Conference' %}
        {% if item.award == 'Best Paper' %}
            {% for j in site.data.conferencepapers %}
                {% if j.id == item.id %}
                <h4 id="{{ j.id }}">{{ j.Title }}</h4>
                <p><i>{{ j.authors }}</i></p>
                <div id="{{ j.id }}" class="wrap-collabsible"> <input id="collapsible{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsible{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
{% endfor %}
</div> -->

<!-- <h2 id='conference-honorable' class="alignCenter">Conference Papers - Honorable Mentions</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == 'Conference' %}
        {% if item.award == 'Honorable Mention' %}
            {% for j in site.data.conferencepapers %}
                {% if j.id == item.id %}
                <h4 id="{{ j.id }}">{{ j.Title }}</h4>
                <p><i>{{ j.authors }}</i></p>
                <div id="{{ j.id }}" class="wrap-collabsible"> <input id="collapsible{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsible{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
    
        {% endif %}
    {% endif %}
    
{% endfor %}
</div> -->

<!-- <h2 id='conference-nominees' class="alignCenter">Conference Papers - Nominees</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == 'Conference' %}
        {% if item.award == 'Nominee' %}
            {% for j in site.data.conferencepapers %}
                {% if j.id == item.id %}
                <h4 id="{{ j.id }}">{{ j.Title }}</h4>
                <p><i>{{ j.authors }}</i></p>
                <div id="{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleC{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleC{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
{% endfor %}
</div> -->

<h2 id='best-poster' class="alignCenter">Best Poster</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == 'Poster' %}
        {% if item.award == 'Best Poster' %}
            {% for j in site.data.posters %}
                {% if j.id == item.id %}
                <h4 id="P{{ j.id }}">{{ j.title }}</h4>
                <p><i>{{ j.authors }}</i></p>
                <div id="P{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleP{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleP{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
{% endfor %}
</div>

<h2 id='poster-honorable' class="alignCenter">Poster - Honorable Mention</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == 'Poster' %}
        {% if item.award == 'Honorable Mention' %}
            {% for j in site.data.posters %}
                {% if j.id == item.id %}
                <h4 id="P{{ j.id }}">{{ j.title }}</h4>
                <p><i>{{ j.authors }}</i></p>
                <div id="P{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleP{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleP{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
{% endfor %}
</div>

<h2 id='demo-best' class="alignCenter">Best Demo</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == 'Demo' %}
        {% if item.award == 'Best Demo' %}
            {% for j in site.data.demos %}
                {% if j.id == item.id %}
                <h4 id="D{{ j.id }}">{{ j.title }}</h4>
                <p><i>{{ j.authors }}</i></p>
                <div id="D{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleD{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleD{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
{% endfor %}
</div>

<h2 id='demo-honorable' class="alignCenter">Demo - Honorable Mention</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == 'Demo' %}
        {% if item.award == 'Honorable Mention' %}
            {% for j in site.data.demos %}
                {% if j.id == item.id %}
                <h4 id="D{{ j.id }}">{{ j.title }}</h4>
                <p><i>{{ j.authors }}</i></p>
                <div id="D{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleD{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleD{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
{% endfor %}
</div>

<!-- <h2 id='demo-people' class="alignCenter">Demos - People's Choice</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == 'Demo' %}
        {% if item.award == 'Peoples Choice Demo' %}`
            {% for j in site.data.demos %}
                {% if j.id == item.id %}
                <h4 id="{{ j.id }}">{{ j.title }}</h4>
                <p><i>{{ j.authors }}</i></p>
                <div id="{{ j.id }}" class="wrap-collabsible"> <input id="collapsible{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsible{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
{% endfor %}
</div> -->
<h2 id='3dui-best' class="alignCenter">Best 3DUI</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == '3DUI Contest' %}
        {% if item.award == 'Best 3DUI' %}
            {% for j in site.data.3duicontest %}
                {% if j.id == item.id %}
                <h4 id="3dui{{ j.id }}">{{ j.title }}</h4>
                <p><i>{{ j.authors }}</i></p>
                <!-- <div id="3dui{{ j.id }}" class="wrap-collabsible"> <input id="collapsible3dui{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsible3dui{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div> -->
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}    
{% endfor %}
</div>
<h2 id='3dui-honorable' class="alignCenter">3DUI - Honorable Mention</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == '3DUI Contest' %}
        {% if item.award == 'Honorable Mention' %}
            {% for j in site.data.3duicontest %}
                {% if j.id == item.id %}
                <h4 id="3dui{{ j.id }}">{{ j.title }}</h4>
                <p><i>{{ j.authors }}</i></p>
                <!-- <div id="3dui{{ j.id }}" class="wrap-collabsible"> <input id="collapsible3dui{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsible3dui{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div> -->
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}    
{% endfor %}
</div>

<h2 id='DC-best' class="alignCenter">DC - Honorable Mention</h2>
<div>
    <h4>Supporting Embodied Sensemaking in Immersive Environment</h4>
    <p>
        <strong>Yidan Zhang</strong><br/>
        <i>Monash University</i><br/>
    </p>
</div>
<div>
    <h4>Immersive Record and Replay for Lively Virtual Environments</h4>
    <p>
        <strong>Klara Brandstätter</strong><br/>
        <i>University College London</i><br/>
    </p>
</div>
<div>
    <h4>Limb Motion Guidance in Extended Reality</h4>
    <p>
        <strong>Xingyao Yu</strong><br/>
        <i>University of Stuttgart</i><br/>
    </p>
</div>

<h2 id='DC-best' class="alignCenter">DC - Best Presentation</h2>
<div>
    <h4>Fostering Well-Being with Virtual Reality Applications</h4>
    <p>
        <strong>Nadine Wagner</strong><br/>
        <i>University of Bremen</i><br/>
    </p>
</div>

<h2 id='Paper-presentation-best' class="alignCenter">Best Paper Presentation</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == 'PresentationJ' %}
        {% if item.award == 'Best Presentation' %}
            {% for j in site.data.journalpapers %}
                {% if j.id == item.id %}
                {% assign authornames = j.authors | split: ";" %}
                <h4 id="J{{ j.id }}">{{ j.Title }}</h4>
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
                <div id="J{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleJ{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleJ{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
    {% if item.type == 'PresentationC' %}
        {% if item.award == 'Best Presentation' %}
            {% for j in site.data.conferencepapers %}
                {% if j.id == item.id %}
                {% assign authornames = j.authors | split: ";" %}
                <h4 id="C{{ j.id }}">{{ j.Title }}</h4>
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
                <div id="C{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleC{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleC{{ j.id }}" class="lbl-toggle">Abstract</label>
                    <div class="collapsible-content">
                        <div class="content-inner">
                            <p>{{ j.abstract }}</p>
                        </div>
                    </div>
                </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
{% endfor %}
</div>

<!--<h2 id='best-dissertation' class="alignCenter">Best Dissertation</h2>
 <div>
    <h4>A Framework for Enhancing the Sense of Presence in Virtual and Mixed Reality</h4>
    <p>
        <strong>Misha Sra</strong><br/>
        <i>Massachusets Institute of Technology</i><br/>
        Advisor: <i>Pattie Maes</i>
    </p>
</div>
<h2 id='honorable-dissertation' class="alignCenter">Best Dissertation - Honorable Mention</h2>
<div>
    <h4>Optimal Spatial Registration of SLAM for Augmented Reality</h4>
    <p>
        <strong>Folker Wientapper</strong><br/>
        <i>Technical University of Darmstadt</i><br/>
        Advisor: <i>Arjan Kuijper</i>
    </p>
</div> -->

<!-- <h2 id='ready-player-21' class="alignCenter">Ready Player 21 - Winner</h2>
<div>
    <h4>Xiaodan Hu</h4>
    <i>Nara Institute of Science and Technology, Ikoma, Japan</i>
</div> -->

