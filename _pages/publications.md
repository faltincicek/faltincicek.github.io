---
layout: archive
title: "My Publications"
permalink: /publications/
author_profile: true
---

You can also find my most up-to-date publications on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.

### Electronic structures of atomic silicon dimer wires as a function of length
**Altincicek, F. M.**; Livadaru, L.; Leon, C. C.; Chutora, T.; Yuan, M.; Achal, R.; Croshaw, J.; Pitters J.; Wolkow, R. Nanotechnology, 2025. DOI: [10.48550/arXiv.2411.10625](doi.org/10.48550/arXiv.2411.10625)



{% comment %}
{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my most up-to-date publications on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

<!-- New style rendering if publication categories are defined -->
{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}
{% endcomment %}


