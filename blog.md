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

## Posts
Put a markup file in the posts folder and name it in the format
'yyyy-mm-dd-title.md`
Add some code to the start and it will then be listed as a `POST` on the `BLOG` page
Add this code to the header of the file to make it a POST

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
