---
layout: ieeevr-default
title: "Conference Awards Committee IEEE VR 2024"
subtitle: "IEEE VR 2024"
title_separator: "|"
---
<script type="text/javascript">
    $(document).ready(function(){
		var email = ""; 
		var domain = "ieeevr.org"; 

        email = "awards2024";  		
		$(".awards").html("<span class='text-nowrap'><a href=javascript:location='" + "mail" + "to:" + email + "@" + domain + "'><i class='fas fa-fw fa-envelope-square emailIcon' style=''></i><i class='emailText'>" + email + "@" + domain + "</a></i></span>");   
        
        $(".awardsSm").html("<span class='text-nowrap'><a href=javascript:location='" + "mail" + "to:" + email + "@" + domain + "'><i class='fas fa-fw fa-envelope-square emailIconSm' style=''></i><i class='emailTextSm'>" + email + "@" + domain + "</a></i></span>"); 
	});
</script>
<h1>Conference Awards Committee IEEE VR 2024 <div class="floatRight"><span class="awardsSm"></span></div></h1>

<h2>Conference Awards Chairs</h2>
<ul>
    <li>Frank Steinicke ‒ Universität Hamburg, Germany</li>
    <li>Shi-Min Hu ‒ Tsinghua University, China</li>
    <li>Kiyoshi Kiyokawa ‒ Nara Institute of Science and Technology, Japan</li>
    <li>Luciana Nedel ‒ Federal University of Rio Grande do Sul, Brazil</li>
    <li>Missie Smith ‒ Meta Reality Labs, USA</li>
</ul>
 <div class="ieeevrmsgbox">
    <div class = "ieeevrmsgboxInsideNoColor small_emphasize">            
        <div class= "bold alignCenter paddingBottomxSmall">
            Congratulations to the Best Paper Winners and Honorable Mentions!<br />
            The other award winners will be announced during the week of the conference.
        </div>
    </div>
</div>
<table class="styled-table" style="font-size: 0.9em; ">
    <tr>
        <th colspan="3">Conference Awards - Quick Links</th>
    </tr>
    <tr>
        <td><a href="#papers">Papers</a></td>
        <td><a href="#conference-best">Best Papers</a></td>
        <td><a href="#conference-honorable">Honorable Mentions</a></td>
    </tr> 
    <!--
    <tr>
        <td><a href="#posters">Posters</a></td>
        <td><a href="#best-poster">Best Poster</a></td>
        <td><a href="#poster-honorable">Honorable Mention</a></td>
    </tr>  
    <tr>
        <td><a href="#demos">Research Demos</a></td>
        <td><a href="#demo-best">Best Research Demo</a></td>
        <td><a href="#demo-honorable">Honorable Mention</a></td>
    </tr>
    <tr>
        <td><a href="#3dui">3DUI Contest</a></td>
        <td><a href="#3dui-best">Best 3DUI</a></td>
        <td><a href="#3dui-honorable">Honorable Mention</a></td>
    </tr>  
    <tr>
        <td><a href="#dc">Doctoral Consortium</a></td>
        <td><a href="#DC-best">Best Presentation</a></td>
        <td><a href="#DC-honorable">Honorable Mention</a></td>
    </tr>      
    <tr>
        <td><a href="#paper-presentation">Paper Presentation</a></td>
        <td><a href="#Paper-presentation-best">Best Paper Presentation</a></td>
        <td><a href="#Paper-presentation-honorable">Honorable Mention</a></td>
    </tr> -->     
</table>
<h2 id="papers">Best Papers & Honorable Mention for Best Papers</h2>

<p>The IEEE VR Best Paper Awards honor exceptional papers published and presented at the IEEE VR conference. During the review process, the program committee chairs will choose approximately 3% of submissions to receive an award. Among these chosen submissions, the separate Conference Awards Selection Committee will select the best submissions to receive a Best Paper Award (ca. 1% of total submissions), while a selection of the remaining submissions receive an Honorable Mention Award. Papers that receive an award will be marked in the program, and authors will receive a certificate at the conference.</p>

