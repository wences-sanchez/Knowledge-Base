```
{% if category %}
{% if category == "books" %}
{% if "Literature" in document_tags %} DECK: Literature-Quotes::{{title}}
{% elif "UNI" in document_tags %} DECK: UNI::{{title}}
{% elif "O'Reilly-Learning" in document_tags %} DECK: O'Reilly-Learning::{{title}}
{% elif "Self-Help" in document_tags %} DECK: Self-Help::{{title}}
{% elif "Science" in document_tags %} DECK: Science::{{title}}
{% else %}
DECK: Other-Books::{{title}}
{% endif -%}
{% elif category == "articles" %}
DECK: Across-the-Net
{% endif -%}
{% endif %}
{% if image_url -%}
![rw-book-cover]({{image_url}})

{% endif -%}

## Info:
- Author: {% if author %}[[{{author}}]]{% endif %}
- Full Title: {{full_title}}
- Category: #{{category}}
{% if document_tags -%}
- Document Tags: {% for tag in document_tags %}#{{tag}} {% endfor %}
{% endif -%}
{% if url -%}
- URL: {{url}}

{% else %}

{% endif -%}
FILE TAGS: {% for tag in document_tags %}{{tag}} {% endfor %}
#tags {% for tag in document_tags %}#{{tag}} {% endfor %}
```

