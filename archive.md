---
layout: default
title: AAKR | Archive
---
<div id="articles">
<section id="archive">
  {%for post in site.posts %}
      {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
      {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
      {% if year != nyear %}
        </ul>
        <h3>{{ post.date | date: '%Y' }}</h3>
        <ul class="past">
      {% endif %}
      <li><time>{{ post.date | date:"%d %b" }}</time> -- <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a> by {{ post.author }}</li>
  {% endfor %}
  </ul>
</section>
</div>