<h2 id='conference-best' style="text-align: center; color: #00aeef;">Best Papers</h2>
<div>
    {% for item in site.data.awards %}
        {% if item.type == 'Journal' %}
            {% if item.award == 'Best Paper' %}
                {% for j in site.data.journalpapers %}
                    {% if j.id == item.id %}
                        {% assign authornames = j.authors | split: ";" %}
                        <p id="{{ j.id }}">
                            <strong>{{ j.Title }}</strong><br/>
                            <i>
                                {% for name in authornames %}
                                    {% assign barename = name | split: ":" %}
                                    {% if name == authornames.last %}
                                        {{ barename.first | strip }}
                                    {% else %}
                                        {{ barename.first | strip }}, 
                                    {% endif %}
                                {% endfor %}
                            </i>
                        </p>
                        <div id="J{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleJ{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleJ{{ j.id }}" class="lbl-toggle">Abstract</label>
                            <div class="collapsible-content">
                                <div class="content-inner">
                                    <p>{{ j.abstract }}</p>
                                </div>
                            </div>
                        </div>
                    {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
    {% if item.type == 'Conference' %}
        {% if item.award == 'Best Paper' %}
            {% for j in site.data.conferencepapers %}
                {% if j.id == item.id %}
                    {% assign authornames = j.authors | split: ";" %}
                    <p id="{{ j.id }}">
                        <strong>{{ j.Title }}</strong><br/>
                        <i>
                        {% for name in authornames %}
                            {% assign barename = name | split: ":" %}
                            {% if name == authornames.last %}
                                {{ barename.first | strip }}
                            {% else %}
                                {{ barename.first | strip }}, 
                            {% endif %}
                        {% endfor %}
                        </i>
                    </p>
                    <div id="C{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleC{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleC{{ j.id }}" class="lbl-toggle">Abstract</label>
                        <div class="collapsible-content">
                            <div class="content-inner">
                                <p>{{ j.abstract }}</p>
                            </div>
                        </div>
                    </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}
{% endfor %}
</div>

<h2 id='conference-honorable' style="text-align: center; color: #00aeef;">Best Papers - Honorable Mentions</h2>
<div>
    {% for item in site.data.awards %}
        {% if item.type == 'Journal' %}
            {% if item.award == 'Honorable Mention' %}
                {% for j in site.data.journalpapers %}
                    {% if j.id == item.id %}
                        {% assign authornames = j.authors | split: ";" %}
                        <p id="{{ j.id }}">
                            <strong>{{ j.Title }}</strong><br/>
                            <i>
                            {% for name in authornames %}
                                {% assign barename = name | split: ":" %}
                                {% if name == authornames.last %}
                                    {{ barename.first | strip }}
                                {% else %}
                                    {{ barename.first | strip }}, 
                                {% endif %}
                            {% endfor %}
                            </i>
                        </p>
                        <div id="J{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleJ{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleJ{{ j.id }}" class="lbl-toggle">Abstract</label>
                            <div class="collapsible-content">
                                <div class="content-inner">
                                    <p>{{ j.abstract }}</p>
                                </div>
                            </div>
                        </div>
                    {% endif %}
                {% endfor %}
            {% endif %}
        {% endif %}
        {% if item.type == 'Conference' %}
            {% if item.award == 'Honorable Mention' %}
                {% for j in site.data.conferencepapers %}
                    {% if j.id == item.id %}
                        {% assign authornames = j.authors | split: ";" %}
                        <p id="{{ j.id }}">
                            <strong>{{ j.Title }}</strong><br/>
                            <i>
                            {% for name in authornames %}
                                {% assign barename = name | split: ":" %}
                                {% if name == authornames.last %}
                                    {{ barename.first | strip }}
                                {% else %}
                                    {{ barename.first | strip }}, 
                                {% endif %}
                            {% endfor %}
                            </i>
                        </p>
                        <div id="C{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleC{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleC{{ j.id }}" class="lbl-toggle">Abstract</label>
                            <div class="collapsible-content">
                                <div class="content-inner">
                                    <p>{{ j.abstract }}</p>
                                </div>
                            </div>
                        </div>
                    {% endif %}
                {% endfor %}
            {% endif %}
        {% endif %}
    {% endfor %}
</div>

<h2 id="posters">Best Posters & Honorable Mention for Best Poster</h2>

