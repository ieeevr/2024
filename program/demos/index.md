---
layout: ieeevr-default
title: "Research Demos"
---

<link rel="stylesheet" href="{{ '/assets/css/tableStyles.css' | relative_url }}">

<div>
    <table class="styled-table">

        <tr>
            <th>Research Demos</th>
        </tr>
        {% for demo in site.data.demos %}
        <tr>
            <td style="font-size: 0.9em;"><a href="#{{ demo.id }}">{{ demo.title }}</a></td>
        </tr>
        {% endfor %}
    </table>
</div>

<div>
    {% for demo in site.data.demos %}
    <h3 id="{{ demo.id }}">{{ demo.title }}</h3>
    <p><i>{{ demo.authors }}</i></p>
<p> <small><strong style="color: black;"> Booth: {{ demo.booth }} - {{ demo.hall }} </strong></small> <br> </p>    
    {% if demo.url %}
        <!-- <p>Teaser Video: <a href="{{ demo.url }}" target="_blank">Watch Now</a></p> -->
    {% endif %}
    {% if demo.url-embed %}
        <div class="video-container">
            <iframe src="https://www.youtube.com/embed/{{ demo.url-embed }}" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
    {% endif %}
    {% if demo.abstract %}
    <div id="{{ demo.id }}" class="wrap-collabsible"> <input id="collapsible{{ demo.id }}" class="toggle" type="checkbox"> <label for="collapsible{{ demo.id }}" class="lbl-toggle">Abstract</label>
        <div class="collapsible-content">
            <div class="content-inner">
                <p>{{ demo.abstract }}</p>
            </div>
        </div>
    </div>
    {% endif %}
    {% endfor %}
</div>



