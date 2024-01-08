---
layout: ieeevr-default
title: "Program Overview"
---


<style>  
    /*************************
    * Accordian Styling
    *************************/ 
    .ui-state-active,
    .ui-widget-content .ui-state-active,
    .ui-widget-header .ui-state-active,
    a.ui-button:active,
    .ui-button:active,
    .ui-button.ui-state-active:hover {
        border: 1px solid #12a6c9;
        background: #12a6c9;
        font-weight: normal;
        color: #ffffff;
    }
    .ui-icon-background,
    .ui-state-active .ui-icon-background {
        border: #12a6c9;
        background-color: #ffffff;
    }

    /****************************************************************************************************
    * GRID SCHEDULE LAYOUT: https://css-tricks.com/building-a-conference-schedule-with-css-grid
    ****************************************************************************************************/
    @media screen and (min-width:700px) {
        .schedule-sat {
            display: grid;
            grid-gap: 1em;
            grid-template-rows:
            [tracks] auto [time-0800] 0.5fr [time-0830] 0.5fr [time-0900] 0.5fr [time-0930] 0.5fr [time-1000] 0.5fr [time-1030] 0.5fr [time-1100] 0.5fr [time-1130] 0.5fr [time-1200] 0.5fr [time-1230] 0.5fr [time-1300] 0.5fr [time-1330] 0.5fr [time-1400] 0.5fr [time-1430] 0.5fr [time-1500] 0.5fr [time-1530] 0.5fr [time-1600] 0.5fr [time-1630] 0.5fr [time-1700] 0.5fr [time-1730] 
            /*0.5fr [time-1800] 0.5fr [time-1830] 0.5fr [time-1900] 0.5fr*/
            ;
            /* Note 1:
            Use 24hr time for gridline names for simplicity

            Note 2: Use "auto" instead of "1fr" for a more compact schedule where height of a slot is not proportional to the session length. Implementing a "compact" shortcode attribute might make sense for this!
            Try 0.5fr for more compact equal rows. I don't quite understand how that works :)
            */
            
            grid-template-columns:
            [times] 4em [track-1-start] 1fr [track-1-end track-2-start] 1fr [track-2-end track-3-start] 1fr [track-3-end track-4-start] 1fr [track-4-end track-5-start] 1fr [track-5-end track-6-start] 1fr [track-6-end];
        }

        .schedule-sun {
            display: grid;
            grid-gap: 1em;
            grid-template-rows:
            [tracks] auto [time-0800] 0.5fr [time-0830] 0.5fr [time-0900] 0.5fr [time-0930] 0.5fr [time-1000] 0.5fr [time-1030] 0.5fr [time-1100] 0.5fr [time-1130] 0.5fr [time-1200] 0.5fr [time-1230] 0.5fr [time-1300] 0.5fr [time-1330] 0.5fr [time-1400] 0.5fr [time-1430] 0.5fr [time-1500] 0.5fr [time-1530] 0.5fr [time-1600] 0.5fr [time-1630] 0.5fr [time-1700] 0.5fr [time-1730] 
            /*0.5fr [time-1800] 0.5fr [time-1830] 0.5fr [time-1900] 0.5fr*/
            ;
            /* Note 1:
            Use 24hr time for gridline names for simplicity

            Note 2: Use "auto" instead of "1fr" for a more compact schedule where height of a slot is not proportional to the session length. Implementing a "compact" shortcode attribute might make sense for this!
            Try 0.5fr for more compact equal rows. I don't quite understand how that works :)
            */
            
            grid-template-columns:
            [times] 4em [track-1-start] 1fr [track-1-end track-2-start] 1fr [track-2-end track-3-start] 1fr [track-3-end track-4-start] 1fr [track-4-end track-5-start] 1fr [track-5-end track-6-start] 1fr [track-6-end];
        }
    }

    .time-slot {
        font-size:.75em;
        font-weight: normal;
        text-decoration: none;
        grid-column: times;
    }

    .track-slot {
        display: none; /* hidden on small screens and browsers without grid support */
    }

    @supports( display:grid ) {
        @media screen and (min-width:700px) {
            .track-slot {
                display: block;
                padding: 10px 5px 5px;
                position: sticky;
                top: 0;
                z-index: 1000;
                background-color: rgba(255,255,255,.9);
            }
        }
    }

    /* Small-screen & fallback styles */
    .session {
        margin-bottom:  1em;
    }

    @supports( display:grid ) {
        @media screen and (min-width: 700px) {
            .session {
                margin: 0;
            } 
        }
    }

    /*************************
    * VISUAL STYLES
    * Design-y stuff ot particularly important to the demo
    *************************/
    .session {
        padding: .5em;
        border-radius: 2px;
        font-size: 14px;
        box-shadow:
            rgba(255,255,255,.6) 1px 1px 0,
            rgba(0,0,0,.3) 4px 4px 0;
    }

    .session-title,
    .session-time,
    .session-track,
    .session-presenter {
     display: block;
    }

    .session-title {
        margin: 0;
        font-size: 1em;
    }

    .session-title a {
        color: #fff;
        text-decoration-style: solid;
    
        &:hover {
            text-decoration-style: none;
        }  
    }

    .track-slot{
        font-size:.75em;
    }
    .track-green {
        background-color: #1fb55a;
        color: #fff;
    }
    .track-rose {
        background-color: #d30f45;
        color: #fff;
    }
    .track-lavender {
        background-color: #c488c3;
        color: #fff;
    }
    .track-orange {
        background-color: #f5725e;
        color: #fff;
    }
    .track-blue {
        background-color: #0c5789;
        color: #fff;
    }
    .track-lightpurple {
        background-color: #c488c3;
        color: #fff;
    } 
    .track-pink {
        background-color: #EF127F;
        color: #fff;
    }

    .track-all {
        display: flex;
        justify-content: center;
        align-items: center;
        background: #ebf5f8;
        color: #000;
        box-shadow: none;
    }

    .text {
        max-width: 750px;
        font-size: 18px;
        margin: 0 auto 50px;
    }

    .meta {
        color: #555;
        font-style: italic;
    }

    .meta a {
        color: #555;
    }

    hr {
        margin: 40px 0;
    }     
