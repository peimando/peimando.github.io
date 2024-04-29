---
layout: default
title: Uso de iptables para bloquear solicitudes GET

---

# Uso de iptables para bloquear solicitudes GET en el puerto 7022

Iptables es una potente herramienta de filtrado de paquetes en sistemas Linux. Permite configurar reglas de firewall para controlar el tráfico de red entrante y saliente. A continuación, te mostraremos cómo utilizar iptables para bloquear solicitudes GET en el puerto 7022:

## 1. Accede al servidor

Accede al servidor Linux donde deseas aplicar las reglas iptables. Puedes conectarte mediante SSH u otro método de acceso remoto.

## 2. Ejecuta el comando iptables

Ejecuta el siguiente comando para bloquear las solicitudes GET en el puerto 7022:

```shell
iptables -I DOCKER-USER 1 -p tcp -d 172.18.0.3 --dport 7022 -m string --string "GET" --algo kmp --to 65535 -j DROP
```

Este comando inserta una nueva regla en la cadena de reglas DOCKER-USER. La regla especifica que los paquetes TCP destinados al puerto 7022 y que contengan la cadena "GET" en el payload del paquete serán rechazados (DROP).

Asegúrate de reemplazar "172.18.0.3" con la dirección IP correcta del destino en tu entorno.

## 3. Verifica las reglas iptables

Para verificar que la regla se haya aplicado correctamente, ejecuta el siguiente comando:

```shell
iptables -L DOCKER-USER
```

Este comando mostrará todas las reglas en la cadena DOCKER-USER. Asegúrate de que la regla que bloquea las solicitudes GET en el puerto 7022 esté presente en la lista.

## 4. Guarda las reglas iptables

Para que las reglas iptables se mantengan después de reiniciar el servidor, debes guardarlas. El método para hacerlo puede variar según la distribución de Linux que estés utilizando.

En la mayoría de las distribuciones, puedes utilizar el siguiente comando:

```shell
iptables-save > /etc/iptables/rules.v4
```

Este comando guarda las reglas iptables en un archivo llamado "rules.v4" en el directorio "/etc/iptables".

## 5. Prueba las reglas

Una vez que las reglas se hayan aplicado y guardado, puedes realizar pruebas para verificar que las solicitudes GET en el puerto 7022 estén bloqueadas correctamente.

Intenta realizar una solicitud GET al servidor en el puerto 7022 desde un cliente externo. La solicitud debería ser rechazada y no recibirás respuesta.

Recuerda que el uso correcto de iptables requiere un conocimiento sólido de las reglas de firewall y la configuración de red. Asegúrate de comprender el impacto de las reglas que estás aplicando y de tener medidas de seguridad adecuadas en tu entorno.

Si necesitas más información sobre iptables y cómo utilizarlo, consulta la documentación oficial de iptables y otros recursos en línea.

¡Utiliza iptables de manera adecuada para fortalecer la seguridad de tu servidor y protegerlo contra solicitudes no deseadas!

