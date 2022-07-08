---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
{% for post in site.posts %}
  <h1><a href="{{ post.url }}" style="color: inherit">{{ post.title }}</a></h1>
  <p>Author: {{ post.author }} - {{ post.date | date_to_string }}</p>
  {{ post.excerpt }}
  <h3><a href="{{ post.url }}" style="color: inherit">See More</a></h3>
{% endfor %}
