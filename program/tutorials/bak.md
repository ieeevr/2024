
<div>
    {% for tutorial in site.data.tutorials %}
    {% if tutorial.id == 'T1' %}
    <h2 id="{{ tutorial.id }}">{{ tutorial.name }}: {{ tutorial.title}}</h2>

    <!-- TAKE ME TO THE EVENT START 
    {% for event in site.data.events %}
    {% if event.id == 'T1' %}
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
    TAKE ME TO THE EVENT END -->
    <p>
        {{ tutorial.day }}, {{ tutorial.starttime }}-{{ tutorial.endtime }}, {{ tutorial.timezone }}, {{ tutorial.room }}
    </p>
    <p>
        <strong>Organizers</strong>
    </p>
    <p>
        Aditi Majumder, Department of Computer Science, University of California, Irvine.<br />
        Muhammad Twaha Ibrahim, Department of Computer Science, University of California, Irvine.<br />
    </p>
    <!-- <p>
        <strong style="font-size: 0.8em;color: black"> {{ tutorial.schedule1 }}, {{ tutorial.timezone1 }}</strong>
    </p> -->
    <h3>Summary</h3>
    <p>Spatially augmented reality (SAR) uses projections to augment
    physical surfaces with digital information. SAR has been the focus of
    enormous research in the past, culminating in works that can generate
    geometrically registered and photometrically seamless multi-projector
    displays automatically on complex shapes. Today, such systems are largely
    limited to static and rigid surfaces. More recent advances have enabled SAR
    on non-rigid, dynamic surfaces as well. In addition to the challenges faced
    with rigid static surfaces, SAR on non-rigid, dynamic surfaces introduces a
    host of new technical challenges that must be overcome before they are ready
    for general use.
    </p>
    <p>
    This tutorial will present an overview of automated geometric registration
    techniques to build SAR systems on non-rigid surfaces. It will discuss the
    complexities introduced by a non-rigid, dynamic surface for projection, as
    well as how prior research has attempted to overcome those challenges.
    Finally, it will illustrate various applications for non-rigid SAR systems.
    </p>
    <h3>Technical Level</h3>
    <p>
    The course will be self-contained and does not assume
    prior knowledge on SAR. Familiarity and prior exposure to basic
    graphics/vision techniques for geometric registration and color calibration
    will be helpful. A basic understanding of linear algebra is required.
    </p>
    <h3>Intended Audience</h3>
    <p>
    The tutorial targets students, professionals and
    practitioners who would like to build SAR systems using one or more
    projectors. Though the tutorial focuses on non-rigid, dynamic surfaces, the
    first part of the tutorial provides background knowledge that comprises SAR
    systems on rigid surfaces. This course can be extremely useful for beginners
    who want to start research in this domain and for professionals who want to
    build SAR systems.
    </p>
    <h3>Value</h3>
    <p>
    The goal of this tutorial is to impart sufficient information that the
    audience understands the current research, its limitations as well as
    remaining open challenges in building their own automated SAR systems for
    non-rigid, dynamic surfaces and objects.
    </p>
    
    {% endif %}
    {% endfor %}
</div>

