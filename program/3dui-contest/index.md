---
layout: ieeevr-default
title: "3DUI Contest"
subtitle: "IEEE VR 2024"
title_separator: "|"
---
<h1>3DUI Contest</h1>
  
<div>
    <table class="styled-table">
        <tr>
            <th>3DUI Contest Entries</th>
        </tr>
        {% assign i = 0 %}
        {% for entry in site.data.contest3dui %}
            {% assign i = i | plus:1 %}
            <tr>
                <td class="medLarge"><a href="#{{ entry.id }}" title="{{ entry.title }}">{{ entry.title }}</a></td>
            </tr>
        {% endfor %}
    </table>
</div>
<h2>Schedule</h2>
<p>
    <table class="program-table">
        <thead>
            <tr>
                <th colspan="4">3DUI&nbsp;Contest&nbsp;Schedule (Timezone: Orlando, Florida USA UTC-4)</th>
            </tr>
        </thead>
        <tbody>           
            <tr>
                <td style="width:25%">3DUI&nbsp;Contest Fast&nbsp;Forward</td>
                <td style="width:25%">Monday,&nbsp;18&nbsp;March</td>                
                <td style="width:25%">13:00&#8209;13:30</td>             
                <td style="width:25%">Fantasia Ballroom&nbsp;H</td>
            </tr>
             <tr>
                <td>3DUI&nbsp;Contest Booths&nbsp;Open</td>
                <td>Monday,&nbsp;18&nbsp;March</td>                
                <td>9:45&#8209;10:00, 13:00&#8209;13:30, 15:00&#8209;15:30, 17:00&#8209;19:00</td>       
                <td>Sorcerer's&nbsp;Apprentice Ballroom</td>  
            </tr>            
             <tr>
                <td>3DUI&nbsp;Contest Booths&nbsp;Open</td>
                <td>Tuesday,&nbsp;19&nbsp;March</td>                
                <td>9:45&#8209;10:00, 13:00&#8209;13:30, 15:00&#8209;15:30, 17:00&#8209;17:30</td>       
                <td>Sorcerer's&nbsp;Apprentice Ballroom</td>  
            </tr>
            <tr>
                <td>3DUI&nbsp;Contest Booths&nbsp;Open</td>
                <td>Wednesday,&nbsp;20&nbsp;March</td>                
                <td>9:45&#8209;10:00, 13:00&#8209;13:30, 15:00&#8209;15:30, 17:00&#8209;17:30</td>       
                <td>Sorcerer's&nbsp;Apprentice Ballroom</td>  
            </tr>
            <tr>
                <td>Awards</td>
                <td>Thursday,&nbsp;21&nbsp;March</td>                
                <td>15:30&#8209;17:00</td>       
                <td>Fantasia Ballroom&nbsp;H</td>  
            </tr>
        </tbody>
    </table>
</p>
<h2>Entries</h2>
<div>
    {% assign j = 0 %}
    {% for entry in site.data.contest3dui %}
        {% assign j = j | plus:1 %}
        <h3 id="{{ entry.id }}">{{ entry.title }}</h3>
        {% if entry.boothid2 %}
            <p><small><strong> Booth {{ entry.boothid2}} - {{ entry.boothid1}}   </strong></small></p>        
        {% endif %}
        <p><i>{{ entry.authors }}</i></p>  
        {% if entry.url-embed %}
            <div class="video-container">
                <iframe src="https://www.youtube.com/embed/{{ entry.url-embed }}" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </div>
        {% endif %}
        {% if j == i %}
        {% else %}
            <hr style="margin: 25px 0 25px 0;">
        {% endif %}
    {% endfor %}
</div>
