# Plataforma: ¿web instalable, app nativa o Flutter?

## Contexto
Club Mayores es una aplicación pensada para asociaciones de personas mayores. Hoy estas asociaciones organizan excursiones, comidas y cuotas con un grupo de WhatsApp de unas 80 personas, donde las respuestas se mezclan con fotos y buenos días, y con una libreta para llevar las cuentas. La idea es ayudarles de forma simple a unirse a las actividades del club.

La aplicación debe permitir entrar con un enlace de invitación, sin contraseñas, publicar actividades en un tablón con aviso a los socios y que estos respondan con un toque. También lleva el control de cuotas y gastos con el saldo de cada socio, sin cobrar nada de verdad, y un calendario de cumpleaños con aviso.

Lo que más condiciona la plataforma es la edad de los usuarios, de 70 u 80 años. Una persona mayor debe poder apuntarse a una actividad sin ayuda, y para superar el hito 2 el móvil de una persona mayor tiene que recibir el aviso. Por eso la forma de entregar esos avisos pesa mucho en la decisión.

## Alternativas
### Web instalable (PWA)
Una web que se puede instalar en el móvil con su propio icono y que se abre como una app, sin pasar por una tienda de aplicaciones. Se entra con un enlace, y requiere HTTPS y un manifiesto.

### App nativa
Una app hecha específicamente para cada sistema, con sus propios lenguajes y herramientas (Kotlin para Android, Swift para iPhone). Se publica en las tiendas de aplicaciones y hay que mantener dos versiones.

### Flutter
Un framework gratuito y de código abierto de Google que permite hacer una sola app para Android y iPhone con un único código. También se publica en las tiendas de aplicaciones.

## Criterios
1. **Entrada por enlace, sin contraseña:** la invitación debe bastar para ser socio.
2. **Avisos en el móvil de una persona mayor:** requisito del hito 2.
3. **Uso sin ayuda:** una persona de 70 u 80 años debe poder usarla sola.
4. **Coste y mantenimiento:** el equipo dispone de poco tiempo (una hora a la semana).
5. **Conocimientos del equipo:** cuánto hay que aprender de cero.

## Comparación
| Criterio | PWA | App nativa | Flutter |
|---|---|---|---|
| Entrada por enlace | Sí, se abre directamente con el enlace | Hay que instalarla antes desde la tienda | Hay que instalarla antes desde la tienda |
| Avisos | Android: sí. iPhone: Apple lo admite en webs añadidas a la pantalla de inicio (iOS 16.4 o superior) | Sí, con Firebase Cloud Messaging (guías para Android e iOS) | Sí, con el plugin firebase_messaging para Android e iOS |
| Uso sin ayuda | Instalar en iPhone puede resultar poco intuitivo para una persona mayor | Buscar e instalar desde la tienda también requiere ayuda | Igual que la nativa |
| Coste y mantenimiento | Una sola web | Dos apps que mantener | Un solo código, pero con tiendas y, para iPhone, Xcode |
| Conocimientos del equipo | Tecnologías web (HTML, CSS, JavaScript) | Dos lenguajes distintos (Kotlin y Swift) | Un lenguaje nuevo (Dart) |

## Recomendación
Recomiendo una **PWA** (web instalable). Es la única que se abre directamente con el enlace de invitación, sin instalar nada antes, necesita un solo código que mantener y utiliza tecnologías web, así que encaja con el poco tiempo del equipo.

Su punto débil son los avisos en iPhone, que Apple admite en webs añadidas a la pantalla de inicio. Para reducir ese riesgo, la primera pantalla de la web debería explicar con pasos sencillos cómo instalarla, y habría que probarlo con personas mayores reales (hito 4). Si esa prueba falla en iPhone, el plan B sería una app de tienda hecha con Flutter, que mantiene un solo código para Android y iPhone.

Antes de cerrar la decisión conviene averiguar qué móviles usan los socios, porque en Android los avisos funcionan.

## Fuentes
1. MDN Web Docs, «Making PWAs installable»: https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Guides/Making_PWAs_Installable
2. Apple Developer, «Sending web push notifications in web apps and browsers»: https://developer.apple.com/documentation/usernotifications/sending-web-push-notifications-in-web-apps-and-browsers
3. web.dev, «Progressive Web App checklist»: https://web.dev/pwa-checklist/
4. Firebase, «Get started with Firebase Cloud Messaging in Flutter apps»: https://firebase.google.com/docs/cloud-messaging/flutter/client

## Uso de IA
He usado IA (Claude y Copilot) para buscar fuentes, proponer el esquema del documento y redactar y corregir borradores. He leído y revisado el contenido completo.