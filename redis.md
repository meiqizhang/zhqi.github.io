---
layout: default
---

<body>
  <div class="index-wrapper">
    <div class="aside">
      <div class="info-card">

        <div align="left">
          {% for post in site.categories.redis %}
            {% assign tags = tags | concat : post.tags | uniq %}
          {% endfor %}
          
          {% for tag in tags %}
            <h3>&nbsp;</h3>
            <a href="leetcode-{{ tag }}" class="title">{{ tag }}</a>
          {% endfor %}
        </div>

      </div>
        <div id="particles-js"></div>
      </div>

    <div class="index-content">
      <ul class="artical-list">
        {% for post in site.categories.redis %}
          <li>
            <a href="{{ post.url }}" class="title">{{ post.title }}</a>
            <div class="title-desc">{{ post.description }}</div>
          </li>
        {% endfor %}
      </ul>
    </div>
    
  </div>
</body>