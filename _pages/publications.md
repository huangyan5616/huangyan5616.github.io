---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

My articles are also available on [Google Scholar](https://scholar.google.com/citations?user=5P3TXU0AAAAJ&hl=en).

{% include base_path %}
{% assign sorted_publications = site.publications | sort: "date" | reverse %}
{% assign current_year = "" %}

{% for post in sorted_publications %}
{% assign publication_year = post.date | date: "%Y" %}
{% if publication_year != current_year %}
{% unless current_year == "" %}</section>{% endunless %}
<h2 id="{{ publication_year }}">{{ publication_year }}</h2>
<section class="publication-year">
{% assign current_year = publication_year %}
{% endif %}

{% assign publication_authors = post.authors | default: post.excerpt %}
{% assign highlighted_authors = publication_authors | replace: "Yan Huang", "<strong>Yan Huang</strong>" %}

<article class="archive__item" itemscope itemtype="http://schema.org/ScholarlyArticle">
<h3 class="archive__item-title" itemprop="headline">
<a href="{{ base_path }}{{ post.url }}" rel="permalink">{{ post.title }}</a>
</h3>
<p>{{ highlighted_authors }}</p>
<p><em>{{ post.venue }}</em>, {{ publication_year }}</p>
<p>
{% if post.paperurl %}
<a href="{{ post.paperurl }}" class="btn btn--small" target="_blank" rel="noopener noreferrer">Paper</a>
{% endif %}
<a href="{{ base_path }}{{ post.url }}" class="btn btn--small btn--inverse">Abstract</a>
</p>
</article>
{% endfor %}
{% unless current_year == "" %}</section>{% endunless %}