<p>The IEEE VR Best Poster Awards honors exceptional posters published and presented at the IEEE VR conference. During the review process, the best poster committee for IEEE VR consists of three distinguished members chosen by the Conference Awards Committee and Poster Chairs, which will select the best posters. Posters that receive an award will be marked in the program, and authors will receive a certificate at the conference. </p>

<!--<h2 id='best-poster' style="text-align: center; color: #00aeef;">Best Poster</h2>
<div>
    {% for item in site.data.awards %}
        {% if item.type == 'Poster' %}
            {% if item.award == 'Best Poster' %}
                {% for j in site.data.posters %}
                    {% if j.id == item.id %}
                        <p id="{{ j.id }}">
                            <strong>{{ j.Title }}</strong><br/>
                            <i>{{ j.authors }}</i>
                        </p>
                        <div id="P{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleP{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleP{{ j.id }}" class="lbl-toggle">Abstract</label>
                            <div class="collapsible-content">
                                <div class="content-inner">
                                    <p>{{ j.abstract }}</p>
                                </div>
                            </div>
                        </div>
                    {% endif %}
                {% endfor %}
            {% endif %}
        {% endif %}
    {% endfor %}
</div>

<h2 id='poster-honorable' style="text-align: center; color: #00aeef;">Poster - Honorable Mention</h2>
<div>
    {% for item in site.data.awards %}
        {% if item.type == 'Poster' %}
            {% if item.award == 'Honorable Mention' %}
                {% for j in site.data.posters %}
                    {% if j.id == item.id %}
                        <p id="{{ j.id }}">
                            <strong>{{ j.Title }}</strong><br/>
                            <i>{{ j.authors }}</i>
                        </p>
                        <div id="P{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleP{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleP{{ j.id }}" class="lbl-toggle">Abstract</label>
                            <div class="collapsible-content">
                                <div class="content-inner">
                                    <p>{{ j.abstract }}</p>
                                </div>
                            </div>
                        </div>
                    {% endif %}
                {% endfor %}
            {% endif %}
        {% endif %}
    {% endfor %}
</div>-->

<h2 id="demos">Best Demo & Honorable Mention for Best Demo</h2>

<p>The IEEE VR Best Demo Awards honors exceptional research demos published and presented at the IEEE VR conference. The IEEE VR Demo Chairs rank the accepted demos and recommend approximately 10% of all demos for an award. The best demo committee for IEEE VR consists of three distinguished members chosen by the Conference Awards Committee Chairs and the Demo Chairs. This committee selects one of the demos for the Best Demo Award and one for the Honorable Mention Award. The corresponding authors will receive a certificate at the conference. </p>

<!--<h2 id='demo-best' style="text-align: center; color: #00aeef;">Best Research Demo</h2>
<div>
    {% for item in site.data.awards %}
        {% if item.type == 'Demo' %}
            {% if item.award == 'Best Demo' %}
                {% for j in site.data.demos %}
                    {% if j.id == item.id %}                   
                        <p id="{{ j.id }}">
                            <strong>{{ j.Title }}</strong><br/>
                            <i>{{ j.authors }}</i>
                        </p>
                        <div id="D{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleD{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleD{{ j.id }}" class="lbl-toggle">Abstract</label>
                            <div class="collapsible-content">
                                <div class="content-inner">
                                    <p>{{ j.abstract }}</p>
                                </div>
                            </div>
                        </div>
                    {% endif %}
                {% endfor %}
            {% endif %}
        {% endif %}
    {% endfor %}
</div>

<h2 id='demo-honorable' style="text-align: center; color: #00aeef;">Research Demo - Honorable Mention</h2>
<div>
    {% for item in site.data.awards %}
        {% if item.type == 'Demo' %}
            {% if item.award == 'Honorable Mention' %}
                {% for j in site.data.demos %}
                    {% if j.id == item.id %}                                      
                        <p id="{{ j.id }}">
                            <strong>{{ j.Title }}</strong><br/>
                            <i>{{ j.authors }}</i>
                        </p>
                        <div id="D{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleD{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleD{{ j.id }}" class="lbl-toggle">Abstract</label>
                            <div class="collapsible-content">
                                <div class="content-inner">
                                    <p>{{ j.abstract }}</p>
                                </div>
                            </div>
                        </div>
                    {% endif %}
                {% endfor %}
            {% endif %}
        {% endif %}
    {% endfor %}