<div>
    {% for tutorial in site.data.tutorials %}
    {% if tutorial.id == 'T2' %}
    <h2 id="{{ tutorial.id }}">{{ tutorial.name }}: {{ tutorial.title}}</h2>

    <!-- TAKE ME TO THE EVENT START
    {% for event in site.data.events %}
    {% if event.id == 'T2' %}
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
    TAKE ME TO THE EVENT END-->

    <p>
        {{ tutorial.day }}, {{ tutorial.starttime }}-{{ tutorial.endtime }}, {{ tutorial.timezone }}, {{ tutorial.room }}
    </p>

    <p>
        <strong>Organizers</strong>
    </p>
    
    <p>
        Anthony Steed, University College London<br />
        Sebastian Friston, University College London<br />
        Ben Congdon, University College London<br />
    </p>

    <!-- 
    <p>
        <strong style="font-size: 0.8em;color: black"> {{ tutorial.schedule1 }}, {{ tutorial.timezone1 }}</strong>
    </p> -->
    <h3>Summary</h3>
    <p>
        In this tutorial we will demonstrate how to construct social virtual reality applications using our Ubiq tool. Ubiq is open source and designed to be easily extensible. It enables development of applications or systems that would be difficult or time-consuming on commercial systems. The tutorial is targeted at participants with some technical background. 
    </p>
    <h3>Background</h3>
    <p>
        One of the most promising applications of consumer virtual reality technology is its use for remote collaboration. A very wide variety of social virtual reality (SVR) applications are now available; from competitive games amongst small numbers of players; through to conference-like setups supporting dozens of visitors. Ubiq is an open source tool that allows developers to very quickly build SVR applications. In this short tutorial, we will introduce some of the capabilities of Ubiq, demonstrate some of the tools it has, and work through a complete example of how to build a non-trivial application including custom distributed behaviours. The tutorial is backed up by extensive online documentation, other explanatory videos and a growing set of more complex example systems.
    </p>
    <h3>Intended Audience and Technical Level</h3>
    <p>
        The tutorial will be of value to any student, researcher or professional who wants to develop their own social VR applications, or just wants to get a grounding in what the challenges in building such applications are. Some experience with Unity would be very useful, but not necessary as the practical part will do a guided walkthrough of the specific issues of using Unity and will not rely on prior knowledge. More experienced participants will be able to implement their own ideas rather than follow our specific guidance.
    </p>
    <h3>Expected Value</h3>
    <p>
        In this tutorial, participants will learn about SVR technologies and how to build their own system using the Ubiq toolkit in Unity. We will give a short explanation of the difficulties of using many of the commercial platforms for research and the, through examples, show how it is relatively straightforward to implement quite sophisticated applications using Ubiq. We will also give an overview of some of the open source applications built using Ubiq, including tools for running distributed and remote experiments. 
    </p>

    {% endif %}
    {% endfor %}

</div>

<div>
    {% for tutorial in site.data.tutorials %}
    {% if tutorial.id == 'T3' %}
    <h2 id="{{ tutorial.id }}">{{ tutorial.name }}: {{ tutorial.title}}</h2>

    <!-- TAKE ME TO THE EVENT START 
    {% for event in site.data.events %}
    {% if event.id == 'T3' %}
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
     TAKE ME TO THE EVENT END-->

    <p>
        {{ tutorial.day }}, {{ tutorial.starttime }}-{{ tutorial.endtime }}, {{ tutorial.timezone }}, {{ tutorial.room }}
    </p>

    <p>
        <strong>Organizers</strong>
    </p>
    <p>
        Shen Song, Senior Solution Architecture, Nividia<br />
    </p>

    <!-- <p>
        <strong style="font-size: 0.8em;color: black"> {{ tutorial.schedule1 }}, {{ tutorial.timezone1 }}</strong>
    </p> -->

    <p>
        Creating interactive XR environments is becoming essential for researchers in XR areas. With the modern game engine, building an XR environment is reasonably convenient. However, developing an interactive XR environment for research purposes, such as usability studies, still needs many jobs in the working pipeline, including creating 3D models, animations, lighting, etc., which would require the research team to have different members for different works in the pipeline to finish a quality XR environments. How to help the team collaborate efficiently or how to create an XR POC environment quickly is challenging. For example, the entire pipeline might need various tools, such as the tools for 3D modeling, animation, lighting, programming, real-time engine, etc. Most of the time, it is teamwork. NVIDIA Omniverse is a platform that could connect those different tools and create a collaborative working pipeline. In this half-day tutorial, a new platform from NVIDIA will be introduced called NIVIDA Omniverse. The session will include how to start working with NVIDIA Omniverse, set up the environment, build an XR environment quickly for a POC by leveraging the resources and AI capabilities in NVIDIA Omniverse, and how to present the XR environments to the users using the cloud-based Omniverse XR.
    </p>
    <h3>Intended Audience and value</h3>
    <p>
        Since NVIDIA Omniverse will provide a collaborative pipeline for the entire design and development team, this tutorial will benefit any students, researchers, or professionals who need to design and develop XR environments, manage the projects, and who will review the work. Participants with experience in using the tools like Unity, UE, Maya, Blender, and Autodesk would be helpful but unnecessary.
    </p>
    <p>
        In this tutorial, the participants will learn how to work with NVIDIA Omniverse in their XR design and development. NVIDIA Omniverse is free for any individual developer. The participants will also have a glance at how NVIDIA Omniverse Enterprise could improve the collaborative working pipeline. With our real customers’ experiences, using NVIDIA Omniverse with our latest RTX GPUs could improve teamwork and rendering efficiency, creating more realistic rendering results with RTX on. 
    </p>

    {% endif %}
    {% endfor %}

