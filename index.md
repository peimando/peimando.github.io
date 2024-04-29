---
layout: default
---

## Bienvenido a la página de Ciberseguridad y Redes

¡Hola! Esta es una página estática de ciberseguridad y redes creada con Jekyll. Aquí puedes encontrar información y recursos relacionados con estos temas.

![Cibersecurity](https://img.freepik.com/vector-gratis/vector-fondo-tecnologia-seguridad-datos-tono-azul_53876-112201.jpg "Cibersecurity")
### Artículos recientes

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }})
{% endfor %}



### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
