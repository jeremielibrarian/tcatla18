This will be the home page for our site.

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url }})  
{{ post.excerpt | strip_html | truncatewords: 50 }}  
{{ post.date | date_to_long_string }}
{% endfor %}
