# practica-solid-poo

Quiero hacer en aproximadamente una hora un mini proyecto en TypeScript para practicar POO y SOLID. No quiero que escribas todo el código por mí: guiame paso a paso, explicando cada decisión y revisando mi código cuando te lo comparta.

Proyecto: Sistema de notificaciones de una aplicación.

Objetivo:
Un usuario puede crear una notificación y enviarla por distintos canales: correo, SMS o notificación interna. Cada canal debe comportarse de manera intercambiable.

Requisitos mínimos:
- Clase Usuario: id, nombre y contacto.
- Clase Notificacion: mensaje, usuario destinatario y estado de envío.
- Interfaz ICanalNotificacion con el método enviar(notificacion).
- Clases Correo, SMS y NotificacionInterna que implementen ICanalNotificacion.
- Clase ServicioNotificaciones que reciba un ICanalNotificacion por constructor y envíe notificaciones sin saber qué canal concreto usa.
- Validar que el mensaje no esté vacío y que el usuario sea válido.
- Guardar las notificaciones enviadas en una colección privada y devolver copias para no exponerla.
- Hacer tests cortos con Vitest.

Conceptos que quiero aplicar y explicar:
- Encapsulamiento: atributos privados, getters y métodos que protejan reglas.
- Abstracción: interfaz para definir el contrato de envío.
- Polimorfismo: que ServicioNotificaciones funcione igual con Correo, SMS o NotificacionInterna.
- Composición: ServicioNotificaciones tiene un canal y administra una colección.
- SOLID:
  - SRP: cada clase con una única responsabilidad.
  - OCP: poder agregar WhatsApp sin modificar ServicioNotificaciones.
  - DIP: depender de ICanalNotificacion, no de Correo o SMS.
  - ISP: la interfaz debe ser pequeña y específica.
- Herencia: analizá conmigo si realmente hace falta una clase abstracta CanalNotificacion o si alcanza con interfaz. No agregues herencia artificialmente.

Restricciones:
- Identificadores y clases en español.
- No usar if ni switch; usar validaciones con booleanos, operadores lógicos, métodos de colección o polimorfismo.
- Interfaces sólo con métodos, sin atributos.
- Hacer commits simples luego de cada avance importante.

Empezá proponiendo la estructura de carpetas, las clases, responsabilidades, interfaces y tests mínimos. Después avanzamos de a una clase, explicando antes de escribir código.
