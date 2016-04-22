---
layout: page
title: About
permalink: /about/
---

# About

  - what is CityGML
  - who is responsible for it?
  - copy stuff from Thomas here...
  
# Docs & schemas


# CityGML classes

  - Terrain
  - Vegetation

# LOD
  
  - 16 lods
  - datasets from 16 lod

# Tools
  
  - 3d reconsturction workflow FME of Ravi
  - link to validation
  - viewers 
  - 3dcitydb

# Datasets

  - list of open datasets
  - examples for diff classes

# Applications
  
  - what can be done with CityGML (our 400 references paper maintained there)


The 3D geoinformation research group is part of the [Department of Urbanism](http://www.bk.tudelft.nl/en/about-faculty/departments/urbanism/), [Faculty of Architecture and the Built Environment](http://www.bk.tudelft.nl) of the [Delft University of Technology](http://www.tudelft.nl), and is affiliated with [AMS, the Amsterdam Institute for Advanced Metropolitan Solutions](http://www.ams-institute.org). 
It focuses on the technologies underpinning geographical information systems (GIS), and aims at designing, developing and implementing better systems to model 3D cities, buildings and landscapes.
These systems help in environmental modelling, crisis management, automated cartographic generalisation, information modelling, modelling of the interior of buildings, etc.

It is a multidisciplinary group (computer scientists, geomatics engineers, and geographers) composed of 3 permanent research staff and several PhD students, postdocs and visitors.

It has a history of successful collaborations with the industry and the government: its research has led to [software]({{ "/code/" |  prepend: site.baseurl }}), standards and patents for the management of 3D geographic information.

The staff of the group is active in several international organisations such as the [Open Geospatial Consortium](http://www.opengeospatial.org), [EuroSDR](http://www.eurosdr.net), and the [International Society for Photogrammetry and Remote Sensing](http://www.isprs.org).

Our research funding mostly comes from the following organisations:

<div class="row">
  <div class="col-md-2 col-xs-6 nopadding"><a href="https://erc.europa.eu"><img class="img-responsive" src="{{ "/img/partners/erc.png" | prepend: site.baseurl }}"/></a></div>
  <div class="col-md-2 col-xs-6 nopadding"><a href="http://www.stw.nl"><img class="img-responsive" src="{{ "/img/partners/stw.png" | prepend: site.baseurl }}"/></a></div>
  <div class="col-md-2 col-xs-6 nopadding"><a href="http://www.ams-institute.org"><img class="img-responsive" src="{{ "/img/partners/ams.png" | prepend: site.baseurl }}"/></a></div>
  <div class="col-md-2 col-xs-6 nopadding"><a href="http://www.kadaster.nl"><img class="img-responsive" src="{{ "/img/partners/kadaster.png" | prepend: site.baseurl }}"/></a></div>
</div>

- - - 

## <a name="people"></a> Staff

{% assign members = site.data.staff | sort: 'surname' %}

<div class="row">
    {% for member in members %}
    <div class="col-md-3 col-sm-4 col-xs-8 col-xs-offset-2 col-sm-offset-0 col-md-offset-0">
    {% if member.homepage %}
      <a href="http://{{ member.homepage }}"><img class="img-circle img-responsive" src="{{ "/img/staff/" | append: member.photo | prepend: site.baseurl }}"></a>
    {% else %}
      <img class="img-circle img-responsive" src="{{ "/img/staff/" | append: member.photo | prepend: site.baseurl }}">
    {% endif %}
    {% if member.swapnames == False %}
      <h3>{{ member.name }} {{ member.van }} {{ member.surname }}<br><small>{{ member.title }}</small></h3>
    {% else %}
      <h3>{{ member.surname }} {{ member.name }}<br><small>{{ member.title }}</small></h3>
    {% endif %}
      <p>
        {% if member.homepage %}
          <i class="fa fa-home"></i> <a href="http://{{ member.homepage }}">{{ member.homepage }}</a><br>
        {% endif %}
        {% if member.email %}
          <i class="fa fa-envelope"></i> <a href="mailto:{{ member.email }}">{{ member.email }}</a><br>
        {% endif %}
        {% if member.phone %}
          <i class="fa fa-phone"></i> <a href="tel:{{ member.phone }}">{{ member.phone }}</a><br>
        {% endif %}
        {% if member.twitter %}
          <i class="fa fa-twitter"></i> <a href="https://twitter.com/{{ member.twitter }}">@{{ member.twitter }}</a><br>
        {% endif %}
        {% unless member.homepage %}
          <br>
        {% endunless %}
        {% unless member.email %}
          <br>
        {% endunless %}
        {% unless member.phone %}
          <br>
        {% endunless %}
        {% unless member.twitter %}
          <br>
        {% endunless %}
      </p>
    </div>
    {% endfor %}
</div>

- - - 

## <a name="people"></a> Former Staff

[List of former staff]({{ "/about/formerstaff" | prepend: site.baseurl }})

- - -

<h2 id="where">Our offices</h2>

<div class="col-md-4">
  <i class="fa fa-map-marker fa-fw">     </i> Room BG.WEST.010 (building #8) <br>
  <i class="fa fa-map-marker fa-fw fade"></i> Faculty of Architecture <br>
  <i class="fa fa-map-marker fa-fw fade"></i> and the Built Environment<br>
  <i class="fa fa-map-marker fa-fw fade"></i> Delft University of Technology <br>
  <i class="fa fa-map-marker fa-fw fade"></i> Julianalaan 134 <br>
  <i class="fa fa-map-marker fa-fw fade"></i> Delft 2628BL<br>
  <i class="fa fa-map-marker fa-fw fade"></i> the Netherlands <br>
  <i class="fa fa-map-marker fa-fw fade"></i> <a href="http://www.tudelft.nl/en/about-tu-delft/contact-and-accessibility/housing-tu-delft/accessibility/building-8/">How to get here</a>
</div>
<div class="col-md-8">
  <div id="map"></div>
</div>

<script src="//d19vzq90twjlae.cloudfront.net/leaflet-0.4/leaflet.js"></script> 
<script src="//cdnjs.cloudflare.com/ajax/libs/proj4js/1.1.0/proj4js-compressed.js"></script>
<script src="{{ "/assets/js/mymap.js" | prepend: site.baseurl }}"></script>
