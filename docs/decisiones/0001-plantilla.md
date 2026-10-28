y programable en Codespaces.
# 0001 · Plataforma de la app

- **Estado:** propuesta
- **Autor/a:** Cristofer
- **Fecha:** 2026-10-28
- **Issue:** Pendiente

## Problema

Club Mayores la usarán personas mayores con Android y con iPhone. Necesitamos
que puedan entrar desde una invitación por WhatsApp y recibir avisos de
actividades, mientras desarrollamos en el aula sin instalar nada y con una hora
a la semana.

## Requisitos que debe cumplir

- Alta en 2–3 toques desde un enlace de invitación.
- Avisos en Android y en iPhone.
- Sin instalar herramientas en el aula y programable en Codespaces.
- Coste 0 € y sin cuentas de desarrollador.

## Alternativas estudiadas

| Opción | A favor | En contra | Coste (nivel gratuito y qué pasa si se supera) |
|---|---|---|---|
| Kotlin + Android Studio (Jetpack Compose) | Aprovecha lo que vemos en PMDM. | No cumple el requisito de llegar a personas con iPhone. | Pendiente de estimar. |
| Web instalable (PWA): HTML, CSS, JavaScript, manifest y service worker | Una base de código para todos los móviles; se publica con un enlace y las actualizaciones llegan sin pasar por una tienda. | En iPhone, los avisos requieren añadirla a la pantalla de inicio. Hace falta HTTPS y un servidor para las altas y los avisos. | 0 € según la propuesta; revisar límites y posibles costes del servidor. |
| Flutter (Dart) | Pendiente de valorar. | No aprovechamos directamente lo que vemos en PMDM (Kotlin/Compose). | Pendiente de estimar. |

## Decisión

Elegimos la **PWA**. Es la única que cumple a la vez: alta en 2–3 toques desde
un enlace, avisos en Android y en iPhone, coste 0 €, sin cuentas de desarrollador
y programable en Codespaces.

## Consecuencias

- Una sola base de código para todos los móviles; se publica con un enlace.
- Las actualizaciones llegan solas, sin pasar por ninguna tienda.
- En iPhone, los avisos solo funcionan si la persona la añade a la pantalla de
  inicio: hay que enseñarlo, con capturas, en la sesión de alta.
- Hace falta HTTPS y un servidor para las altas y los avisos.
- No aparecemos en Play Store ni en la App Store; hay gente que confía más en
  «la tienda».
- Menos acceso al hardware del móvil, que no nos hace falta por ahora.
- Más adelante podemos envolver la PWA como app Android (TWA) con Android
  Studio si la asociación quiere estar en Play Store.

## Fuentes

Pendiente: añadir enlaces a la documentación oficial consultada.