</div>

<div>
    {% for tutorial in site.data.tutorials %}
    {% if tutorial.id == 'T4' %}
    <h2 id="{{ tutorial.id }}">{{ tutorial.name }}: {{ tutorial.title}}</h2>

    <!-- TAKE ME TO THE EVENT START 
    {% for event in site.data.events %}
    {% if event.id == 'T4' %}
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
     TAKE ME TO THE EVENT END-->

    <p>
        {{ tutorial.day }}, {{ tutorial.starttime }}-{{ tutorial.endtime }}, {{ tutorial.timezone }}, {{ tutorial.room }}
    </p>

    <p>
        <strong>Organizers</strong>
    </p>
    <p>
        Dongdong Weng, Beijing Institute of Technology<br />
    </p>
    <!--
    <p>
        <strong style="font-size: 0.8em;color: black"> {{ tutorial.schedule1 }}, {{ tutorial.timezone1 }}</strong>
    </p> -->

    <p>
        A virtual digital human is broadly defined as a computer application that presents and interacts with a humanoid appearance, integrating computer graphics, computer vision, intelligent speech, natural language processing and other technologies. It can be used for digital content generation and human-computer interaction to help improve content production efficiency and user experience. In a narrow sense, it is a digital twin of a human being that exists in the non-physical world, created and used by computer means such as computer graphics, graphics rendering, motion capture, deep learning, speech synthesis, etc. It is a comprehensive product with multiple human characteristics (external appearance characteristics, human performance ability, human interaction ability, etc.). In order to make the digital human more realistic, it is necessary to construct a highly realistic appearance of the digital human through various technical means. Such construction techniques are mainly divided into static and dynamic aspects. The mainstream static modeling technology captures multiple photos of the actor through camera arrays, thus achieving 3D reconstruction of the face and body. The light field capture technology represented by Lightstage, on the other hand, solves the problem by capturing sequential photos of the human face under different lighting modes, so as to obtain multiple skin material textures required for high fidelity rendering. The dynamic construction of digital human is mainly based on 4D acquisition technology, which expands the temporal dimension based on facial reconstruction. Multi-view geometry is used for continuous and batch reconstruction using camera arrays. The generated 4D model sequences can record clearly the nonlinear deformation characteristics of the human face in motion, breaking through the limitations of traditional 3D animation technology in realism.
    </p>
    <h3>Intended Audience and value</h3>
    <p>
        This course will be of value to any student, researcher and professional who wants to develop digital humans for PGC and AIGC. There are no mandatory requirements for participants' digital human production experience and skill level for the course. Anyone with experience in digital human production will be able to find ways to improve the efficiency and quality of digital human production in the content.
    </p>
    <p>
        In this tutorial, an overview of the production path and difficulties of digital figures will be presented. Participants will learn how to use 3D and 4D acquisition data to optimize the skin texture and dynamics of expression.  Examples will be used to compare the level of realism of the figures in different production paths. We will also outline some practical applications of 3D reconstruction and Unreal Engine for digital human production.
    </p>

    {% endif %}
    {% endfor %}

</div>