---
layout: page
title: blog
categories: blog
permalink: /blog/
---

{%- for category in site.categories -%}
{%- if category[0] == "blog" -%}
{%- assign posts = category[1] | sort: 'date' -%}
<ul class="post-list">
  {%- for post in posts -%}
    <li>
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <span class="post-meta">{{ post.date | date: date_format }}</span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        {{ post.excerpt }}
      </li>
  {%- endfor -%}
</ul>
{%- endif -%}
{%- endfor -%}