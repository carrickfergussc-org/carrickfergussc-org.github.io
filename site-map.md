---
layout: default
title: Sitemap
permalink: /sitemap/
---

<h1>Sitemap</h1>

<h2>Pages</h2>
<ul class="sitemap-root">
  {%- assign pages_by_dir = site.pages | sort: "url" | group_by: "dir" -%}
  
  {%- for folder in pages_by_dir -%}
    {%- if folder.name != "/" -%}
      <!-- Sub-directory folder item -->
      <li>
        <strong>{{ folder.name }}</strong>
        <ul>
          {%- for p in folder.items -%}
            {%- if p.title and p.sitemap != false -%}
              <li><a href="{{ p.url | relative_url }}">{{ p.title }}</a></li>
            {%- endif -%}
          {%- endfor -%}
        </ul>
      </li>
    {%- else -%}
      <!-- Root level pages -->
      {%- for p in folder.items -%}
        {%- if p.title and p.sitemap != false -%}
          <li><a href="{{ p.url | relative_url }}">{{ p.title }}</a></li>
        {%- endif -%}
      {%- endfor -%}
    {%- endif -%}
  {%- endfor -%}
</ul>

<h2>Blog Posts</h2>
<ul class="sitemap-posts">
  {%- for post in site.posts -%}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>({{ post.date | date: "%b %d, %Y" }})</small>
    </li>
  {%- endfor -%}
</ul>