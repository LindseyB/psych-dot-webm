{% for folder in site.data.folders %}
  {% for image in site.static_files %}
    {% if image.extname contains 'webm' and image.path contains folder.name %}
      <video loop muted autoplay>
        <source src="{{ image.path }}" type="video/webm">
      </video>
    {% endif %}
  {% endfor %}
{% endfor %}
