---
layout: default
title: Cómo Ver Procesos del Sistema Asociados a los Puertos con SS en Linux

---

# Cómo Ver Procesos del Sistema Asociados a los Puertos con SS en Linux

El comando `ss` (Socket Statistics) en Linux puede proporcionar información sobre los puertos abiertos y los procesos del sistema asociados a esos puertos. Sin embargo, para ver los procesos del sistema asociados a los puertos, generalmente se requieren permisos de superusuario (root) debido a restricciones de seguridad. Aquí te mostramos cómo utilizar `ss` junto con `sudo` para ver los procesos del sistema asociados a los puertos en tu sistema Linux:

## 1. Ver todos los puertos abiertos con sus procesos asociados

Para ver todos los puertos abiertos junto con los procesos del sistema asociados, puedes ejecutar el siguiente comando:

```
sudo ss -tulpn
```

Este comando utiliza `sudo` para ejecutar `ss` con privilegios de superusuario, lo que permite acceder a información más detallada sobre los procesos del sistema asociados a los puertos. Mostrará una lista de todos los sockets TCP (`-t`) y UDP (`-u`) que están escuchando (`-l`) y no están traducidos (`-n`). La opción `-p` muestra los procesos del sistema asociados a los sockets y la opción `-u` muestra los nombres de los programas en lugar de los números de puerto.

## 2. Filtrar puertos y procesos por estado

Puedes utilizar filtros para ver solo los puertos y procesos en un estado específico. Por ejemplo, si deseas ver solo los puertos en estado LISTEN (escuchando) junto con los procesos asociados, puedes ejecutar el siguiente comando:

```
sudo ss -tulpn state LISTEN
```

Esto mostrará únicamente los puertos que están en estado LISTEN, junto con los procesos del sistema asociados.

## 3. Filtrar puertos y procesos por número de puerto

Si deseas ver solo los detalles de un puerto específico junto con el proceso asociado, puedes filtrar por número de puerto utilizando la opción `sport` o `dport` seguida del número de puerto. Por ejemplo, para ver detalles del puerto 80 y el proceso asociado, puedes ejecutar:

```
sudo ss -tulpn sport = :80
```

Esto mostrará información detallada sobre el socket TCP o UDP que está escuchando en el puerto 80, así como el proceso del sistema asociado.

Recuerda utilizar `sudo` para ejecutar `ss` con privilegios de superusuario y acceder a la información de los procesos del sistema.

¡Utiliza el comando `ss` junto con `sudo` para obtener información detallada sobre los puertos y los procesos del sistema asociados en tu sistema Linux!

Si tienes más preguntas, no dudes en hacerlas.
