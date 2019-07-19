# re:docs

jynnie's devlog. she's writing this readme because she forgot how to start this up locally...

`bundle exec jekyll serve`

## main page templates

all main pages need to include a `permalink: /NAME/` in the metadata

the following template should be used for main pages that want to display child data

```
---
layout: post
title: TITLE_HERE
categories: CATEGORY
permalink: /LINK/
---
<div markdown="1">

EXCERPT

<!--more-->

MORE_MARKDOWN

</div>

{%- for post in site.categories.CATEGORY reserved -%}
{%- if post.title != "TITLE_HERE" -%}
<div markdown="1" class="categoryUpdate">
# <a href="{{site.baseurl}}{{ post.url }}">{{ post.title }}</a>

{{ post.excerpt | markdownify }}

<a href="{{site.baseurl}}{{ post.url }}" class="readMore">- read more -</a>
</div>

{%- endif -%}
{%- endfor -%}
```