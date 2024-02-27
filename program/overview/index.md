---
layout: ieeevr-default
title: "Program Overview"
---
<link rel="stylesheet" href="{{ '/assets/css/calendar.css' | relative_url }}?version=20240227">
    
<script>
    (function($) {
        $(function() {
            $("#accordion > div").accordion({ header: "h4", heightStyle: "content", active: false, collapsible: true });
        })
    })(jQuery);

   $(document).ready(function(){
		$('#day1').click(); 
		$('#day2').click(); 
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
            <p class="time-slot" style="grid-row: time-0730;">7:30</p> 
            <div class="session track-registration" style="grid-column: track-0; grid-row: time-0730 / time-1530;">  
                <div class="rotate_reg">             
                    <span class="session-title">Registration:&nbsp;7:30&#8209;15:30&nbsp;&nbsp;&nbsp;&nbsp;</span>
                </div>
            </div>             
            <p class="time-slot" style="grid-row: time-0800;">8:00</p>             
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'XRGaming' %}
                    <div class="session session-w1a track-workshop" style="grid-column: track-1; grid-row: time-0800 / time-1000;">                    
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">8:00-10:00</span>
                        <span class="session-time">Room: Fantasia, A</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}   
            {% endfor %}             
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'WSR' %}
                    <div class="session session-w2a track-workshop" style="grid-column: track-2; grid-row: time-0800 / time-1000;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">8:00-10:00</span>
                        <span class="session-time">Room: Fantasia, B</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>         
                {% endif %}     
            {% endfor %}                  
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'XRIOS' %}
                    <div class="session session-w3a track-workshop" style="grid-column: track-3; grid-row: time-0800 / time-1000;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">8:00-10:00</span>
                        <span class="session-time">Room: Fantasia, C</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>        
                {% endif %}   
            {% endfor %}                  
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'LocXR' %}
                    <div class="session session-w4a track-workshop" style="grid-column: track-4; grid-row: time-0800 / time-1000;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">8:00-10:00</span>
                        <span class="session-time">Room: Fantasia, D</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}    
            {% endfor %}                  
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'KELVAR' %}
                    <div class="session session-w5a track-workshop" style="grid-column: track-5; grid-row: time-0800 / time-1000;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">8:00-10:00</span>
                        <span class="session-time">Room: Fantasia, E</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}     
            {% endfor %}                            
            {% for workshop in site.data.workshops %}    
                {% if workshop.id == 'IDEATExR' %}
                    <div class="session session-w6a track-workshop" style="grid-column: track-6; grid-row: time-0800 / time-1000;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">8:00-10:00</span>
                        <span class="session-time">Room: Fantasia, F</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}     
            {% endfor %}     
            <p class="time-slot" style="grid-row: time-0845;">8:15</p>    
            <div class="session session-w1b track-consortium" style="grid-column: track-8; grid-row: time-0815 / time-1000;">                    
                <span class="session-title">Doctoral Consortium</span><br/>
                <span class="session-time">8:15-10:00</span>
                <span class="session-time">Room: Sorcerer's Apprentice, 2</span>
            </div>              
            <p class="time-slot" style="grid-row: time-0830;">8:30</p>    
            {% for tutorial in site.data.tutorials %}  
                {% if tutorial.id == 'T1' %}
                    <div class="session session-t1a track-tutorials" style="grid-column: track-7; grid-row: time-0830 / time-1000;">                    
                        <span class="session-title">Tutorial<br /><a href="{{ '/program/tutorials/' | relative_url }}#{{ tutorial.id }}">{{ tutorial.title }}</a></span><br/>
                        <span class="session-time">8:30-10:00</span>
                        <span class="session-time">Room: Fantasia, K-M</span>
                        <span class="session-presenter"><br />{{ tutorial.authors }}</span>
                    </div>
                {% endif %}   
            {% endfor %} 
            <p class="time-slot" style="grid-row: time-1000;">10:00</p>
            <div class="session session-16 track-all" style="grid-column:  track-1-start / track-8-end; grid-row: time-1000 / time-1030;">
                <span class="session-title">Break: 10:00-10:30</span>
            </div>   
             <p class="time-slot" style="grid-row: time-1030;">10:30</p>             
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'XRGaming' %}
                    <div class="session session-w1b track-workshop" style="grid-column: track-1; grid-row: time-1030 / time-1200;">                    
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">10:30-12:00</span>
                        <span class="session-time">Room: Fantasia, A</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}   
            {% endfor %}           
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'WSR' %}
                    <div class="session session-w2b track-workshop" style="grid-column: track-2; grid-row: time-1030 / time-1200;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">10:30-12:00</span>
                        <span class="session-time">Room: Fantasia, B</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>         
                {% endif %}     
            {% endfor %}                  
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'XRIOS' %}
                    <div class="session session-w3b track-workshop" style="grid-column: track-3; grid-row: time-1030 / time-1200;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">10:30-12:00</span>
                        <span class="session-time">Room: Fantasia, C</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>        
                {% endif %}   
            {% endfor %}                  
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'LocXR' %}
                    <div class="session session-w4b track-workshop" style="grid-column: track-4; grid-row: time-1030 / time-1200;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">10:30-12:00</span>
                        <span class="session-time">Room: Fantasia, D</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}    
            {% endfor %}                  
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'KELVAR' %}
                    <div class="session session-w5b track-workshop" style="grid-column: track-5; grid-row: time-1030 / time-1200;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">10:30-12:00</span>
                        <span class="session-time">Room: Fantasia, E</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}     
            {% endfor %}                            
            {% for workshop in site.data.workshops %}    
                {% if workshop.id == 'IDEATExR' %}
                    <div class="session session-w6b track-workshop" style="grid-column: track-6; grid-row: time-1030 / time-1200;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">10:30-12:00</span>
                        <span class="session-time">Room: Fantasia, F</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}     
            {% endfor %}              
             {% for tutorial in site.data.tutorials %}  
                {% if tutorial.id == 'T1' %}
                    <div class="session session-t1b track-tutorials" style="grid-column: track-7; grid-row: time-1030 / time-1200;">                    
                        <span class="session-title">Tutorial (cont)<br /><a href="{{ '/program/tutorials/' | relative_url }}#{{ tutorial.id }}">{{ tutorial.title }}</a></span><br/>
                        <span class="session-time">10:30-12:00</span>
                        <span class="session-time">Room: Fantasia, k-M</span>
                        <span class="session-presenter"><br />{{ tutorial.authors }}</span>
                    </div>
                {% endif %}   
            {% endfor %}     
            <div class="session session-w1b track-consortium" style="grid-column: track-8; grid-row: time-1030 / time-1200;">                    
                <span class="session-title">Doctoral Consortium</span><br/>
                <span class="session-time">10:30-12:00</span>
                <span class="session-time">Room: Sorcerer's Apprentice, 2</span>
            </div>            
            <p class="time-slot" style="grid-row: time-1200;">12:00</p> 
            <div class="session session-lunch track-all" style="grid-column: track-1-start / track-8-end; grid-row: time-1200 / time-1330;">
                <span class="session-title">Lunch: 12:00-13:30</span>
            </div>            
            <p class="time-slot" style="grid-row: time-1330;">13:30</p>   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'WISP' %}
                    <div class="session session-7a track-workshop" style="grid-column: track-1; grid-row: time-1330 / time-1530;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">13:30-15:30</span>
                        <span class="session-time">Room: Fantasia, A</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'GEMINI' %}
                    <div class="session session-8a track-workshop" style="grid-column: track-2; grid-row: time-1330 / time-1530;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">13:30-15:30</span>
                        <span class="session-time">Room: Fantasia, B</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>              
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'VHCIE' %}
                    <div class="session session-9a track-workshop" style="grid-column: track-3; grid-row: time-1330 / time-1530;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">13:30-15:30</span>
                        <span class="session-time">Room: Fantasia, C</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'CLEVER' %}
                    <div class="session session-10a track-workshop" style="grid-column: track-4; grid-row: time-1330 / time-1530;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">13:30-15:30</span>
                        <span class="session-time">Room: Fantasia, D</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'ENPTXR' %}
                    <div class="session session-11a track-workshop" style="grid-column: track-5; grid-row: time-1330 / time-1530;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">13:30-15:30</span>
                        <span class="session-time">Room: Fantasia, E</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'IDEATExR' %}
                    <div class="session session-6c track-workshop" style="grid-column: track-6; grid-row: time-1330 / time-1530;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">13:30-15:30</span>
                        <span class="session-time">Room: Fantasia, F</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}       
            {% endfor %}       
            <div class="session session-w1b track-consortium" style="grid-column: track-8; grid-row: time-1330 / time-1530;">                    
                <span class="session-title">Doctoral Consortium</span><br/>
                <span class="session-time">13:30-15:30</span>
                <span class="session-time">Room: Sorcerer's Apprentice, 2</span>
            </div>         
            <p class="time-slot" style="grid-row: time-1530;">15:30</p>
            <div class="session session-16 track-all" style="grid-column:  track-1-start / track-8-end; grid-row: time-1530 / time-1600;">
                <span class="session-title">Break: 15:30-16:00</span>
            </div>    
            <p class="time-slot" style="grid-row: time-1600;">16:00</p>   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'WISP' %}
                    <div class="session session-7b track-workshop" style="grid-column: track-1; grid-row: time-1600 / time-1730;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">16:00-17:30</span>
                        <span class="session-time">Room: Fantasia, A</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'GEMINI' %}
                    <div class="session session-8b track-workshop" style="grid-column: track-2; grid-row: time-1600 / time-1730;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">16:00-17:30</span>
                        <span class="session-time">Room: Fantasia, B</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>              
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'VHCIE' %}
                    <div class="session session-9b track-workshop" style="grid-column: track-3; grid-row: time-1600 / time-1730;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">16:00-17:30</span>
                        <span class="session-time">Room: Fantasia, C</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'CLEVER' %}
                    <div class="session session-10b track-workshop" style="grid-column: track-4; grid-row: time-1600 / time-1730;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">16:00-17:30</span>
                        <span class="session-time">Room: Fantasia, D</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'ENPTXR' %}
                    <div class="session session-11b track-workshop" style="grid-column: track-5; grid-row: time-1600 / time-1730;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">16:00-17:30</span>
                        <span class="session-time">Room: Fantasia, E</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}     
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'IDEATExR' %}
                    <div class="session session-6d track-workshop" style="grid-column: track-6; grid-row: time-1600 / time-1730;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">16:00-17:30</span>
                        <span class="session-time">Room: Fantasia, F</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}       
            {% endfor %}                      
             {% for tutorial in site.data.tutorials %}  
                {% if tutorial.id == 'T2' %}
                    <div class="session session-t2a track-tutorials" style="grid-column: track-7; grid-row: time-1600 / time-1730;">                    
                        <span class="session-title">Tutorial<br /><a href="{{ '/program/tutorials/' | relative_url }}#{{ tutorial.id }}">{{ tutorial.title }}</a></span><br/>
                        <span class="session-time">16:00-17:30</span>
                        <span class="session-time">Room: Fantasia, K-M</span>
                        <span class="session-presenter"><br />{{ tutorial.authors }}</span>
                    </div>
                {% endif %}   
            {% endfor %}     
            <div class="session session-w1b track-consortium" style="grid-column: track-8; grid-row: time-1600 / time-1745;">                    
                <span class="session-title">Doctoral Consortium</span><br/>
                <span class="session-time">16:00-17:45</span>
                <span class="session-time">Room: Sorcerer's Apprentice, 2</span>
            </div>          
        </div> 
    </div>
    <div>
        <h4 id="day2">Sunday, 17 March 2024</h4> 
        <div class="schedule-sun" aria-labelledby="Sunday, 17 March 2024 - Workshop Schedule">  
        <p class="time-slot" style="grid-row: time-0730;">7:30</p> 
            <div class="session track-registration" style="grid-column: track-0; grid-row: time-0730 / time-1530;">  
                <div class="rotate_reg">             
                    <span class="session-title">Registration:&nbsp;7:30&#8209;15:30&nbsp;&nbsp;&nbsp;&nbsp;</span>
                </div>
            </div>   
            <p class="time-slot" style="grid-row: time-0800;">8:00</p>
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'MASSXR' %}
                    <div class="session session-w12a track-workshop" style="grid-column: track-1; grid-row: time-0800 / time-1000;">                        
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">8:00-10:00</span>
                        <span class="session-time">Room: Fantasia, A</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %} 
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'IVL' %}
                    <div class="session session-w13a track-workshop" style="grid-column: track-2; grid-row: time-0800 / time-1000;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">8:00-10:00</span>
                        <span class="session-time">Room: Fantasia, B</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>         
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'ReDigiTS' %}
                    <div class="session session-w14a track-workshop" style="grid-column: track-3; grid-row: time-0800 / time-1000;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">8:00-10:00</span>
                        <span class="session-time">Room: Fantasia, C</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>        
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'NIDIT' %}
                    <div class="session session-w15a track-workshop" style="grid-column: track-4; grid-row: time-0800 / time-1000;"> 
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">8:00-10:00</span>
                        <span class="session-time">Room: Fantasia, D</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'Data4XR' %}
                    <div class="session session-w16a track-workshop" style="grid-column: track-5; grid-row: time-0800 / time-1000;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">8:00-10:00</span>
                        <span class="session-time">Room: Fantasia, E</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}  
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'PANDAS' %}
                    <div class="session session-w17a track-workshop" style="grid-column: track-6; grid-row: time-0800 / time-1000;">                   
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">8:00-10:00</span>
                        <span class="session-time">Room: Fantasia, F</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}                          
             {% for tutorial in site.data.tutorials %}  
                {% if tutorial.id == 'T3' %}
                    <div class="session session-t3a track-tutorials" style="grid-column: track-7; grid-row: time-0830 / time-1000;">                    
                        <span class="session-title">Tutorial<br /><a href="{{ '/program/tutorials/' | relative_url }}#{{ tutorial.id }}">{{ tutorial.title }}</a></span><br/>
                        <span class="session-time">8:30-10:00</span>
                        <span class="session-time">Room: Fantasia, K-M</span>
                        <span class="session-presenter"><br />{{ tutorial.authors }}</span>
                    </div>
                {% endif %}   
            {% endfor %}                  
             <div class="session session-f31 track-f3" style="grid-column: track-8; grid-row: time-0830 / time-0845;">                        
                <span class="session-title"><a href="{{ '/program/future-faculty-forum/' | relative_url }}">Future Faculty Forum (F3)</a></span>
            </div>    
            <p class="time-slot" style="grid-row: time-0845;">8:45</p>         
            <div class="session session-f32 track-f3" style="grid-column: track-8; grid-row: time-0845 / time-0900;">                        
                <span class="session-title"><a href="{{ '/program/future-faculty-forum/' | relative_url }}">F3</a> | Welcome & Opening Remarks</span>
                <span class="session-time">8:45-9:00</span>
                <span class="session-time">Room: Sorcerer's Apprentice, 2</span>
            </div>                
            <p class="time-slot" style="grid-row: time-0900;">9:00</p>           
            <div class="session session-f33 track-f3" style="grid-column: track-8; grid-row: time-0900 / time-1000;">  
                <span class="session-title"><a href="{{ '/program/future-faculty-forum/' | relative_url }}">F3</a> | Tutorial: Professor Application Process</span>                      
                <span class="session-time">9:00-10:00</span>
                <span class="session-time">Room: Sorcerer's Apprentice, 2</span>
            </div>            
            <p class="time-slot" style="grid-row: time-1000;">10:00</p>
            <div class="session session-b track-all" style="grid-column:  track-1-start / track-8-end; grid-row: time-1000 / time-1030;">
                <span class="session-title">Break: 10:00-10:30</span><br />
            </div> 
            <p class="time-slot" style="grid-row: time-1030;">10:30</p>
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'MASSXR' %}
                    <div class="session session-w12b track-workshop" style="grid-column: track-1; grid-row: time-1030 / time-1200;">                        
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">10:30-12:00</span>
                        <span class="session-time">Room: Fantasia, A</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %} 
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'IVL' %}
                    <div class="session session-w13b track-workshop" style="grid-column: track-2; grid-row: time-1030 / time-1200;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">10:30-12:00</span>
                        <span class="session-time">Room: Fantasia, B</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>         
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'ReDigiTS' %}
                    <div class="session session-w14b track-workshop" style="grid-column: track-3; grid-row: time-1030 / time-1200;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">10:30-12:00</span>
                        <span class="session-time">Room: Fantasia, C</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>        
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'NIDIT' %}
                    <div class="session session-w15b track-workshop" style="grid-column: track-4; grid-row: time-1030 / time-1200;"> 
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">10:30-12:00</span>
                        <span class="session-time">Room: Fantasia, D</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'Data4XR' %}
                    <div class="session session-w16b track-workshop" style="grid-column: track-5; grid-row: time-1030 / time-1200;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">10:30-12:00</span>
                        <span class="session-time">Room: Fantasia, E</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}  
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'PANDAS' %}
                    <div class="session session-w17b track-workshop" style="grid-column: track-6; grid-row: time-1030 / time-1200;">                   
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">10:30-12:00</span>
                        <span class="session-time">Room: Fantasia, F</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}                          
            {% for tutorial in site.data.tutorials %}  
                {% if tutorial.id == 'T3' %}
                    <div class="session session-t3b track-tutorials" style="grid-column: track-7; grid-row: time-1030 / time-1200;">                    
                        <span class="session-title">Tutorial (cont)<br /><a href="{{ '/program/tutorials/' | relative_url }}#{{ tutorial.id }}">{{ tutorial.title }}</a></span><br/>
                        <span class="session-time">10:30-12:00</span>
                        <span class="session-time">Room: Fantasia, K-M</span>
                        <span class="session-presenter"><br />{{ tutorial.authors }}</span>
                    </div>
                {% endif %}   
            {% endfor %}   
            <div class="session session-f34 track-f3" style="grid-column: track-8; grid-row: time-1030 / time-1115;">                        
                <span class="session-title"><a href="{{ '/program/future-faculty-forum/' | relative_url }}">F3</a> | Panel 1: Differences in Universities (Geo, Research vs. Teaching Alloc.)</span>
                <span class="session-time">10:30-11:15</span>
                <span class="session-time">Room: Sorcerer's Apprentice, 2</span>
            </div>      
            <p class="time-slot" style="grid-row: time-1115;">11:15</p>          
            <div class="session session-f35 track-f3" style="grid-column: track-8; grid-row: time-1115 / time-1200;">                        
                <span class="session-title"><a href="{{ '/program/future-faculty-forum/' | relative_url }}">F3</a> | Panel 2: Lab Formation & Management</span>
                <span class="session-time">11:15-12:00</span>
                <span class="session-time">Room: Sorcerer's Apprentice, 2</span>
            </div>   
            <p class="time-slot" style="grid-row: time-1200;">12:00</p>
            <div class="session session-l track-all" style="grid-column: track-1-start / track-8-end; grid-row: time-1200 / time-1330;">
                <span class="session-title">Lunch: 12:00-13:30</span>
            </div>             
            <p class="time-slot" style="grid-row: time-1330;">13:30</p>             
            {% for workshop in site.data.workshops %} 
                {% if workshop.id == 'AVR' %}
                    <div class="session session-8 track-workshop" style="grid-column: track-1; grid-row: time-1330 / time-1530;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">13:30-15:30</span>
                        <span class="session-time">Room: Fantasia, A</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}      
            {% endfor %}  
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'OAT' %}
                    <div class="session session-9 track-workshop" style="grid-column: track-2; grid-row: time-1330 / time-1530;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">13:30-15:30</span>
                        <span class="session-time">Room: Fantasia, B</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>              
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'TrainingXR' %}
                    <div class="session session-10 track-workshop" style="grid-column: track-3; grid-row: time-1330 / time-1530;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">13:30-15:30</span>
                        <span class="session-time">Room: Fantasia, C</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'NIDIT' %}
                    <div class="session session-11 track-workshop" style="grid-column: track-4; grid-row: time-1330 / time-1530;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">13:30-15:30</span>
                        <span class="session-time">Room: Fantasia, D</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}  
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'xrWORKS' %}
                    <div class="session session-12 track-workshop" style="grid-column: track-5; grid-row: time-1330 / time-1530;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">13:30-15:30</span>
                        <span class="session-time">Room: Fantasia, E</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'ANIVAE' %}
                    <div class="session session-13 track-workshop" style="grid-column: track-6; grid-row: time-1330 / time-1530;">
                        <span class="session-title">Workshop<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">13:30-15:30</span>
                        <span class="session-time">Room: Fantasia, F</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}       
            {% endfor %}           
            <div class="session session-19 track-f3" style="grid-column: track-8; grid-row: time-1330 / time-1415;">                  
                <span class="session-title"><a href="{{ '/program/future-faculty-forum/' | relative_url }}">F3</a> | Panel 3: Challenges & Opportunities&nbsp;of Interdisciplinary Research</span>
                <span class="session-time">13:30-14:15</span>
                <span class="session-time">Room: Sorcerer's Apprentice, 2</span>
            </div>  
            <p class="time-slot" style="grid-row: time-1400;">14:00</p> 
            {% for tutorial in site.data.tutorials %}  
                {% if tutorial.id == 'T4' %}
                    <div class="session session-t3b track-tutorials" style="grid-column: track-7; grid-row: time-1400 / time-1530;">                    
                        <span class="session-title">Tutorial<br /><a href="{{ '/program/tutorials/' | relative_url }}#{{ tutorial.id }}">{{ tutorial.title }}</a></span><br/>
                        <span class="session-time">14:00-15:30</span>
                        <span class="session-time">Room: Fantasia, A</span>
                        <span class="session-presenter"><br />{{ tutorial.authors }}</span>
                    </div>
                {% endif %}   
            {% endfor %}  
            <p class="time-slot" style="grid-row: time-1415;">14:15</p>          
            <div class="session session-20 track-f3" style="grid-column: track-8; grid-row: time-1415 / time-1530;">                        
                <span class="session-title"><a href="{{ '/program/future-faculty-forum/' | relative_url }}">F3</a> | Tutorial: Review & Critique of Application Materials (Research, Teaching & Diversity Statements)</span>
                <span class="session-time">14:15-15:30</span>
                <span class="session-time">Room: Sorcerer's Apprentice, 2</span>
            </div>
            <p class="time-slot" style="grid-row: time-1530;">15:30</p>
            <div class="session session-16 track-all" style="grid-column: track-1 / track-8; grid-row: time-1530 / time-1600;">
                <span class="session-title">Break: 15:30-16:00</span>
            </div>  
            <p class="time-slot" style="grid-row: time-1600;">16:00</p>
            {% for workshop in site.data.workshops %} 
                {% if workshop.id == 'AVR' %}
                    <div class="session session-8 track-workshop" style="grid-column: track-1; grid-row: time-1600 / time-1730;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">16:00-17:30</span>
                        <span class="session-time">Room: Fantasia, A</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}      
            {% endfor %}  
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'OAT' %}
                    <div class="session session-9 track-workshop" style="grid-column: track-2; grid-row: time-1600 / time-1730;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">16:00-17:30</span>
                        <span class="session-time">Room: Fantasia, B</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>              
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'TrainingXR' %}
                    <div class="session session-10 track-workshop" style="grid-column: track-3; grid-row: time-1600 / time-1730;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">16:00-17:30</span>
                        <span class="session-time">Room: Fantasia, C</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>            
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'NIDIT' %}
                    <div class="session session-11 track-workshop" style="grid-column: track-4; grid-row: time-1600 / time-1730;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">16:00-17:30</span>
                        <span class="session-time">Room: Fantasia, D</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}  
            {% for workshop in site.data.workshops %}   
                {% if workshop.id == 'xrWORKS' %}
                    <div class="session session-12 track-workshop" style="grid-column: track-5; grid-row: time-1600 / time-1730;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">16:00-17:30</span>
                        <span class="session-time">Room: Fantasia, E</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}      
            {% endfor %}   
            {% for workshop in site.data.workshops %}  
                {% if workshop.id == 'ANIVAE' %}
                    <div class="session session-13 track-workshop" style="grid-column: track-6; grid-row: time-1600 / time-1730;">
                        <span class="session-title">Workshop (cont)<br/><a href="{{ '/program/workshop/' | relative_url }}#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></span><br/>
                        <span class="session-time">16:00-17:30</span>
                        <span class="session-time">Room: Fantasia, F</span>
                        <span class="session-presenter"><br />{{ workshop.organiser }}</span>
                    </div>
                {% endif %}       
            {% endfor %}          
            <div class="session session-22 track-f3" style="grid-column: track-8; grid-row: time-1600 / time-1645;">                        
                <span class="session-title"><a href="{{ '/program/future-faculty-forum/' | relative_url }}">F3</a> | Speed Advising</span>
                <span class="session-time">16:00-16:45</span>
                <span class="session-time">Room: Sorcerer's Apprentice, 2</span>
            </div>       
            {% for tutorial in site.data.tutorials %}  
                {% if tutorial.id == 'T5' %}
                    <div class="session session-t3b track-tutorials" style="grid-column: track-7; grid-row: time-1600 / time-1730;">                    
                        <span class="session-title">Tutorial<br /><a href="{{ '/program/tutorials/' | relative_url }}#{{ tutorial.id }}">{{ tutorial.title }}</a></span><br/>
                        <span class="session-time">16:00-17:30</span>
                        <span class="session-time">Room: Fantasia, K-M</span>
                        <span class="session-presenter"><br />{{ tutorial.authors }}</span>
                    </div>
                {% endif %}   
            {% endfor %}     
            <p class="time-slot" style="grid-row: time-1645;">16:45</p>   
            <div class="session session-23 track-f3" style="grid-column: track-8; grid-row: time-1645 / time-1700;">                        
                <span class="session-title"><a href="{{ '/program/future-faculty-forum/' | relative_url }}">F3</a> | Closing Remarks & Feedback for Future F3 Events</span>
                <span class="session-time">16:45-17:00</span>
                <span class="session-time">Room: Sorcerer's Apprentice, 2</span>
            </div> 
        </div>
    </div> 
</div>