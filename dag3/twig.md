# Twig

<img src="twig.png" width="600">

* [Drupal render engine - Twig](https://twig.symfony.com/)
* [Drupal Twig dokumentasjon](https://www.drupal.org/docs/develop/theming-drupal/twig-in-drupal)

### Example - `block.html.twig`

```jinja
<div{{ attributes.addClass(classes) }}>
  {{ title_prefix }}
  {% if label %}
    <h2{{ title_attributes }}>{{ label }}</h2>
  {% endif %}
  {{ title_suffix }}
  {% block content %}
    {{ content }}
  {% endblock %}
</div>
```

## Grunnleggende syntax

```jinja
{{ ... }}
```

Example:

```jinja
<h1>{{ page_title }}</h1>
```

### Kjøre logiske operasjoner:

```jinja
{% ... %}
```

Example:

```jinja
{% if title %}
  <h4{{ title_attributes.addClass(title_classes) }}>{{ title }}</h4>
{% endif %}
```

