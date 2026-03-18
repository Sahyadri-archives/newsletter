---
layout: page
title: Newsletter
permalink: /posts/
---

<div id="top" style="scroll-margin-top: 150px;"></div>

<div class="newsletter-container">
  
  <aside class="toc-sidebar">
    <nav class="toc-card">
      <h2 class="toc-title">Editions</h2>
      <ul class="toc-list">
        {% assign grouped_posts = site.posts | group_by: "category" %}
        {% for group in grouped_posts %}
          {% assign category_id = group.name | slugify | default: "general-updates" %}
          <li><a href="#{{ category_id }}">{{ group.name | default: "General Updates" }}</a></li>
        {% endfor %}
      </ul>
    </nav>
  </aside>

  <div class="posts-list">
    {% for group in grouped_posts %}
      {% assign category_id = group.name | slugify | default: "general-updates" %}
      
      <section class="term-section" id="{{ category_id }}">
        <h2 class="category-heading">
          {{ group.name | default: "General Updates" }}
        </h2>

        {% comment %} 
          This is the key change: we sort the items in this category group 
          by the "weight" property defined in your post's Front Matter.
        {% endcomment %}
        {% assign sorted_posts = group.items | sort: "weight" %}

        {% for post in sorted_posts %}
          <article class="post-preview">
            <a href="{{ post.url | relative_url }}" style="text-decoration: none;">
              <h3 class="post-title">{{ post.title }}</h3>
              {% if post.subtitle %}
                <h4 class="post-subtitle">
                  {{ post.subtitle }}
                </h4>
              {% endif %}
            </a>

            <p class="post-meta">
              Posted on {{ post.date | date: site.date_format }}
            </p>

            <div class="post-entry-container">
              {% if post.image %}
                <div class="post-image">
                  <a href="{{ post.url | relative_url }}">
                    {% comment %} Added leading slash to help with the 404 issues {% endcomment %}
                    <img src="{{ post.image | prepend: '/' | relative_url }}" alt="{{ post.title }}">
                  </a>
                </div>
              {% endif %}
              
              <div class="post-entry">
                {{ post.excerpt | strip_html | truncatewords: 30 }}
                <a href="{{ post.url | relative_url }}" class="post-read-more">[Read&nbsp;More]</a>
              </div>
            </div>
          </article>
        {% endfor %}
        
        <div class="back-to-top">
            <a href="#top">↑ Back to top</a>
        </div>
      </section>
    {% else %}
      <p>No newsletters found. Check back soon!</p>
    {% endfor %}
  </div>
</div>