</div>-->

<h2 id="dui">Best 3DUI Contest & Honorable Mention</h2>

<p>The IEEE VR Best 3DUI Contest Submission Awards honors exceptional 3DUI contest submissions published and presented at the IEEE VR conference. The 3DUI contest chairs select one of the submissions for the Best 3DUI Contest Submission Award and one for the Honorable Mention Award. The final decision is based on a combination of the reviews’ scores, scores from experts testing the contest submission during the conference, and the audience scores. The winning team with the highest score will be awarded. Authors will receive a certificate at the conference.</p>

<!--<h2 id='3dui-best' style="text-align: center; color: #00aeef;">Best 3DUI</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == '3DUI Contest' %}
        {% if item.award == 'Best 3DUI' %}
            {% for j in site.data.3duicontest %}
                {% if j.id == item.id %}                                   
                    <p id="{{ j.id }}">
                        <strong>{{ j.Title }}</strong><br/>
                        <i>{{ j.authors }}</i>
                    </p>
                    <div id="3dui{{ j.id }}" class="wrap-collabsible"> <input id="collapsible3dui{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsible3dui{{ j.id }}" class="lbl-toggle">Abstract</label>
                        <div class="collapsible-content">
                            <div class="content-inner">
                                <p>{{ j.abstract }}</p>
                            </div>
                        </div>
                    </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}    
{% endfor %}
</div>

<h2 id='3dui-honorable' style="text-align: center; color: #00aeef;">3DUI - Honorable Mention</h2>
<div>
{% for item in site.data.awards %}
    {% if item.type == '3DUI Contest' %}
        {% if item.award == 'Honorable Mention' %}
            {% for j in site.data.3duicontest %}
                {% if j.id == item.id %}                                   
                    <p id="{{ j.id }}">
                        <strong>{{ j.Title }}</strong><br/>
                        <i>{{ j.authors }}</i>
                    </p>
                    <div id="3dui{{ j.id }}" class="wrap-collabsible"> <input id="collapsible3dui{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsible3dui{{ j.id }}" class="lbl-toggle">Abstract</label>
                        <div class="collapsible-content">
                            <div class="content-inner">
                                <p>{{ j.abstract }}</p>
                            </div>
                        </div>
                    </div>
                {% endif %}
            {% endfor %}
        {% endif %}
    {% endif %}    
{% endfor %}
</div>-->

<h2 id="dc">Best DC Paper & Honorable Mention for Best DC Paper</h2>

<p>The IEEE VR Best Doctoral Consortium (DC) Paper Awards honors exceptional DC papers published and presented at the IEEE VR conference. The best DC paper committee consists of three distinguished members chosen by the Conference Awards Committee Chairs and the DC chairs. The DC chairs recommend 20% of all DC papers for such an award. The best DC committee selects one of these DC papers for Best DC Paper Award and one to receive an Honorable Mention Award. DC papers that receive an award will be marked in the program, and authors will receive a certificate at the conference. </p>

<!--<h2 id='DC-best' style="text-align: center; color: #00aeef;">Best Doctoral Consortium</h2>
<div>
</div>

<h2 id='DC-honorable' style="text-align: center; color: #00aeef;">Doctoral Consortium - Honorable Mention Award</h2>
<div>
</div>
-->

<h2 id="paper-presentation">Best Paper Presentation</h2>

<p>The IEEE VR Best Presentation Awards honor excellent, interesting, and stimulating presentations of research papers at the IEEE VR conference. During the conference, the audience can give a vote for each presentation that they think deserves an award. Approximately 3% of presentations with the highest number of votes receive an award. Among these selected presentations, the top 1% regarding the number of votes, will receive a Best Presentation Award, while the remaining presentations receive an Honorable Mention Award.</p>

