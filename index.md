---
layout: default
---

## Bienvenido a la página de Ciberseguridad y Redes

¡Hola! Esta es una página estática de ciberseguridad y redes creada con Jekyll. Aquí puedes encontrar información y recursos relacionados con estos temas.

### Artículos recientes
https://github.com/peimando/peimando.github.io/blob/main/_posts/28-04-2024.md

{% for post in site._posts %}
- [{{ post.title }}]({{ post.url }})
{% endfor %}

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/peimando/peimando.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
