---
layout: page2
title: Nicolas Magain - publications 
description: When building a website it's helpful to see what the focus of your site is. This page is an example of how to show a website's focus.
sitemap:
    priority: 0.7
    lastmod: 2017-11-02
    changefreq: weekly
---
## Publications


<ul>

    {% assign sorted = (site.publications | sort: 'year') | reverse %}
    {% for publication in sorted %}
    <h4><a href="{{ publication.pdf | absolute_url }}" class="fas fa-file-pdf"></a> {{ publication.title }}</h4>
      <span style="line-height: -100px ;">       {{ publication.year }}.  {{ publication.authors }}  {{ publication.journalinfo }}</span>
<br /> <a href="{{ publication.orbi | absolute_url }}" class="smallbutton">ORBI</a>
  <a href="{{ publication.journal | absolute_url }}" class="smallbutton">Journal Website</a>
  {% if publication.supplementary %} <a href="{{ publication.supplementary | absolute_url }}" class="smallbutton">SUPPLEMENTARY MATERIAL</a>{% endif %}
<br />
    {% endfor %}
</ul>


