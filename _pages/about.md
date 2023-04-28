---
layout: page
permalink: /
title: about
nav: about

<!--description: <a href="https://ai.google/" target="_blank">Google AI</a> -->
address: <a href="https://cs.stonybrook.edu" class="page-description" target="_blank">Stony Brook University, Stony Brook, New York, USA </a>
---

<div class="col p-0 pt-4 pb-4">
  <h1 class="pb-3 title text-left font-weight-bold">Brian Kondracki</h1>
  <h6 class="m-0 mb-2" style="font-size: 0.83em;">{{ page.description }}</h6>
  {% if page.address %}
      <h6 class="m-0 mb-2" style="font-size: 0.83em;">{{ page.address }}</h6>
  {% endif %}
</div>

<!-- Introduction -->

<div style="display: flex; flex-wrap: wrap;">
    <div class="text-justify p-0">
        <div class="col-xs-12 col-sm-6 p-0 pt-2 pb-sm-2 pb-4 pl-sm-4 text-center" style="float: right;">
          <img class="profile-img img-responsive" src="{{ 'prof_pic.jpg' | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}">
        </div>

        <p>
            I am a cybersecurity researcher working in the <a href="https://securitee.org/lab" target="_blank">Pragsec Lab</a> at Stony Brook University under the guidance of <a href="https://securitee.org" target="_blank">Professor Nick Nikiforakis</a>, where I earned a PhD in Computer Science.
        </p>
        
        <p>
	    My research focuses on web and network security. Specifically, I'm working on developing techinques to identify networked entities using characteristics of their behavior.
        </p>

	    <p>
		Before starting my Ph.D., I received my B.S. and M.S. in Computer Science, with specialization in Computer Security, from Stony Brook University.	
	    </p>
    </div>
</div>

<!-- News -->
<div class="news mt-3 p-0">
  <h1 class="title mb-4 p-0">news</h1>
  {% assign news = site.news | reverse %}
  {% for item in news limit: site.news_limit %}
    <div class="row p-0">
      <div class="col-sm-2 p-0">
        <span class="badge orange darken-1 font-weight-bold text-uppercase align-middle date ml-3">
          {{ item.date | date: "%b %Y" }}
        </span>
      </div>
      <div class="col-sm-10 mt-2 mt-sm-0 ml-3 ml-md-0 p-0 font-weight-light text">
        <p>{{ item.content | remove: '<p>' | remove: '</p>' | emojify }}</p>
      </div>
    </div>
  {% endfor %}
</div>
