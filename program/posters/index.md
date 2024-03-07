---
layout: ieeevr-default
title: "Posters"
subtitle: "IEEE VR 2024"
title_separator: "|"
---

<h1>Posters</h1>
<div>
    <table class="styled-table">
        <tr>
            <th colspan="3">Posters (Timezone: Orlando, Florida USA UTC-4)</th>
        </tr>
        <tr>
            <td class="medLarge"><a href="#P1">Monday Posters</a></td>
            <td class="medLarge">Sorcerer's Apprentice Ballroom</td>
            <td class="medLarge">Talk with the authors:<br/>9:45&#8209;10:15, 13:00&#8209;13:30, 15:00&#8209;15:30, 17:00&#8209;17:30</td>
        </tr>
        <tr>
            <td class="medLarge"><a href="#P2">Tuesday Posters</a></td>
            <td class="medLarge">Sorcerer's Apprentice Ballroom</td>
            <td class="medLarge">Talk with the authors:<br/>9:45&#8209;10:15, 13:00&#8209;13:30, 15:00&#8209;15:30, 17:00&#8209;17:30</td>
        </tr>
        <tr>
            <td class="medLarge"><a href="#P3">Wednesday Posters</a></td>
            <td class="medLarge">Sorcerer's Apprentice Ballroom</td>
            <td class="medLarge">Talk with the authors:<br/>9:45&#8209;10:15, 13:00&#8209;13:30, 15:00&#8209;15:30, 17:00&#8209;17:30</td>
        </tr>
    </table>
</div>

<div>    
    <h2 id="P1" class="pink" style="padding-top:25px;">Monday Posters</h2>    
    {% for poster in site.data.mondayPosters %}
        <p>
            <strong>{{ poster.title }} (ID: {{ poster.id }})</strong>
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
        </p>
    {% endfor %}
</div>
<div>
    <h2 id="P2" class="pink" style="padding-top:25px;">Tuesday Posters</h2>
    {% for poster in site.data.tuesdayPosters %}
        <p>
             <strong>{{ poster.title }} (ID: {{ poster.id }})</strong>
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
        </p>
    {% endfor %}
</div>
<div>
    <h2 id="P3" class="pink" style="padding-top:25px;">Wednesday Posters</h2>
    {% for poster in site.data.wednesdayPosters %}
        <p>
             <strong>{{ poster.title }} (ID: {{ poster.id }})</strong>
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
        </p> 
    {% endfor %}
</div>