---
layout: ieeevr-default
title: "Panels"
---

<link rel="stylesheet" href="{{ '/assets/css/tableStyles.css' | relative_url }}">

<h1>Panels -- Tentative Program</h1>

<div>
    <table class="styled-table" style="font-size: 0.9em; ">
        <tr>
            <th>Monday, March 27, 2024, Shanghai UTC+8</th>
            <th></th>
        </tr>
        {% for panel in site.data.panels %}
        {% if panel.day == 'Monday, March 27, 2024' %}
        <tr>
            <td style="font-size: 0.9em;"><a href="#{{ panel.id }}">{{ panel.name }}</a></td>
            <td>{{ panel.starttime }} - {{ panel.panel }}</td>
            <td>{{ panel.room }}</td>
        </tr>
        {% endif %}
        {% endfor %}
    </table>
</div>
<div>
    <table class="styled-table" style="font-size: 0.9em; ">
        <tr>
            <th>Tuesday, March 28, 2024, Shanghai UTC+8</th>
            <th></th>
        </tr>
        {% for panel in site.data.panels %}
        {% if panel.day == 'Tuesday, March 28, 2024' %}
        <tr>
            <td style="font-size: 0.9em;"><a href="#{{ panel.id }}">{{ panel.name }}</a></td>
            <td>{{ panel.starttime }} - {{ panel.panel }}</td>
            <td>{{ panel.room }}</td>
        </tr>
        {% endif %}
        {% endfor %}
    </table>
</div>
<div>
    <table class="styled-table" style="font-size: 0.9em; ">
        <tr>
            <th>Wednesday, March 29, 2024, Shanghai UTC+8</th>
            <th></th>
        </tr>
        {% for panel in site.data.panels %}
        {% if panel.day == 'Wednesday, March 29, 2024' %}
        <tr>
            <td style="font-size: 0.9em;"><a href="#{{ panel.id }}">{{ panel.name }}</a></td>
            <td>{{ panel.starttime }} - {{ panel.panel }}</td>
            <td>{{ panel.room }}</td>
        </tr>
        {% endif %}
        {% endfor %}
    </table>
</div>

