---
layout: base/bar-sidebar-none
title: Projects

projects:
  - name: Neighborly
    path: savvy
  - name: Lend a Hand
    path: lendahand
  - name: JRNY
    path: jrny
  - name: Defroster
    path: defroster
  - name: Broccoli for All
    path: broccoli
  - name: OffTheStreet
    path: offthestreet
  - name: Nexus
    path: nexus
  - name: Helping Hands
    path: helpinghands
   
---

<html>
<div class="row">
<div class="col-md-9" markdown="block">
# Project Theme

Social software continues to pervade our daily lives, influencing with whom we connect, the news to which we are exposed and the entertainment with which we amuse ourselves. In addition to our online social networks of friendship and shared interests, everyone also lives in a specific physical community.  Each community is a locale with a distinct mix of individuals, resources and needs, with the particular complications of space, awareness and privacy that go along right in hand. Considering both the benefits and challenges of physical proximity, what kinds of applications, interactions or services can we design that support and leverage our communities?

# Project Websites

{% assign projects_rows = page.projects | size | divided_by: 4 %}

<div class="row">
  {% for item_project in page.projects %}
    <div class="col-sm-3 col-xs-6">        
      <p>
        <a href="{{ site.baseurl }}/projects/{{ item_project.path }}/" target="_blank">
          {{ item_project.name }}
        </a>
      </p>
      <div class="thumbnailBox">
        <a href="{{ site.baseurl }}/projects/{{ item_project.path }}/" target="_blank">
          <img src="{{ site.baseurl }}/projects/{{ item_project.path }}/project_thumb.png" width="150" class="projectThumbnail" alt="{{ item_project.name }}"/>
        </a>
      </div>
      {% assign row_current = forloop.index | minus: 1 | divided_by: 4 | plus: 1 %}
      {% unless row_current == projects_rows %}
        <p>&nbsp;</p>
      {% endunless %}
    </div>
  {% endfor %}
</div>

</div>
<div class="col-md-3 hidden-xs hidden-sm" markdown="block">
<div class="panel panel-default" style="margin-top:20px;">
<div class="panel-heading" markdown="block">
## Poster Session
</div>
<div class="panel-body" markdown="block">
{% comment %}
Please join us for a poster session celebrating the outstanding design work of CSE 440 students:
  
Tuesday, June 7
  
12:30 pm
    
[CSE Atrium](http://www.washington.edu/maps/#!/cse)
{% endcomment %}
Thank you for joining us to celebrate the outstanding design work of CSE 440 students:

Tuesday, June 7
  
12:30 pm

<img src="{{ site.baseurl }}/images/poster_session.jpg" width="100%" alt="Poster Session"/>
</div>
</div>
</div>
</div>
</html>