</style>
<script>
    $( function() {
        $( "#accordion" ).accordion({
            collapsible: true,
			heightStyle: "content"
        });
    } );
</script>

<h1 id="schedule-heading">Program Overview</h1>
<div class="notice--info alignCenter bold" style="font-size: 0.9em !important;">
    Please note that all times are given in Orlando, Florida USA local time, EDT (UTC-4).
</div>
<div id="accordion">
    <h3>Saturday, 16 March 2024</h3>
    <div class="schedule-sat" aria-labelledby="March 16 - Workshop Schedule"> 
        {% for workshop in site.data.workshops %}  
            <h2 class="time-slot" style="grid-row: time-0800;">8:00am</h2>
            {% if workshop.id == 'XRGaming' %}
                <div class="session session-1 track-blue" style="grid-column: track-1; grid-row: time-0800 / time-1200;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">8:00am - 12:00pm</span>
                    <span class="session-track">Room: 1</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>
            {% endif %}
            {% if workshop.id == 'KELVAR' %}
                <div class="session session-2 track-blue" style="grid-column: track-2; grid-row: time-0800 / time-1200;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">8:00am - 12:00pm</span>
                    <span class="session-track">Room: 2</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>         
            {% endif %}
            {% if workshop.id == 'LocXR' %}
                <div class="session session-3 track-blue" style="grid-column: track-3; grid-row: time-0800 / time-1200;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">8:00am - 12:00pm</span>
                    <span class="session-track">Room: 3</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>        
            {% endif %}
            {% if workshop.id == 'CLEVER' %}
                <div class="session session-4 track-blue" style="grid-column: track-4; grid-row: time-0800 / time-1200;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">8:00am - 12:00pm</span>
                    <span class="session-track">Room: 4</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>
            {% endif %}
            {% if workshop.id == 'XRIOS' %}
                <div class="session session-5 track-blue" style="grid-column: track-5; grid-row: time-0800 / time-1200;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">8:00am - 12:00pm</span>
                    <span class="session-track">Room: 5</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>
            {% endif %}
            {% if workshop.id == 'IDEATExR' %}
                <div class="session session-6 track-blue" style="grid-column: track-6; grid-row: time-0800 / time-1200;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">8:00am - 12:00pm</span>
                    <span class="session-track">Room: 6</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>
            {% endif %}
            <h2 class="time-slot" style="grid-row: time-1200;">12:00pm</h2>

            <div class="session session-7 track-all" style="grid-column: track-1-start / track-6-end; grid-row: time-1200 / time-1330;">
            <h3 class="session-title">Lunch: 12:00-1:30</h3>
            </div>

            <h2 class="time-slot" style="grid-row: time-1330;">1:30pm</h2>

            {% if workshop.id == 'WISP' %}
                <div class="session session-8 track-blue" style="grid-column: track-1; grid-row: time-1330 / time-1730;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">1:30pm - 5:30pm</span>
                    <span class="session-track">Room: 1</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>            
            {% endif %}
            {% if workshop.id == 'VHCIE' %}
                <div class="session session-9 track-blue" style="grid-column: track-2; grid-row: time-1330 / time-1730;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">1:30pm - 5:30pm</span>
                    <span class="session-track">Room: 2</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>              
            {% endif %}
            {% if workshop.id == 'GEMINI' %}
                <div class="session session-10 track-blue" style="grid-column: track-3; grid-row: time-1330 / time-1730;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">1:30pm - 5:30pm</span>
                    <span class="session-track">Room: 3</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>            
            {% endif %}
            {% if workshop.id == 'ENPTXR' %}
                <div class="session session-11 track-blue" style="grid-column: track-4; grid-row: time-1330 / time-1730;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">1:30pm - 5:30pm</span>
                    <span class="session-track">Room: 4</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>
            {% endif %}
            {% if workshop.id == 'Data4XR' %}
                <div class="session session-12 track-blue" style="grid-column: track-5; grid-row: time-1330 / time-1730;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">1:30pm - 5:30pm</span>
                    <span class="session-track">Room: 5</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>
            {% endif %}
            {% if workshop.id == 'IDEATExR' %}
                <div class="session session-13 track-blue" style="grid-column: track-6; grid-row: time-1330 / time-1730;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">1:30pm - 5:30pm</span>
                    <span class="session-track">Room: 6</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>
            {% endif %}       
        {% endfor %}  
    </div> 

    <h3>Sunday, 17 March 2024</h3> 
    <div class="schedule-sun" aria-labelledby="March 16 - Workshop Schedule">  
        {% for workshop in site.data.workshops %}  
            <h2 class="time-slot" style="grid-row: time-0800;">8:00am</h2>
            {% if workshop.id == 'MASSXR' %}
                <div class="session session-1 track-blue" style="grid-column: track-1; grid-row: time-0800 / time-1200;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">8:00am - 12:00pm</span>
                    <span class="session-track">Room: 1</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>
            {% endif %}
            {% if workshop.id == 'IVL' %}
                <div class="session session-2 track-blue" style="grid-column: track-2; grid-row: time-0800 / time-1200;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">8:00am - 12:00pm</span>
                    <span class="session-track">Room: 2</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>         
            {% endif %}
            {% if workshop.id == 'ReDigiTS' %}
                <div class="session session-3 track-blue" style="grid-column: track-3; grid-row: time-0800 / time-1200;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">8:00am - 12:00pm</span>
                    <span class="session-track">Room: 3</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>        
            {% endif %}
            {% if workshop.id == 'WSR' %}
                <div class="session session-4 track-blue" style="grid-column: track-4; grid-row: time-0800 / time-1200;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">8:00am - 12:00pm</span>
                    <span class="session-track">Room: 4</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>
            {% endif %}
            {% if workshop.id == 'PANDAS' %}
                <div class="session session-5 track-blue" style="grid-column: track-5; grid-row: time-0800 / time-1200;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">8:00am - 12:00pm</span>
                    <span class="session-track">Room: 5</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>
            {% endif %}
            {% if workshop.id == 'NIDIT' %}
                <div class="session session-6 track-blue" style="grid-column: track-6; grid-row: time-0800 / time-1200;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">8:00am - 12:00pm</span>
                    <span class="session-track">Room: 6</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>
            {% endif %}
            <h2 class="time-slot" style="grid-row: time-1200;">12:00pm</h2>

            <div class="session session-7 track-all" style="grid-column: track-1-start / track-6-end; grid-row: time-1200 / time-1330;">
                <h3 class="session-title">Lunch: 12:00-1:30</h3>
            </div>

            <h2 class="time-slot" style="grid-row: time-1330;">1:30pm</h2>

            {% if workshop.id == 'TrainingXR' %}
                <div class="session session-8 track-blue" style="grid-column: track-1; grid-row: time-1330 / time-1730;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">1:30pm - 5:30pm</span>
                    <span class="session-track">Room: 1</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>            
            {% endif %}
            {% if workshop.id == 'OAT' %}
                <div class="session session-9 track-blue" style="grid-column: track-2; grid-row: time-1330 / time-1730;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">1:30pm - 5:30pm</span>
                    <span class="session-track">Room: 2</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>              
            {% endif %}
            {% if workshop.id == 'AVR' %}
                <div class="session session-10 track-blue" style="grid-column: track-3; grid-row: time-1330 / time-1730;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">1:30pm - 5:30pm</span>
                    <span class="session-track">Room: 3</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>            
            {% endif %}
            {% if workshop.id == 'xrWORKS' %}
                <div class="session session-11 track-blue" style="grid-column: track-4; grid-row: time-1330 / time-1730;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">1:30pm - 5:30pm</span>
                    <span class="session-track">Room: 4</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>
            {% endif %}
            {% if workshop.id == 'ANIVAE' %}
                <div class="session session-12 track-blue" style="grid-column: track-5; grid-row: time-1330 / time-1730;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">1:30pm - 5:30pm</span>
                    <span class="session-track">Room: 5</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>
            {% endif %}
            {% if workshop.id == 'NIDIT' %}
                <div class="session session-13 track-blue" style="grid-column: track-6; grid-row: time-1330 / time-1730;">
                    <h3 class="session-title"><a href="\program\workshop\#{{ workshop.id }}">{{ workshop.title }} ({{ workshop.id }})</a></h3><br/>
                    <span class="session-time">1:30pm - 5:30pm</span>
                    <span class="session-track">Room: 6</span>
                    <span class="session-presenter">{{ workshop.organiser }}</span>
                </div>
            {% endif %}       
        {% endfor %}  
    </div> 
</div>