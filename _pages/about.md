---
permalink: /about/
author_profile: false
sidebar:
  - title: Hoon Kim
    # image: http://placehold.it/350x250
    # image_alt: "image"
  - text: 'London N1 0DF'
  - text: 'recruit@hoonio.com'
  - text: 'github.com/hoonio'
---

## Work Experience

{% for post in site.data.resume.work %}

### [{{ post.client }}]({{ post.url}})

**{{ post.title }}** _{{ post.location }}_ _{{ post.period }}_

{{ post.summary }} {% for task in post.tasks %}
- {{ task }} {% endfor %}

{% for stack in post.stacks %}[{{ stack }}](#){: .btn .btn--primary .btn--small} {% endfor %} {% endfor %}

## Education

{% for degree in site.data.resume.education %}

### [{{ degree.institution }}]( {{degree.url }})

{{ degree.title }} _{{ degree.location }}_ _{{ degree.year }}_ {% endfor %}

## Skills

### Publications
{% for cert in site.data.resume.publication %}
- [{{ cert.title }}]({{cert.link}})
{% endfor %}

### Certificates
{% for cert in site.data.resume.certificate %}
- [{{ cert.title }}]({{cert.link}})
{% endfor %}

### Languages
{% for lang in site.data.resume.linguistic %}
- {{ lang.language }} _({{ lang.fluency }})_
{% endfor %}
