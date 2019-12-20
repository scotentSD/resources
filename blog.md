## Blog
The Blog page has code to display any posts in the posts folder

```

<ul>
 {% for post in site.posts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
 {% endfor %}
</ul>

```


It uses **liquid** to inject variables into the code like this:  ``` {% raw %}{{variablename}}{% endraw %}```


## Posts
Put a markup file in the posts folder and name it in the format
'yyyy-mm-dd-title.md`
Add some code (**Front Matter**) to the start and it will then be listed as a `POST` on the `BLOG` page
Add this code (**Front Matter**) to the header of the file to make it a POST

```
---
layout: post
title: Shared Entry Point
---
```

If an excerpt marker is defined in the `\_config.yml` file then you can mark a section of the post as the excerpt.
Everything above the  `<!—more—> `code will be the excerpt
```
<!--more-->
```

Add this line the `_config.yml` to enable the excerpt marker
```
excerpt_separator: "<!--more-->"
```

## Posts to populate timeline
Create a post as shown above but add extra code (**Front Matter**) to the start of the post like this:
```
---
layout: post              # Don't change this from "post"
title: Lab Research       # Title to show on the page
type: lab                 # Chose from: lab, online, a11y, other, partner
phase: beta               # chose from discovery, alpha, beta, live
initials: mk              # initials of person who did/uploaded the research
display_date: 22nd May 2019 # Date to show on the page
---```

Then add content using the following headings: ]

```
**Audience**
- zzz

**Focus**
- zzz

**Observations**
- zzz

**Documents**
- [ Findings ](../files/)
```

## Timeline page
The timeline page will consume the posts and use the **Front Matter** variables to insert the metadata into the timeline page using **liquid** calls.
Timeline pages in all repositories, call the **timeline.css** from this repository.

```
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
          <div class="date_{{post.type}}" > {{ post.display_date }} </div>
          <!-- <br>  -->
          <div class="type_{{post.type}}" > </div>  
        </div>
       </a>
        <div class="timeline_body">

           {{ post.excerpt }}

        </div>
        <!-- <span class="initials">{{ post.initials }}</span> -->
     </li>
  {% endfor %}
</ul>
</section>
```
