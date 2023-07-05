---
layout: ieeevr-default
title: "Videos"
---

<link rel="stylesheet" href="{{ '/assets/css/tableStyles.css' | relative_url }}">

<div>
    <table class="styled-table">
        <tr>
            <th>Videos</th>
        </tr>
        {% for video in site.data.videos %}
        <tr>
            <td style="font-size: 0.9em;"><a href="#{{ video.id }}">{{ video.title }}</a></td>
        </tr>
        {% endfor %}
    </table>
</div>

<div>
    {% for video in site.data.videos %}

    <h3 id="{{ video.id }}">{{ video.title }}</h3>
    <p><i>{{ video.authors }}</i></p>

    <div class="video-container">
        <iframe src="https://www.youtube.com/embed/{{ video.url-embed }}" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
    
    <div id="{{ video.id }}" class="wrap-collabsible"> <input id="collapsible{{ video.id }}" class="toggle" type="checkbox"> <label for="collapsible{{ video.id }}" class="lbl-toggle">Abstract</label>
        <div class="collapsible-content">
            <div class="content-inner">
                <p>{{ video.abstract }}</p>
            </div>
        </div>
    </div>

    {% endfor %}
</div>