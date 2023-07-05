---
layout: ieeevr-default
title: "3DUI Contest"
---

<link rel="stylesheet" href="{{ '/assets/css/tableStyles.css' | relative_url }}">


<h1>3DUI Contest</h1>

<div>
    <h2>Fast Forward</h2>
    
<div class="video-container">
    <iframe src="https://www.youtube.com/embed/a86uUNm-kAU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>
    

<div>
    <table class="styled-table">

        <tr>
            <th>3DUI Contest Entries</th>
        </tr>
        {% for entry in site.data.3duicontest %}
        <tr>
            <td style="font-size: 0.9em;"><a href="#{{ entry.id }}">{{ entry.title }}</a></td>
        </tr>
        {% endfor %}
    </table>
</div>
<!-- TAKE ME TO THE EVENT START -->
<!-- <div>
    {% for event in site.data.events %}
    {% if event.id == '3dui1' %}
    {% if event.location %}
    <div class="notice--info" style="background-color: $theme-yellow ! important; color: $theme-text ! important;">
        <strong style="padding-bottom: 5px;">Take me to the event:</strong>
        <p>
            <strong style="color: black;">Virbela Location:</strong> {{ event.location }} (<a href="/2021/attend/virbela-instructions/#map">MAP</a>)
            {% if event.stream-url %}
            <br />
            {% if event.aindanaoaconteceu %}
            <strong style="color: black;">Watch the 3DUI Contest Fast Forward here:</strong> <a href="{{ event.stream-url }}" target="_blank">HERE</a>
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
</div> -->
<!-- TAKE ME TO THE EVENT END-->


<!-- <div class="notice--info" style="background-color: $theme-yellow ! important; color: $theme-text ! important;">
    <strong>Best of IEEE VR 2021</strong>
    <p>
        Please use this form to vote for the best poster, best demo, and best 3DUI contest submission.
    </p>
    <center>
        <p style="font-size: 20px;">
            <a href="https://cutt.ly/Mx0n5Zu" class="btn btn--primary" style="color: white;" target="_blank">Vote!</a>
        </p>
    </center>
</div> -->


<div>
    {% for entry in site.data.3duicontest %}
    <h3 id="{{ entry.id }}">{{ entry.title }}</h3>
    <p><small><strong> Booth {{ entry.boothid2}} - {{ entry.boothid1}}   </strong></small></p>
    <p><i>{{ entry.authors }}</i></p>  
    {% if entry.url-embed %}
        <div class="video-container">
            <iframe src="https://www.youtube.com/embed/{{ entry.url-embed }}" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
    {% endif %}
    <hr>
    {% endfor %}
</div>
