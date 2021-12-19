---
layout: page
title: Team 
description: When building a website it's helpful to see what the focus of your site is. This page is an example of how to show a website's focus.
sitemap:
    priority: 0.7
    lastmod: 2017-11-02
    changefreq: weekly
---
<h2>Team members</h2>


<ul>

 
<h2>Permanent members</h2>
{% for member in site.members %}
{% if member.position == "permanent" %}
<h4>{{ member.fullname }} {% unless member.researchgate == blank %}<a href="{{ member.researchgate | absolute_url }}" class="fab fa-researchgate" target="_blank"></a>{% endunless %}  {% unless member.googlescholar == blank %} <a href="{{ member.googlescholar | absolute_url }}" class="fab fa-google" target="_blank"></a> {% endunless %} </h4>
      <span style="line-height: -100px ;">       {{ member.text }} </span>


     {% endif %}

{% endfor %}

</ul>

<ul>


<h2>PhD Students</h2>
{% for member in site.members %}
    {% if member.position == "phd" and member.membership == "current" %}
    <h4>{{ member.fullname }} {% unless member.researchgate == blank %}<a href="{{ member.researchgate | absolute_url }}" class="fab fa-researchgate" target="_blank"></a>{% endunless %}  {% unless member.googlescholar == blank %} <a href="{{ member.googlescholar | absolute_url }}" class="fab fa-google" target="_blank"></a> {% endunless %} </h4>
      <span style="line-height: -100px ;">       {{ member.text }} </span>

     {% endif %}
  {% endfor %}   
</ul>
<h2>Master students</h2>
<br />

<h2>Other</h2>
<h4>Laurent Gohy</h4> <p> Laurent is managing the molecular lab. He is a real pro in everything DNA extractions and PCR. He also has some duties with the herbarium, contributing to the management of collections</p>
<h4>Ludovic Sottiaux</h4>
<p>Ludovic is actively involved in teaching botany and conservation to the students of the specialized master in conservation biology and biodiversity management.</p>
<br />
<ul>
<h2>Alumni PhD Students</h2>
 {% assign sorted = (site.members | sort: 'year') | reverse %}
{% for member in sorted %}
{% if member.position == "phd" and member.membership != "current" %}
    <h4>{{ member.fullname }} {% unless member.researchgate == blank %}<a href="{{ member.researchgate | absolute_url }}" class="fab fa-researchgate" target="_blank"></a>{% endunless %}  {% unless member.googlescholar == blank %} <a href="{{ member.googlescholar | absolute_url }}" class="fab fa-google" target="_blank"></a> {% endunless %} </h4>
      <span style="line-height: -100px ;">       {{ member.text }} </span>

     {% endif %}
  {% endfor %}   
</ul>


<br />
<ul>
<h2>Alumni Master Students</h2>
 {% assign sorted = (site.members | sort: 'year') | reverse %}
{% for member in sorted %}
{% if member.position == "master" and member.membership != "current" %}
    <h4>{{ member.fullname }} ({{ member.year }}) {% unless member.researchgate == blank %}<a href="{{ member.researchgate | absolute_url }}" class="fab fa-researchgate" target="_blank"></a>{% endunless %}  {% unless member.googlescholar == blank %} <a href="{{ member.googlescholar | absolute_url }}" class="fab fa-google" target="_blank"></a> {% endunless %} </h4>
      <span style="line-height: -100px ;">       {{ member.text }} </span>
<p>{% unless member.download == blank %}<a class="smallbutton" target="_blank" href="/PDF/{{member.download}}">Download</a>{% endunless %} {% unless member.matheo == blank %}<a class="smallbutton" target="_blank" href="{{member.matheo}}">MatheO</a>{% endunless %}</p>

     {% endif %}
  {% endfor %}   
</ul>

<h2>Affiliations</h2>
<p> <a href="http://www.bionat.ulg.ac.be/"> Evolution and Conservation Biology Unit, ULiège</a>
<br /> <a href="https://www.inbios.uliege.be/cms/c_4259640/fr/inbios">InBioS Research Center, ULiège</a>
<br /> <a href="https://www.sciences.uliege.be/cms/c_3966569/en/sciences">Faculté des Sciences, ULiège</a>
