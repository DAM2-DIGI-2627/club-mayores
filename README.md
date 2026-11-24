# Club Mayores

Aplicación para clubes y asociaciones de personas mayores. Proyecto del módulo
**Digitalización aplicada a los sectores productivos** · 2º DAM · IES Fray Diego Tadeo González · curso 2026/2027.

## El problema

Una asociación de jubilados organiza excursiones, comidas, talleres y viajes, cobra
cuotas y comparte gastos. Hoy lo hace así:

- La excursión se anuncia en un grupo de WhatsApp de 80 personas, las respuestas se mezclan
  con fotos y buenos días, y alguien cuenta a mano quién va.
- Las cuotas se apuntan en una libreta. El café del bar, en la memoria del tesorero.
- Los cumpleaños, en la cabeza de la presidenta.

## Qué vamos a construir

Quien lleva la asociación la da de alta y comparte **un enlace**. Quien abre el enlace
ya es socio. Dentro:

| # | Función | Mínimo viable |
|---|---|---|
| 1 | Asociación e invitación | Crear la asociación y unirse con un enlace, sin contraseñas |
| 2 | Tablón de actividades | El admin publica, los socios reciben un aviso y responden «me apunto» / «no voy» con un toque |
| 3 | Cuentas | Quién ha pagado la cuota, cada excursión, el café. Saldo por socio. **No se cobra nada de verdad** |
| 4 | Cumpleaños | Calendario y aviso el día señalado |

Todo lo demás (coche compartido, fotos, lectura en voz alta…) va al tablero como
ampliación y **solo se toca cuando el mínimo esté terminado**.

Fuera del alcance: un chat. No competimos con WhatsApp; le quitamos lo que hace mal.

## El usuario manda

Nuestros usuarios tienen 70 u 80 años y muchos no se llevan bien con el móvil. Si una
persona mayor no es capaz de apuntarse a una excursión **sin ayuda**, la función no
está terminada, aunque el código funcione.

## Cómo trabajamos

Desde el 25/11/2026. Lo hemos cambiado porque se nos iba el tiempo en gestionar
GitHub en lugar de en desarrollar la aplicación.

1. Cada trabajo es **un fichero** en su ruta (la tabla está en [AGENTS.md](AGENTS.md)).
2. Lo escribes en tu Codespace y le dices a tu IA **«entrégalo»**: ella crea la rama
   y abre la pull request siguiendo [AGENTS.md](AGENTS.md).
3. **Nada entra en `main` sin una pull request aprobada por el profesor.**
   Entregado quiere decir fusionado en `main`.
4. Lo que firmas es tuyo: si no sabes explicarlo, no entra.
5. Cada decisión técnica se escribe en [`docs/decisiones/`](docs/decisiones/).
6. **Nunca** se suben contraseñas, claves ni datos reales de personas al repositorio.

El tablero, las issues y la revisión entre compañeros quedan aparcados.

¿Dudas con algún paso? → [GUIA_GITHUB.md](GUIA_GITHUB.md), apartado 0.

## Materiales de clase

- [Presentación del proyecto](docs/clase/Presentacion_Club_Mayores.pdf)
- [Práctica 1 · GitHub en equipo](docs/clase/Practica01_GitHub_en_equipo.pdf)

## Hitos

| Hito | Se supera cuando… |
|---|---|
| 1 | Un segundo móvil abre el enlace de invitación y queda dado de alta |
| 2 | El admin publica una actividad, **el móvil de una persona mayor recibe el aviso**, responde y el admin lo ve. Sí o no, sin nota parcial |
| 3 | No hay credenciales en el repo, un socio no ve datos de otra asociación y sabemos qué datos personales guardamos |
| 4 | Plan de transformación de la asociación + prueba con al menos 5 personas mayores |

## Equipo

[EQUIPO.md](EQUIPO.md)
