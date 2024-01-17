---
layout: ieeevr-default
title: "Program Overview"
---
<link rel="stylesheet" href="{{ '/assets/css/calendar.css' | relative_url }}?version=20240108_1">
    
<script>
    (function($) {
        $(function() {
            $("#accordion > div").accordion({ header: "h4", heightStyle: "content", active: false, collapsible: true });
        })
    })(jQuery);

   $(document).ready(function(){
		$('#day1').click(); 
    });   
</script>

<h1 id="schedule-heading">Program Overview</h1>
<div class="notice--info alignCenter bold" style="font-size: 0.9em !important;">
    Please note that all times are given in Orlando, Florida USA local time, EDT (UTC-4).
</div>
<div class="small italic alignCenter"><strong>Updated:</strong> 16 January 2024 <br>See highlights below.</div>
<div class="clear"></div>
<div id="accordion">
    <div>
        <h4 id="day1">Saturday, 16 March 2024</h4>
        <div class="schedule-sat" aria-labelledby="March 16 - Workshop Schedule"> 
            <h2 class="time-slot" style="grid-row: time-0800;">8:00am</h2>                
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'XRGaming' %}
                    <div class="session session-1 track-blue" style="grid-column: track-1; grid-row: time-0800 / time-1200;">                    
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00am - 12:00pm</span>
                        <span class="session-track">Room: 1</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}   
            {% endfor %}                 
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'KELVAR' %}
                    <div class="session session-2 track-blue" style="grid-column: track-2; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00am - 12:00pm</span>
                        <span class="session-track">Room: 2</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>         
                {% endif %}     
            {% endfor %}                  
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'LocXR' %}
                    <div class="session session-3 track-blue" style="grid-column: track-3; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00am - 12:00pm</span>
                        <span class="session-track">Room: 3</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>        
                {% endif %}   
            {% endfor %}                  
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'CLEVER' %}
                    <div class="session session-4 track-blue" style="grid-column: track-4; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00am - 12:00pm</span>
                        <span class="session-track">Room: 4</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}    
            {% endfor %}                  
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'XRIOS' %}
                    <div class="session session-5 track-blue" style="grid-column: track-5; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00am - 12:00pm</span>
                        <span class="session-track">Room: 5</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}     
            {% endfor %}                            
            {% for workshop in site.data.workshops %}    
                {% if workshop.id == 'IDEATExR' %}
                    <div class="session session-6 track-blue" style="grid-column: track-6; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00am - 12:00pm</span>
                        <span class="session-track">Room: 6</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}     
            {% endfor %}   
                <h2 class="time-slot" style="grid-row: time-1200;">12:00pm</h2>
                <div class="session session-7 track-all" style="grid-column: track-1-start / track-6-end; grid-row: time-1200 / time-1330;">
                <h3 class="session-title">Lunch: 12:00-1:30</h3>
                </div>
                <h2 class="time-slot" style="grid-row: time-1330;">1:30pm</h2>
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'WISP' %}
                    <div class="session session-8 track-blue" style="grid-column: track-1; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30pm - 5:30pm</span>
                        <span class="session-track">Room: 1</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'VHCIE' %}
                    <div class="session session-9 track-blue" style="grid-column: track-2; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30pm - 5:30pm</span>
                        <span class="session-track">Room: 2</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>              
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'GEMINI' %}
                    <div class="session session-10 track-blue" style="grid-column: track-3; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30pm - 5:30pm</span>
                        <span class="session-track">Room: 3</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'ENPTXR' %}
                    <div class="session session-11 track-blue" style="grid-column: track-4; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30pm - 5:30pm</span>
                        <span class="session-track">Room: 4</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'WSR' %}
                    <div class="session session-12 track-blue" style="grid-column: track-5; grid-row: time-1330 / time-1730;">
                        <div class="overview_update small alignCenter">Update:<br />2024-01-16</div>
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30pm - 5:30pm</span>
                        <span class="session-track">Room: 5</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'IDEATExR' %}
                    <div class="session session-13 track-blue" style="grid-column: track-6; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30pm - 5:30pm</span>
                        <span class="session-track">Room: 6</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}       
            {% endfor %}  
        </div> 
    </div>
    <div>
        <h4 id="day2">Sunday, 17 March 2024</h4> 
        <div class="schedule-sun" aria-labelledby="March 16 - Workshop Schedule">  
            <h2 class="time-slot" style="grid-row: time-0800;">8:00am</h2> 
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'MASSXR' %}
                    <div class="session session-1 track-blue" style="grid-column: track-1; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00am - 12:00pm</span>
                        <span class="session-track">Room: 1</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'IVL' %}
                    <div class="session session-2 track-blue" style="grid-column: track-2; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00am - 12:00pm</span>
                        <span class="session-track">Room: 2</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>         
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'ReDigiTS' %}
                    <div class="session session-3 track-blue" style="grid-column: track-3; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00am - 12:00pm</span>
                        <span class="session-track">Room: 3</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>        
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'Data4XR' %}
                    <div class="session session-4 track-blue" style="grid-column: track-4; grid-row: time-0800 / time-1200;">                    
                        <div class="overview_update small alignCenter">Update:<br />2024-01-16</div>
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00am - 12:00pm</span>
                        <span class="session-track">Room: 4</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'PANDAS' %}
                    <div class="session session-5 track-blue" style="grid-column: track-5; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00am - 12:00pm</span>
                        <span class="session-track">Room: 5</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}  
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'NIDIT' %}
                    <div class="session session-6 track-blue" style="grid-column: track-6; grid-row: time-0800 / time-1200;">                   
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00am - 12:00pm</span>
                        <span class="session-track">Room: 6</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}    
                <h2 class="time-slot" style="grid-row: time-1200;">12:00pm</h2>
                <div class="session session-7 track-all" style="grid-column: track-1-start / track-6-end; grid-row: time-1200 / time-1330;">
                    <h3 class="session-title">Lunch: 12:00-1:30</h3>
                </div>
            <h2 class="time-slot" style="grid-row: time-1330;">1:30pm</h2>                
            {% for workshop in site.data.workshops %} 
                {% if workshop.id == 'TrainingXR' %}
                    <div class="session session-8 track-blue" style="grid-column: track-1; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30pm - 5:30pm</span>
                        <span class="session-track">Room: 1</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}      
            {% endfor %}  
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'OAT' %}
                    <div class="session session-9 track-blue" style="grid-column: track-2; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30pm - 5:30pm</span>
                        <span class="session-track">Room: 2</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>              
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'AVR' %}
                    <div class="session session-10 track-blue" style="grid-column: track-3; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30pm - 5:30pm</span>
                        <span class="session-track">Room: 3</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'xrWORKS' %}
                    <div class="session session-11 track-blue" style="grid-column: track-4; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30pm - 5:30pm</span>
                        <span class="session-track">Room: 4</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}  
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'ANIVAE' %}
                    <div class="session session-12 track-blue" style="grid-column: track-5; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30pm - 5:30pm</span>
                        <span class="session-track">Room: 5</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'NIDIT' %}
                    <div class="session session-13 track-blue" style="grid-column: track-6; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30pm - 5:30pm</span>
                        <span class="session-track">Room: 6</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}       
            {% endfor %}  
        </div> 
    </div>
</div>