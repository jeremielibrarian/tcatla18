This will be the home page for our site.

{% for post in site.posts %}
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
    <time datetime="{{ post.date | date_to_long_string }}">{{ post.date | date_to_long_string }}</time>
{% endfor %}
