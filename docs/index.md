This will be the home page for our site.

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url | relative_url }})  
{{ post.date | date_to_long_string }}  
{{ post.excerpt | strip_html | truncatewords: 50 }}
{% endfor %}
