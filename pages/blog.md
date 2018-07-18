---
title: Blog
permalink: "/blog/"
layout: page
feature-img: assets/img/pexels/biblioteca.png
---
<input type="text" id="search-input" placeholder="Palabras clave..." class="search-bar">
<br>
<br>
<ul id="results-container"></ul>

<section>
    <!-- Script pointing to jekyll-search.js -->
    <script src="{{ site.baseurl }}/assets/js/vendor/simple-jekyll-search.min.js" type="text/javascript"></script>

    <script type="text/javascript">
        SimpleJekyllSearch({
            searchInput: document.getElementById('search-input'),
            resultsContainer: document.getElementById('results-container'),
            json: '{{ site.baseurl }}/assets/data/search.json',
            searchResultTemplate: '<div class="search-title"><a href="{url}"><h3> {title}</h3></a><div class="meta">{date} <div class="right"><i class="fa fa-tag"></i> {tags}</div></div><p>{excerpt}</p></div><hr> ',
            noResultsText: 'No results found',
            limit: 10,
            fuzzy: false,
            exclude: []
        })
    </script>
</section>
<SECTION>
<div class="posts">
    {% for post in paginator.posts %}
    <div class="post-teaser">
      {% if post.thumbnail %} 
      <div class="post-img">
         <img src="{{ site.baseurl }}/{{ post.thumbnail }}">
      </div>
      {% endif %}
      <span>
          <header>
            <h1>
              <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
                {{ post.title }}
              </a>
            </h1>
            <p class="meta">
              {{ post.date | date: "%B %-d, %Y" }}
            </p>
          </header>
          <div class="excerpt">
              {{ post.excerpt | strip_html | escape }}
            <!--{{ post.content | strip_html | truncate: "250" }}-->
            <!--<a class="button" href="{{ post.url | prepend: site.baseurl }}">
              {{ site.theme_settings.str_continue_reading }}
            </a>-->
          </div>
      </span>
    </div>
    {% endfor %}
  </div>

  {% if paginator.total_pages > 1 %}
  <div class="pagination">
    {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}" class="button" >
      <i class="fa fa-chevron-left"></i>
      {{ site.theme_settings.str_previous_page }}
    </a>
    {% endif %}
    {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}" class="button" >
      {{ site.theme_settings.str_next_page }}
      <i class="fa fa-chevron-right"></i>
    </a>
    {% endif %}
  </div>
  {% endif %}
</div>
</SECTION>