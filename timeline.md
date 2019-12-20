
<link rel="stylesheet" href="https://scotentsd.github.io/resources/timeline.css?ver=15">
<link href="https://fonts.googleapis.com/css?family=Roboto&display=swap" rel="stylesheet">
<section id="timeline">
<h2>Research Timeline</h2>
<div class="colour_key">
  <p class="colour_key_heading">KEY</p>
  <p><span style="background-color: #f5c44b">&nbsp;&nbsp;&nbsp;&nbsp;</span> Accessibility</p>
  <p><span style="background-color: #3ee9d1">&nbsp;&nbsp;&nbsp;&nbsp;</span> Other</p>
  <p><span style="background-color: #ce43eb">&nbsp;&nbsp;&nbsp;&nbsp;</span> Lab research</p>
  <p><span style="background-color: #4d92eb">&nbsp;&nbsp;&nbsp;&nbsp;</span> Online research</p>
  <p><span style="background-color: #935300">&nbsp;&nbsp;&nbsp;&nbsp;</span> Partners collaboration - co-design</p>
</div>


<ul class="timeline_ul">
  {% for post in site.posts reversed %}
      <li class="timeline_card">
      <div class="timeline_head {{post.type}}">
          <div class="date_{{post.type}}" > {{ post.display_date }} </div>
          <!-- <br>  -->
          <div class="title_{{post.type}}" >{{post.title}} </div>  
        </div>

        <div class="timeline_body">
           {{ post.excerpt }}
        </div>
        <!-- <span class="initials">{{ post.initials }}</span> -->
     </li>
  {% endfor %}
</ul>
</section>
