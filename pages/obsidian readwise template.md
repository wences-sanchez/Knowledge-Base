```
{% if highlight_note %}
#flashcard {% if highlight_tags %}{% for tag in highlight_tags %}#{{tag}} {% endfor %}{% endif %}
{{ highlight_note }}

---
{{ highlight_text }}

{% else %}
#spaced {% if highlight_tags %}{% for tag in highlight_tags %}#{{tag}} {% endfor %}{% endif %}
{{ highlight_text }}

{% endif %}
{% if highlight_location and highlight_location_url %} ([{{highlight_location}}]({{highlight_location_url}})){% elif highlight_location %}({{highlight_location}}){% endif %}

---
```