{% for day in site.data.days %}
<div>
    {% for panel in site.data.panels %}
    {% if panel.day == day.day' %}

    <h2 id="{{ panel.id }}">{{ panel.name }}: {{ panel.title }}   ({{  panel.type  }})</h2>
    
    <p><strong>{{ panel.day }}, {{ panel.start }}-{{ panel.end }}, {{ panel.timezone }}, {{ panel.room }}</strong></p>

    <h3>Moderator</h3>
    <p>
        <strong style="color: black">{{ panel.moderator }}</strong>
    </p>

    <h3>Panelists</h3>
    {% assign authornames = panel.panelists | split: ";" %}
    {% for name in authornames %}
    <p>
    {{ name }}
    </p>
    {% endfor %}

    <h3>Abstract</h3>
    <p>
    {{ panel.abstract }}
    </p>

    {% endif %}
    {% endfor %}
</div>
{% endfor %}


<!-- 
<div>
    {% for panel in site.data.panels %}
    {% if panel.id == 'P3' %}
    <h2 id="{{ panel.id }}">Panel: {{ panel.title}}</h2>
    
    {% for event in site.data.events %}
    {% if event.id == panel.id %}
    {% if event.location %}
    <div class="notice--info">
        <strong style="padding-bottom: 5px;">Take me to the event:</strong>
        <p>
            <strong style="color: black;">Virbela Location:</strong> {{ event.location }} (<a href="/2021/attend/virbela-instructions/#map">MAP</a>)

            {% if event.stream-url %}
            <br />
            {% if event.aindanaoaconteceu %}
            <strong style="color: black;">Watch video stream live:</strong> <a href="{{ event.stream-url }}" target="_blank">HERE</a>
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
    
    <p style="font-size: 0.8em;">{{ panel.day }}, {{panel.start}}, {{ panel.timezone }}</p>
    
    
    <h3 >Description</h3>
    <p>
        Humans are social beings, and even in VR we typically do not want to be alone. As VR becomes increasingly utilized for a wide range of applications, virtual humans are expected to play increasingly important roles.  A lot of research has concentrated on making virtual humans look and move photo-realistically. Here we argue that the fundamental question is what makes virtual humans effective, in the sense that people respond to them in a way that is useful for and predicted by the application. For example, if the purpose of the application is to make people laugh, then no matter how photorealistic or how expressive the virtual humans involved might be, if the human participants do not laugh then the application would have failed. So, the question shifts from ‘How realistic can we make these virtual humans’ to ‘How should the virtual humans look and behave in order to make you laugh as a human comedian would’ - which may not require high levels of animation realism and photorealism.
    </p>
    <p>
        In this panel, we will discuss the theoretical background behind how effective responses might be elicited by virtual humans and the methodologies used to measure the impact they have on participants. We suggest that in VR the most important question about a virtual human is not: “does it look real”, but “do participants respond to it as if it were a real human”. For example, does the virtual psychotherapist contribute to your wellbeing? This shifts the focus from issues intensively studied in the computer graphics and animation communities to questions that are unique to VR. 
    </p>
    <p>
        We will discuss how eliciting realistic responses is related to all levels of virtual human design and development:
    </p>
    <ul>
        <li>With respect to appearance, are there some factors more important than others in order to elicit realistic responses?</li>
        <li>In terms of character animation, what are the key features required of a virtual human to be plausible and thus trigger more realistic responses?</li> 
        <li>When it comes to multimodal integrated behavior, such as combined gesture, speech, and facial expression -- what are the key factors that could help maintain consistency? </li>
        <li>Because VR is interactive, virtual humans have to be responsive to user inputs in real-time. However, human inputs are rich and sometimes very subtle. What is the best practice here?</li>
        <li>One of the key application areas for virtual humans is training. For instance, medical students could be routinely spending 1-2 hours with virtual patients to practise their consultation skills. In this situation, the question is: how do you get humans to want to spend time with virtual humans? How does one frame interactions with virtual humans so people know how and why they should interact with them?</li>
    </ul>
    <p>
        Finally, as our essential question for any VR application involving virtual humans is: “do participants respond to them as if they were real?” We will wrap up our discussion with the following:
    </p>
    <ul>
        <li>Give one example of a novel measurement you used that provides convincing evidence that participants did respond towards it as if it were real.</li>
    </ul>
    
    
    <h3 >Moderator</h3>
    <p>
        <strong style="color: black">Xueni Pan, Department of Computing, Goldsmiths, University of London, UK [x.pan@gold.ac.uk]</strong>
    </p>
    <p>
        Xueni Pan is an Assistant Prof. in VR in Virtual Reality at Goldsmiths College, University of London. She worked at UCL in both Computer Science and Institute of Cognitive Neuroscience. Dr Pan has a unique interdisciplinary research profile, with journal and conference publications on both VR technology and social neuroscience. Her work has featured on the BBC, in New Scientist magazine and the Wall Street Journal. Her Coursera VR specialisation has attracted over 80,000 registered learners globally, and she co-leads on the MA/MSc in Virtual and Augmented Reality at Goldsmith’s Computing.
    </p>
    
    <h3 >Panelists</h3>
    <p>
        <strong style="color: black">Doron Friedman, Sammy Ofer School of Communications, Israel [doronf@idc.ac.il]</strong>
    </p>
    <p>
        Doron Friedman an Associate Prof. in the Sammy Ofer School of Communications and the head of the Advanced Reality Lab (https://arlidc.ac.il), Israel. Since 2008, Prof. Friedman and his lab members have been involved in several national and international projects in the areas of telepresence, VR, and advanced human computer interfaces. Doron's research is highly multidisciplinary and has been published in top scientific journals and peer reviewed conferences, including Artificial Intelligence, Human Computer Interaction, Journal of Neural Engineering, Journal of Neuroscience, PNAS, and more. Friedman and his lab members also frequently take part in real world industry projects.
    </p>
    <p>
        <strong style="color: black">Benjamin Lok, Computer and Information Sciences and Engineering Department, University of Florida, USA [lok@cise.ufl.edu] 
</strong>
    </p>
    <p>
        Ben Lok is a Professor in the Computer and Information Sciences and Engineering Department at the University of Florida and entrepreneur, having previously co-founded Shadow Health. Shadow Health’s virtual humans are used by half of all nursing students and impacts nearly every person in the US and Canada. Professor Lok's research focuses on using virtual humans and mixed reality to train communication skills within the areas of virtual environments, human-computer interaction, and computer graphics. He was awarded the 2019 UF Innovator of the Year and multiple best paper awards involving virtual human research.
    </p>
    <p>
        <strong style="color: black">Mel Slater, Event Lab, University of Barcelona, Spain [melslater@ub.edu]
</strong>
    </p>
    <p>
        Mel Slater is co-Director of the Event Lab at the University of Barcelona. He was previously Professor of Virtual Environments at University College London. He has been involved in research in virtual reality since the early 1990s and has been the first supervisor of more than 40 students who achieved their PhDs in graphics and virtual reality since 1989. He was awarded the 2005 IEEE Virtual Reality Career Award: ‘In Recognition of Pioneering Achievements in Theory and Applications of Virtual Reality’. He is Field Editor of Frontiers in Virtual Reality. He is co-founder of Virtual Bodyworks.
    </p>

        {% endif %}
    {% endfor %}
</div>

 -->
