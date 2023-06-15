---
layout: about
title: Ethan Brewer
permalink: /
subtitle: Research Assistant Professor, New York University

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular

news: false  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: false  # includes social icons at the bottom of the page
---
ethan.brewer@nyu.edu&nbsp;|&nbsp;
[CV](https://drive.google.com/file/d/1_ca6HT2iuR2Tg_-4xOKzQsNAj5jAClDF/view?usp=sharing)&nbsp;&nbsp;|&nbsp;
[Google Scholar](https://scholar.google.com/citations?user=aVcOpMwAAAAJ&hl=en)&nbsp;&nbsp;|&nbsp;
[LinkedIn](https://www.linkedin.com/in/ethanbrewer/)
&nbsp;
## Bio
I am a Research Assistant Professor in the Department of Computer Science and Engineering at NYU and a member of the Visualization and Data Analytics (VIDA) Research Center under <a href='https://engineering.nyu.edu/faculty/claudio-silva'>Claudio Silva</a>. My research interests are centered on the synthesis of geospatial data, computer vision, and machine learning (geoAI). I am interested in better understanding patterns in development, population, and the environment under data-sparse conditions to fill in critical information gaps regarding physical, social, and economic outcomes in these areas. Moreover, my work utilizes remote sensing technologies and the latest computational techniques to expedite and scale analysis. I hold a Ph.D. in computational geography from William & Mary (under <a href='https://www.wm.edu/as/appliedscience/people/runfola_d.php'>Dan Runfola</a>), an M.S. in applied physics from William & Mary, and a B.S. in physics from UMBC.

&nbsp;
## Research Work

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>

