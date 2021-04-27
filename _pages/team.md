---
title: "SACA - Members"
layout: gridlay
excerpt: "SACA Members"
sitemap: false
permalink: /members/
---

# Group Members

 Multiple Ph.D. positions in our research group are currently available. Promising candidates (GRE 310+, TOEFL 100+, GPA 3.8+, publication) will be financially supported. If interested, please email your resume to [ajawad@ncsu.edu](mailto:ajawad@ncsu.edu). Please specify which area interests you:

* Secure Architectures: Access pattern obfuscation, memory encryption, and data integrity efficient verification schemes
* Non-Volatile Memory Technologies: Memory management and filesystem optimizations
* Internet of Things (IoT) Devices: Security and Performance

## Director
{% assign number_printed = 0 %}
{% for member in site.data.director %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="director col-sm-12 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive profile" style="float: left" />
  <h4>{{ member.name }}</h4>
  <a href="{{ member.website }}">Personal Website</a>
  <br/><i>{{ member.info }}</i>
  <ul style="overflow: hidden">
  
  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}
  
  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}
  
  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}
  
  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}
 
  {% if member.number_educ == 5 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}
  
  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## M.Sc./Ph.D. Students
{% assign number_printed = 0 %}
{% for member in site.data.phdstudents %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}</i>
  <h6>{{ member.expe }}</h6>
  <ul style="overflow: hidden">
  
  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}
  
  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}
  
  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}
  
  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}
 
  {% if member.number_educ == 5 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}
  
  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


<!--## Undergrad Students 


-->

## Undergraduate Students 
{% assign number_printed = 0 %}
{% for member in site.data.ugstudents %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}</i>
  <h6>{{ member.expe }}</h6>
  <ul style="overflow: hidden">
  
  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}
  
  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}
  
  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}
  
  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}
  
  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Past Members
 <tr> <td> (Diversity statistics are availabe upon request. SACA has a history of training students from diverse and underrepresented groups in STEM.) </td></tr><br/>



<table align="center" style="width:100%">
<tr> 
    <th> PhD graduates</th>
  </tr>

  <tr>
    <td> - Dr. Vamsee Reddy (UCF), Spring 2021 (<b>first job:</b> AMD Research in Bellevue).  <br/><b>PhD achievements:</b> (1) Modeling of disaggregated NVM systems. (2) Modeling and evaulation of DeACT. (3) Inventing various QoS schemes in disaggregated memory systems..</td>
  </tr>


  <tr>
    <td> - Dr. Mazen Alwadi (UCF), Spring 2021 (<b>first employment:</b> Texas A&M University in College Station).  <br/><b>PhD achievements:</b> (1) Invention of the Phoenix scheme. (2) Design, modeling and evaluation of Stealth-Persist. (3) Modeling and evaluation of Minerva.</td>
  </tr>

  <tr>
    <td> - Dr. Mao Ye (UCF), Spring 2020 (<b>first employment:</b> AMD (Product Team) in Orlando).  <br/><b>PhD achievement:</b> Modeling and evaluation of the Osiris scheme</td>
  </tr>
</table>

<table align="center" style="width:100%">
<tr>
    <th> Post-Doc Mentees</th>
  </tr>
  <tr>
    <td> - Dr. Jian Zhou (UCF), Summer 2020 (<b>co-mentored with Prof. Jun Wang</b>). (<b>first job:</b> Huazhong University of Science and Technology).  <br/><b>Achievement:</b> Modeling and evaluation of the Lelantus scheme</td>
  </tr>
</table>


<table align="center" style="width:100%">
<tr> 
    <th>Master graduates</th>
  </tr>

  <tr>
    <td> - Abdullah Arafat (UCF), Summer 2020 (<b>first employment:</b> PhD student at UCF)</td>
  </tr>

  <tr>
    <td> - Derrick Greenspan (UCF), Falll 2018 (<b>first employment:</b> PhD student at IST institute in UCF, Orlando)</td>
  </tr>
</table>


<table align="center" style="width:100%">
  <tr> 
    <th>Undergraduate graduates</th>
  </tr>

   <tr>
    <td> - Charles Stephens, Spring 2020 (<b>first employment:</b> Embedded Systems Engineer at Motorola)</td>
  </tr>

 <tr>
    <td> - Ignacio Lopez, Summer 2020 (<b>first employment:</b> IT Engineer at Qualcomm)</td>
  </tr>

  <tr>
    <td> - Claudo Afonso, Spring 2019 (<b>first employment:</b> Software Engineer at Microsoft)</td>
  </tr>
 
  <tr>
    <td> - Nicholas Omusi, Spring 2019 (<b>first employment:</b> Electrical Engineer at Texas Instruments)</td>
  </tr>
  <tr>
    <td> - Andre Villaran, Spring 2019</td>
  </tr>
  <tr>
    <td> - Sannidiyan Rajendra, Spring 2018</td>
  </tr>
</table>




<!--
<table align="center" style="width:100%">
<tr><th>Ph.D. Students</th>
    <th>Master Students</th> 
    <th>Bachelor Students</th>
  </tr>
  <tr>
    <td>Someone who visited here, data</td>
    <td>Name name, Fall 2017</td>
    <td>First last, Spring 2017</td>
  </tr>
</table>
-->



