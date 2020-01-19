---
layout: default
---

<body>
  <div class="index-wrapper">
    <div class="aside">
      <div class="info-card">
        <h1>zhangqi</h1>
        <!--
        <a href="http://weibo.com/beiyuu/" target="_blank"><img src="http://www.weibo.com/favicon.ico" alt="" width="25"/></a>
        <a href="http://www.douban.com/people/beiyuu/" target="_blank"><img src="http://www.douban.com/favicon.ico" alt="" width="22"/></a>
        <a href="http://instagram.com/beiyuu/" target="_blank"><img src="http://d36xtkk24g8jdx.cloudfront.net/bluebar/00c6602/images/ico/favicon.ico" alt="" width="22"/></a>
          -->
      </div>
      <div id="particles-js"></div>
    </div>

    <div class="index-content">
      <ul class="artical-list">
 <!--   {% for post in site.categories.blog %}
        <li>
          <a href="{{ post.url }}" class="title">{{ post.title }}</a>
          <div class="title-desc">{{ post.description }}</div>
        </li>
        {% endfor %}
-->
      {% for cat in site.categories %}
        {% for post in cat[1] %}
          <li>
            <a href="{{ post.url }}" class="title">{{ post.title }}</a>
            <div class="title-desc">{{ post.description }}</div>
          </li>
        {% endfor %}
      {% endfor %}

      </ul>
    </div>
  </div>
</body>

<!--
      {% for cat in site.categories %}
        {% for post in cat[1] %}
          <h2> {{ post.title }} </h2>
        {% endfor %}
      {% endfor %}
-->      