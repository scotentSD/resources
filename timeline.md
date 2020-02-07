
---
title: Research timeline
---

<section id="timeline">
  <h1>BETA timeline</h1>
  {% include key.html %}

  <ul class="timeline_ul">
    {% for post in site.posts %}
        <li class="timeline_card">
          <div class="timeline_head {{post.type}}">
            <a href="{{site.url}}/{{site.github.repository_name}}{{post.url}}">
              <div class="date_{{post.type}}" > {{ post.display_date }} </div>
            <!-- <br>  -->
            <div class="type_{{post.type}}" > </div>  
            </a>
          </div>
          <div class="timeline_body">
            <h2>{{ post.title}}</h2>
            {{ post.excerpt }}
          </div>
          <!-- <span class="initials">{{ post.initials }}</span> -->
       </li>
    {% endfor %}
  </ul>
</section>
