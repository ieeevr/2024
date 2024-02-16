---
layout: ieeevr-default
title: "Program Overview"
---
<link rel="stylesheet" href="{{ '/assets/css/calendar.css' | relative_url }}?version=20240216">
    
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
<div id="accordion">
    <div>
        <h4 id="day1">Saturday, 16 March 2024</h4>
        <div class="schedule-sat" aria-labelledby="Saturday, 16 March 2024 - Workshop Schedule"> 
            <p class="time-slot" style="grid-row: time-0800;">8:00&nbsp;am</p>             
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'XRGaming' %}
                    <div class="session session-1 track-blue" style="grid-column: track-1; grid-row: time-0800 / time-1200;">                    
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00&nbsp;am - 12:00&nbsp;pm</span>
                        <span class="session-track">Room: 1</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}   
            {% endfor %}                 
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'KELVAR' %}
                    <div class="session session-2 track-blue" style="grid-column: track-2; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00&nbsp;am - 12:00&nbsp;pm</span>
                        <span class="session-track">Room: 2</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>         
                {% endif %}     
            {% endfor %}                  
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'LocXR' %}
                    <div class="session session-3 track-blue" style="grid-column: track-3; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00&nbsp;am - 12:00&nbsp;pm</span>
                        <span class="session-track">Room: 3</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>        
                {% endif %}   
            {% endfor %}                  
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'CLEVER' %}
                    <div class="session session-4 track-blue" style="grid-column: track-4; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00&nbsp;am - 12:00&nbsp;pm</span>
                        <span class="session-track">Room: 4</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}    
            {% endfor %}                  
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'XRIOS' %}
                    <div class="session session-5 track-blue" style="grid-column: track-5; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00&nbsp;am - 12:00&nbsp;pm</span>
                        <span class="session-track">Room: 5</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}     
            {% endfor %}                            
            {% for workshop in site.data.workshops %}    
                {% if workshop.id == 'IDEATExR' %}
                    <div class="session session-6 track-blue" style="grid-column: track-6; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00&nbsp;am - 12:00&nbsp;pm</span>
                        <span class="session-track">Room: 6</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}     
            {% endfor %}              
            <p class="time-slot" style="grid-row: time-1200;">12:00&nbsp;pm</p> 
            <div class="session session-7 track-all" style="grid-column: track-1-start / track-6-end; grid-row: time-1200 / time-1330;">
                <h3 class="session-title">Lunch: 12:00&nbsp;pm- 1:30&nbsp;pm</h3>
            </div>            
            <p class="time-slot" style="grid-row: time-1330;">1:30&nbsp;pm</p>   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'WISP' %}
                    <div class="session session-8 track-blue" style="grid-column: track-1; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30&nbsp;pm - 5:30&nbsp;pm</span>
                        <span class="session-track">Room: 1</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'VHCIE' %}
                    <div class="session session-9 track-blue" style="grid-column: track-2; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30&nbsp;pm - 5:30&nbsp;pm</span>
                        <span class="session-track">Room: 2</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>              
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'GEMINI' %}
                    <div class="session session-10 track-blue" style="grid-column: track-3; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30&nbsp;pm - 5:30&nbsp;pm</span>
                        <span class="session-track">Room: 3</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'ENPTXR' %}
                    <div class="session session-11 track-blue" style="grid-column: track-4; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30&nbsp;pm - 5:30&nbsp;pm</span>
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
                        <span class="session-time">1:30&nbsp;pm - 5:30&nbsp;pm</span>
                        <span class="session-track">Room: 5</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'IDEATExR' %}
                    <div class="session session-13 track-blue" style="grid-column: track-6; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30&nbsp;pm - 5:30&nbsp;pm</span>
                        <span class="session-track">Room: 6</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}       
            {% endfor %}  
        </div> 
    </div>
    <div>
        <h4 id="day2">Sunday, 17 March 2024</h4> 
        <div class="schedule-sun" aria-labelledby="Sunday, 17 March 2024 - Workshop Schedule"> 
            <p class="time-slot" style="grid-row: time-0800;">8:00&nbsp;am</p>
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'MASSXR' %}
                    <div class="session session-1 track-blue" style="grid-column: track-1; grid-row: time-0800 / time-1200;">                        
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00&nbsp;am - 12:00&nbsp;pm</span>
                        <span class="session-track">Room: 1</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %} 
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'IVL' %}
                    <div class="session session-2 track-blue" style="grid-column: track-2; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00&nbsp;am - 12:00&nbsp;pm</span>
                        <span class="session-track">Room: 2</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>         
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'ReDigiTS' %}
                    <div class="session session-3 track-blue" style="grid-column: track-3; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00&nbsp;am - 12:00&nbsp;pm</span>
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
                        <span class="session-time">8:00&nbsp;am - 12:00&nbsp;pm</span>
                        <span class="session-track">Room: 4</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'PANDAS' %}
                    <div class="session session-5 track-blue" style="grid-column: track-5; grid-row: time-0800 / time-1200;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00&nbsp;am - 12:00&nbsp;pm</span>
                        <span class="session-track">Room: 5</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}  
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'NIDIT' %}
                    <div class="session session-6 track-blue" style="grid-column: track-6; grid-row: time-0800 / time-1200;">                   
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">8:00&nbsp;am - 12:00&nbsp;pm</span>
                        <span class="session-track">Room: 6</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}               
             <div class="session session-14 track-f3" style="grid-column: track-7; grid-row: time-0830 / time-0845;">                        
                <h3 class="session-title smalltext">Future Faculty Forum (F3)</h3>
            </div>    
            <p class="time-slot" style="grid-row: time-0845;">8:45&nbsp;am</p>         
            <div class="session session-14 track-f3" style="grid-column: track-7; grid-row: time-0845 / time-0900;">                        
                <h3 class="session-title smalltext">F3 | Welcome & Opening Remarks</h3>
                <span class="session-time smalltext">8:45&nbsp;am&nbsp;-&nbsp;9:00&nbsp;am</span>
            </div>                
            <p class="time-slot" style="grid-row: time-0900;">9:00&nbsp;am</p>           
            <div class="session session-15 track-f3" style="grid-column: track-7; grid-row: time-0900 / time-1000;">  
                <h3 class="session-title smalltext">F3 | Tutorial: Professor Application Process</h3>                      
                <span class="session-time smalltext">9:00&nbsp;am&nbsp;-&nbsp;10:00&nbsp;am</span>
            </div>            
            <p class="time-slot" style="grid-row: time-1000;">10:00&nbsp;am</p>
            <div class="session session-16  track-f3" style="grid-column: track-7; grid-row: time-1000 / time-1030;">
                <h3 class="session-title smalltext">F3 | Break:<br> 10:00&nbsp;am&nbsp;-&nbsp;10:30&nbsp;am</h3>
            </div>     
            <p class="time-slot" style="grid-row: time-1030;">10:30&nbsp;am</p>   
            <div class="session session-17 track-f3" style="grid-column: track-7; grid-row: time-1030 / time-1115;">                        
                <h3 class="session-title smalltext">F3 | Panel 1: Differences in Universities (Geo, Research vs. Teaching Alloc.)</h3>
                <span class="session-time smalltext">10:30&nbsp;am&nbsp;-&nbsp;11:15&nbsp;am</span>
            </div>      
            <p class="time-slot" style="grid-row: time-1115;">11:15&nbsp;am</p>          
            <div class="session session-18 track-f3" style="grid-column: track-7; grid-row: time-1115 / time-1200;">                        
                <h3 class="session-title smalltext">F3 | Panel 2: Lab Formation & Management</h3>
                <span class="session-time smalltext">11:15&nbsp;am - 12:00&nbsp;pm</span>
            </div>   
            <p class="time-slot" style="grid-row: time-1200;">12:00&nbsp;pm</p>
            <div class="session session-7 track-all" style="grid-column: track-1-start / track-7-end; grid-row: time-1200 / time-1330;">
                <h3 class="session-title">Lunch: 12:00&nbsp;pm - 1:30&nbsp;pm</h3>
            </div> 
            <p class="time-slot" style="grid-row: time-1330;">1:30&nbsp;pm</p>             
            {% for workshop in site.data.workshops %} 
                {% if workshop.id == 'TrainingXR' %}
                    <div class="session session-8 track-blue" style="grid-column: track-1; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30&nbsp;pm - 5:30&nbsp;pm</span>
                        <span class="session-track">Room: 1</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}      
            {% endfor %}  
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'OAT' %}
                    <div class="session session-9 track-blue" style="grid-column: track-2; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30&nbsp;pm - 5:30&nbsp;pm</span>
                        <span class="session-track">Room: 2</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>              
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'AVR' %}
                    <div class="session session-10 track-blue" style="grid-column: track-3; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30&nbsp;pm - 5:30&nbsp;pm</span>
                        <span class="session-track">Room: 3</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'xrWORKS' %}
                    <div class="session session-11 track-blue" style="grid-column: track-4; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30&nbsp;pm - 5:30&nbsp;pm</span>
                        <span class="session-track">Room: 4</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}  
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'ANIVAE' %}
                    <div class="session session-12 track-blue" style="grid-column: track-5; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30&nbsp;pm - 5:30&nbsp;pm</span>
                        <span class="session-track">Room: 5</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'NIDIT' %}
                    <div class="session session-13 track-blue" style="grid-column: track-6; grid-row: time-1330 / time-1730;">
                        <h3 class="session-title"><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                        <span class="session-time">1:30&nbsp;pm - 5:30&nbsp;pm</span>
                        <span class="session-track">Room: 6</span>
                        <span class="session-presenter">{{ workshop.organiser }}</span>
                    </div>
                {% endif %}       
            {% endfor %}            
             <div class="session session-19 track-f3" style="grid-column: track-7; grid-row: time-1330 / time-1415;">                  
                <h3 class="session-title smalltext">F3 | Panel 3: Challenges & Opportunities&nbsp;of Interdisciplinary Research</h3>
                <span class="session-time smalltext">1:30&nbsp;pm - 2:15&nbsp;pm</span>
            </div>   
            <p class="time-slot" style="grid-row: time-1415;">2:15&nbsp;pm</p>          
            <div class="session session-20 track-f3" style="grid-column: track-7; grid-row: time-1415 / time-1530;">                        
                <h3 class="session-title smalltext">F3 | Tutorial: Review & Critique of Application Materials (Research, Teaching & Diversity Statements)</h3>
                <span class="session-time smalltext">2:15&nbsp;pm - 3:30&nbsp;pm</span>
            </div>
            <p class="time-slot" style="grid-row: time-1530;">3:30&nbsp;pm</p>
            <div class="session session-16 track-f3" style="grid-column: track-7; grid-row: time-1530 / time-1600;">
                <h3 class="session-title smalltext">F3 | Break:<br> 3:30&nbsp;pm - 4:00&nbsp;pm</h3>
            </div>    
            <p class="time-slot" style="grid-row: time-1600;">4:00&nbsp;pm</p>         
            <div class="session session-22 track-f3" style="grid-column: track-7; grid-row: time-1600 / time-1645;">                        
                <h3 class="session-title smalltext">F3 | Speed Advising</h3>
                <span class="session-time smalltext">4:00&nbsp;pm - 4:45&nbsp;pm</span>
            </div>          
            <p class="time-slot" style="grid-row: time-1645;">4:45&nbsp;pm</p>   
            <div class="session session-23 track-f3" style="grid-column: track-7; grid-row: time-1645 / time-1700;">                        
                <h3 class="session-title smalltext">F3 | Closing Remarks & Feedback for Future F3 Events</h3>
                <span class="session-time smalltext">4:45&nbsp;pm - 5:00&nbsp;pm</span>
            </div> 
        </div> 
    </div> 
</div>