---
layout: default
---

## Bienvenido a la página de Ciberseguridad y Redes

¡Hola! Esta es una página estática de ciberseguridad y redes creada con Jekyll. Aquí puedes encontrar información y recursos relacionados con estos temas.

![Cibersecurity]([http://www.tecmint.com/wp-content/uploads/2015/05/Linux-Health-Monitoring.png](https://img.freepik.com/vector-gratis/vector-fondo-tecnologia-seguridad-datos-tono-azul_53876-112201.jpg?w=1380&t=st=1714424763~exp=1714425363~hmac=d68d1ccf2a9da30328aee5bbfc38928afeeb7a28c6915b4888184faa3b677cfe) "Cibersecurity")
### Artículos recientes

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }})
{% endfor %}



### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