<!--<h2 id='Paper-presentation-best' style="text-align: center; color: #00aeef;">Best Paper Presentation</h2>
<div>
    {% for item in site.data.awards %}
        {% if item.type == 'PresentationJ' %}
            {% if item.award == 'Best Presentation' %}
                {% for j in site.data.journalpapers %}
                    {% if j.id == item.id %}
                        {% assign authornames = j.authors | split: ";" %}
                        <p id="{{ j.id }}">
                            <strong>{{ j.Title }}</strong><br/>
                            <i>
                            {% for name in authornames %}
                                {% assign barename = name | split: ":" %}
                                {% if name == authornames.last %}
                                    {{ barename.first | strip }}
                                {% else %}
                                    {{ barename.first | strip }}, 
                                {% endif %}
                            {% endfor %}
                            </i>
                        </p>
                        <div id="J{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleJ{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleJ{{ j.id }}" class="lbl-toggle">Abstract</label>
                            <div class="collapsible-content">
                                <div class="content-inner">
                                    <p>{{ j.abstract }}</p>
                                </div>
                            </div>
                        </div>
                    {% endif %}
                {% endfor %}
            {% endif %}
        {% endif %}
        {% if item.type == 'PresentationC' %}
            {% if item.award == 'Best Presentation' %}
                {% for j in site.data.conferencepapers %}
                    {% if j.id == item.id %}
                        {% assign authornames = j.authors | split: ";" %}                        
                        <p id="{{ j.id }}">
                            <strong>{{ j.Title }}</strong><br/>
                            <i>
                            {% for name in authornames %}
                                {% assign barename = name | split: ":" %}
                                {% if name == authornames.last %}
                                    {{ barename.first | strip }}
                                {% else %}
                                    {{ barename.first | strip }}, 
                                {% endif %}
                            {% endfor %}
                            </i>
                        </p>
                        <div id="C{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleC{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleC{{ j.id }}" class="lbl-toggle">Abstract</label>
                            <div class="collapsible-content">
                                <div class="content-inner">
                                    <p>{{ j.abstract }}</p>
                                </div>
                            </div>
                        </div>
                    {% endif %}
                {% endfor %}
            {% endif %}
        {% endif %}
    {% endfor %}
</div>

<h2 id='Paper-presentation-honorable' style="text-align: center; color: #00aeef;">Paper Presentation - Honorable Mention</h2>
<div>
    {% for item in site.data.awards %}
        {% if item.type == 'PresentationJ' %}
            {% if item.award == 'Honorable Mention' %}
                {% for j in site.data.journalpapers %}
                    {% if j.id == item.id %}
                        {% assign authornames = j.authors | split: ";" %}
                        <p id="{{ j.id }}">
                            <strong>{{ j.Title }}</strong><br/>
                            <i>
                            {% for name in authornames %}
                                {% assign barename = name | split: ":" %}
                                {% if name == authornames.last %}
                                    {{ barename.first | strip }}
                                {% else %}
                                    {{ barename.first | strip }}, 
                                {% endif %}
                            {% endfor %}
                            </i>
                        </p>
                        <div id="J{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleJ{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleJ{{ j.id }}" class="lbl-toggle">Abstract</label>
                            <div class="collapsible-content">
                                <div class="content-inner">
                                    <p>{{ j.abstract }}</p>
                                </div>
                            </div>
                        </div>
                    {% endif %}
                {% endfor %}
            {% endif %}
        {% endif %}
        {% if item.type == 'PresentationC' %}
            {% if item.award == 'Honorable Mention' %}
                {% for j in site.data.conferencepapers %}
                    {% if j.id == item.id %}
                        {% assign authornames = j.authors | split: ";" %}
                        <p id="{{ j.id }}">
                            <strong>{{ j.Title }}</strong><br/>
                            <i>
                            {% for name in authornames %}
                                {% assign barename = name | split: ":" %}
                                {% if name == authornames.last %}
                                    {{ barename.first | strip }}
                                {% else %}
                                    {{ barename.first | strip }}, 
                                {% endif %}
                            {% endfor %}
                            </i>
                        </p>
                        <div id="C{{ j.id }}" class="wrap-collabsible"> <input id="collapsibleC{{ j.id }}" class="toggle" type="checkbox"> <label for="collapsibleC{{ j.id }}" class="lbl-toggle">Abstract</label>
                            <div class="collapsible-content">
                                <div class="content-inner">
                                    <p>{{ j.abstract }}</p>
                                </div>
                            </div>
                        </div>
                    {% endif %}
                {% endfor %}
            {% endif %}
        {% endif %}
    {% endfor %}
</div>-->

