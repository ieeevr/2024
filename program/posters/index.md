---
layout: ieeevr-default
title: "Posters"
---

<link rel="stylesheet" href="{{ '/assets/css/tableStyles.css' | relative_url }}">
<h1>Posters</h1>
<div>
    <table class="styled-table">
        <tr>
            <th>Posters</th>
            <th>Location</th>
        </tr>
        <tr>
            <td><a href="#P1">Poster Session 1</a></td>
            <td>Session/Server 1</td>
        </tr>
        <tr>
            <td><a href="#P2">Poster Session 2</a></td>
            <td>Session/Server 2</td>
        </tr>
        <tr>
            <td><a href="#P3">Poster Session 3</a></td>
            <td>Session/Server 3</td>
        </tr>
    </table>
</div>

<div>
    <h2>
        On-site Floor Plan
    </h2>
    <img src="../../assets/images/program/posters/map.png" style="width: 80%"/>
</div>


<div>    
    <h2 id="P1"> Session/Server 1</h2>    
    {% for poster in site.data.posters %}
    {% if poster.location == 'Session/Server 1' %}
    <h3 id="{{ poster.id }}">{{ poster.title }}</h3>
    <p><strong>{{ poster.type }}</strong></p> 
    {% if poster.booth %}
<p> <small><strong style="color: black;"> Booth: {{ poster.booth }} </strong></small> <br> </p>  
    {% endif %}
    <p><i>{{ poster.authors }}</i></p>
    {% if poster.url %}
        <p>Teaser Video: <a href="{{ poster.url }}" target="_blank">Watch Now</a></p>
    {% endif %}
    {% if poster.abstract %}
    <div id="{{ poster.id }}" class="wrap-collabsible"> <input id="collapsibleabstract{{ poster.id }}" class="toggle" type="checkbox"> <label for="collapsibleabstract{{ poster.id }}" class="lbl-toggle">Abstract</label>
        <div class="collapsible-content">
            <div class="content-inner">
                <p>{{ poster.abstract }}</p>
            </div>
        </div>
    </div>   
    {% endif %}    
    {% endif %}
    {% endfor %}
</div>

<div>
    <h2 id="P2"> Session/Server 2</h2>
    {% for poster in site.data.posters %}
    {% if poster.location == 'Session/Server 2' %}
    <h3 id="{{ poster.id }}">{{ poster.title }}</h3>
    <p><strong>{{ poster.type }}</strong></p>
    {% if poster.booth %}
<p> <small><strong style="color: black;"> Booth: {{ poster.booth }} </strong></small> <br> </p>  
    {% endif %}
    <p><i>{{ poster.authors }}</i></p>
    {% if poster.url %}
        <p>Teaser Video: <a href="{{ poster.url }}" target="_blank">Watch Now</a></p>
    {% endif %}
    {% if poster.abstract %}
    <div id="{{ poster.id }}" class="wrap-collabsible"> <input id="collapsibleabstract{{ poster.id }}" class="toggle" type="checkbox"> <label for="collapsibleabstract{{ poster.id }}" class="lbl-toggle">Abstract</label>
        <div class="collapsible-content">
            <div class="content-inner">
                <p>{{ poster.abstract }}</p>
            </div>
        </div>
    </div>   
    {% endif %}    
    {% endif %}
    {% endfor %}
</div>

<div>
    <h2 id="P3"> Session/Server 3</h2>
    {% for poster in site.data.posters %}
    {% if poster.location == 'Session/Server 3' %}
    <h3 id="{{ poster.id }}">{{ poster.title }}</h3>
    <p><strong>{{ poster.type }}</strong></p>
    {% if poster.booth %}
<p> <small><strong style="color: black;"> Booth: {{ poster.booth }} </strong></small> <br> </p>  
    {% endif %}
    <p><i>{{ poster.authors }}</i></p>
    {% if poster.url %}
        <p>Teaser Video: <a href="{{ poster.url }}" target="_blank">Watch Now</a></p>
    {% endif %}
    {% if poster.abstract %}
    <div id="{{ poster.id }}" class="wrap-collabsible"> <input id="collapsibleabstract{{ poster.id }}" class="toggle" type="checkbox"> <label for="collapsibleabstract{{ poster.id }}" class="lbl-toggle">Abstract</label>
        <div class="collapsible-content">
            <div class="content-inner">
                <p>{{ poster.abstract }}</p>
            </div>
        </div>
    </div>   
    {% endif %}    
    {% endif %}
    {% endfor %}
</div>