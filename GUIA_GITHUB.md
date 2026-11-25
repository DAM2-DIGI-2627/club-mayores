# Guía de GitHub para el equipo

Lo justo para trabajar juntos sin pisarnos. Si algo no está aquí, búscalo, y
cuando lo encuentres **añádelo a esta guía con una pull request**.

---

## 0. Cómo entregamos (desde el 25/11/2026)

**Por qué lo cambiamos.** Desde el 7 de octubre no había entrado nada en `main`: se
nos iba la hora en gestionar GitHub (issues, tablero, ramas, revisiones) en lugar de
en desarrollar Club Mayores. GitHub es la herramienta, no el trabajo. Ahora la
gestión la hace la IA y la hora es para pensar, escribir y programar.

1. **Abre tu Codespace.** Botón verde **Code** → pestaña **Codespaces** →
   **Create codespace on main**. Otro día abres el mismo y le dices a la IA
   «ponte al día con main».
2. **Comprueba tu IA** (solo el primer día). Pregúntale: «¿qué normas tiene este
   repositorio?». Tiene que contestar con las de [AGENTS.md](AGENTS.md).
3. **Escribe tu fichero** en su ruta (la tabla está en `AGENTS.md`). Puedes usar la
   IA para escribir, pero lo lees entero y dices para qué la has usado.
4. **Di «entrégalo».** La IA revisa el fichero, te pregunta si lo has leído, te
   enseña lo que va a subir, espera tu «sí», crea la rama y abre la pull request
   con el profesor como revisor.
5. **El profesor la lee.** Si aprueba, la fusiona: entregado. Si no, pide cambios
   con un comentario en la pull request.
6. **Si pide cambios**, corriges el fichero en el mismo Codespace y dices «sube los
   cambios». La pull request es la misma.

**Entregado quiere decir fusionado en `main`.** Una pull request abierta está pendiente.

Si GitHub te dice que se te ha acabado Codespaces (*You are out of monthly free
usage…*), mira el [apartado 7](#7-se-te-ha-acabado-codespaces).

Si tu IA no funciona, se entrega igual desde la web: **Add file** → **Create new
file** → escribe la ruta completa → **Commit changes…** → **Create a new branch for
this commit and start a pull request** → **Create pull request**.

Los apartados 2 y 4 explican el sistema anterior (issues, tablero y revisión entre
compañeros). Se quedan como referencia, pero ya no trabajamos así.

---

## 1. Seis palabras

| Palabra | Qué es | Lo mismo, en nuestra app |
|---|---|---|
| **Repositorio** | La carpeta del proyecto *con toda su historia* | La asociación: todo lo que ha pasado en ella |
| **Commit** | Una foto de unos cambios, con autor, fecha y un mensaje que dice *por qué* | Una línea en la libreta del tesorero: quién, cuándo, qué. No se borra |
| **Rama** (*branch*) | Una línea de trabajo paralela. `main` es lo que funciona | Un borrador de actividad que todavía no has publicado |
| **Pull request** (PR) | «Propongo estos cambios, revisadlos» | Un socio **propone** una excursión y el admin la **acepta o la rechaza** |
| **Issue** | Una tarea o un problema, con responsable | Un punto del orden del día |
| **Codespace** | Un ordenador en la nube con VS Code. Nada que instalar | — |

**Git** es el programa que guarda el historial. **GitHub** es la web donde vive el
repositorio común y donde están las issues, las PR y el tablero.

## 2. El ciclo de cualquier cambio (sistema anterior)

```
issue  →  rama  →  commits  →  pull request  →  revisión  →  merge  →  issue cerrada
 #7     issue-7                 "Closes #7"     un compañero   a main
```

1. **Coge una issue** del tablero (o créala). Asígnatela y muévela a *En curso*.
2. **Crea una rama** para ella: `issue-7-boton-apuntarse`.
3. **Haz commits** pequeños con mensajes que se entiendan: `Añade botón «Me apunto» al tablón`.
   Mal: `cambios`, `arreglo`, `asdf`.
4. **Abre una pull request** hacia `main`. En la descripción escribe `Closes #7`: al
   aceptarla, la issue se cierra sola.
5. **Pide revisión** a un compañero. Quien revisa lee el código, lo prueba si hace
   falta y aprueba o pide cambios. **No se aprueba sin mirar.**
6. **Merge**. Borra la rama.

## 3. Reglas del equipo

1. Nada entra en `main` sin PR aprobada por **el profesor**. GitHub lo impide igualmente.
2. Una PR = una cosa. Si tocas tres cosas, son tres PR.
3. **Nunca** subas contraseñas, claves de API, ni ficheros `.env`. Si pasa, avisa: borrarlo en
   un commit nuevo **no basta**, sigue en el historial.
4. **Nunca** subas datos reales de personas (nombres, teléfonos, fechas de nacimiento).
   En las entrevistas, iniciales y edad.
5. Antes de preguntar al profesor, pregunta a la guía, a internet y a un compañero.

---

## 4. Tu primera pull request (desde la web, sin instalar nada)

Vamos a añadir tu fila a `EQUIPO.md`.

1. Abre `EQUIPO.md` en el repositorio y pulsa el **lápiz** (Edit this file).
2. Añade tu fila **al final de la tabla**.
3. Pulsa **Commit changes…**
4. Escribe un mensaje: `Añade a <tu nombre> al equipo`.
5. Marca **Create a new branch for this commit and start a pull request**.
   Nombre de la rama: `equipo-<tu-nombre>`.
6. **Propose changes** → **Create pull request**.
7. En *Reviewers* (a la derecha), elige al compañero que te toque.

### Revisar la PR de otro

1. Pestaña **Pull requests** → la de tu compañero → **Files changed**.
2. Mira el cambio. ¿Está bien escrito? ¿Ha tocado solo lo que debía?
3. **Review changes** → *Approve* (o *Request changes* explicando qué falta) → **Submit review**.
4. Con la aprobación, el autor pulsa **Merge pull request**.

### «This branch has conflicts»

Os va a pasar hoy, **a propósito**: todos habéis añadido una línea en el mismo sitio.
Git no adivina cuál va primero: te pregunta.

1. En la PR, pulsa **Resolve conflicts**.
2. Verás algo así:
   ```
   <<<<<<< equipo-lucia
   | Lucía | @lucia | ... |
   =======
   | Mario | @mario | ... |
   >>>>>>> main
   ```
3. Deja **las dos filas**, borra las tres líneas de marcas (`<<<<<<<`, `=======`, `>>>>>>>`).
4. **Mark as resolved** → **Commit merge**. Pide revisión de nuevo.

---

## 5. Lo mismo desde Codespaces (lo usaremos para programar)

En el repositorio: botón verde **Code** → pestaña **Codespaces** → **Create codespace on main**.
Se abre VS Code en el navegador. En la terminal:

```bash
git switch main
git pull                              # traer lo último
git switch -c issue-7-boton-apuntarse # rama nueva
# ... programas ...
git add .
git commit -m "Añade botón «Me apunto» al tablón"
git push -u origin issue-7-boton-apuntarse
```

Después, GitHub te ofrece **Compare & pull request**. A partir de ahí, igual que en el apartado 2.

Comandos para no perderse:

| Comando | Para qué |
|---|---|
| `git status` | ¿En qué rama estoy y qué he cambiado? **Úsalo siempre que dudes** |
| `git log --oneline -10` | Los últimos 10 commits |
| `git diff` | Qué he cambiado y aún no he guardado en un commit |
| `git switch main && git pull` | Volver a `main` y traer lo último |

El Codespace se para solo si no lo usas, pero **no se borra**: lo que no hayas subido con
`git push` solo existe ahí. Sube antes de irte.

---

## 6. Registrar una decisión

Cuando el equipo decide algo que cuesta cambiar después (la plataforma, dónde guardar los
datos, cómo se entra sin contraseña…), se escribe en `docs/decisiones/`, copiando
`0000-plantilla.md`. Numeración correlativa: `0001-plataforma.md`, `0002-datos.md`…
Se sube con una PR como cualquier otro cambio: así la decisión también se revisa.

---

## 7. Se te ha acabado Codespaces

Si al abrir tu Codespace sale *«You are out of monthly free usage or have exceeded
your budget for Codespaces»*, no has tocado nada mal: se ha gastado tu cuota gratuita.

**Qué pasa.** Codespaces no lo paga el instituto: lo paga **tu cuenta personal** de
GitHub, aunque el repositorio sea de la clase. Cada mes tienes gratis:

| Cuenta | Tiempo de máquina | Almacenamiento |
|---|---|---|
| GitHub Free | 120 h de núcleo (con la máquina de 2 núcleos, **60 h reales**) | 15 GB·mes |
| GitHub Pro (gratis con el *Student Pack*) | 180 h de núcleo (90 h reales) | 20 GB·mes |

- Cuentan **todos** tus codespaces, de cualquier repositorio, también los que ya
  hayas borrado este mes.
- El tiempo solo corre con el codespace **encendido**; el almacenamiento corre
  mientras el codespace **exista**, aunque esté parado.
- Los GB que salen en la tarjeta del codespace (10 GB o más) **no** son lo que te
  cobran: casi todo es la imagen base de GitHub, que no cuenta.
- La cuota vuelve el **día 1 de cada mes**.

**Qué hacer.**

1. **No borres nada todavía.** Si en la lista de codespaces tu rama sale con
   asterisco (`equipo-lucia*`), tiene cambios sin subir. En los **`···`** del
   codespace → **Export changes to a branch** → **Create branch**. Funciona aunque no
   te quede cuota. Se crea una rama `codespace-…` con tu trabajo.
2. **Mira en qué se ha ido.** *github.com/settings/billing* → uso de Codespaces, por
   día y por repositorio.
3. **Borra los codespaces que no uses** en *github.com/codespaces*. Lo exportado o
   subido con `git push` ya está a salvo en GitHub.
4. **Hasta el día 1**, entrega desde la web (final del [apartado 0](#0-cómo-entregamos-desde-el-25112026))
   o edita con **github.dev**: en el repositorio, pulsa la tecla `.` (punto). Es un
   VS Code en el navegador que no gasta cuota, aunque no tiene terminal ni IA.

**Para que no te pase.**

- **Un codespace por repositorio.** Otro día abres el mismo; no crees uno nuevo cada vez.
- Antes de irte: `git push` y, en *github.com/codespaces*, **`···` → Stop codespace**.
- Pide el **GitHub Student Pack**: te da GitHub Pro y más cuota. Los pasos están
  justo debajo.
- Si no vas a usar un codespace en semanas, **bórralo**: GitHub los borra solos a los
  30 días sin uso, y con ellos lo que no hayas subido.

### Pedir el Student Pack

No es una cuenta nueva: se pide **sobre tu cuenta de GitHub de siempre**. Es gratis
mientras estudies y te da **GitHub Pro** (180 h de núcleo y 20 GB de Codespaces al
mes) y **Copilot Pro**, entre otras cosas.

**Antes de empezar** (si falta algo de esto, te lo rechazan):

1. **Verificación en dos pasos activada.** *github.com/settings/security* →
   *Enable two-factor authentication*. Con una app del móvil (Google Authenticator,
   Microsoft Authenticator…). Guarda los códigos de recuperación.
2. **Tu nombre real** en el perfil (*github.com/settings/profile* → *Name*), igual
   que en el documento que vas a subir.
3. **Un justificante de que estudias aquí** donde se vean **tres cosas**: tu nombre
   completo, el nombre del instituto y una fecha de este curso. Lo mejor es el
   certificado de matrícula de 2026/27 (pídelo en secretaría); el carné de estudiante
   vale si lleva fecha. Ten la foto a mano en el móvil o en el ordenador.

**La solicitud** (mejor desde el instituto, ayuda con la ubicación):

1. Entra en **education.github.com/pack** → **Get student benefits** (o *Sign up for
   Student Developer Pack*).
2. Elige **Student**. Si te pide un correo del centro, añade el de Educacyl
   (`@educa.jcyl.es`) a tu cuenta y confírmalo.
3. Escribe el nombre del centro: **IES Fray Diego Tadeo González**. Si no aparece en
   la lista, escríbelo entero.
4. Cuando el navegador pregunte si puede usar tu **ubicación**, di que **sí**.
5. Si te pide prueba, haz o sube la **foto del justificante**. Que se lea bien: sin
   reflejos y sin cortar los bordes.
6. **Submit** y espera. Puede tardar desde unas horas hasta unos días. Te llega un
   correo con la respuesta.

**Si te lo aprueban**, los beneficios pueden tardar hasta 3 días en aparecer. Lo
compruebas en *github.com/settings/billing*: tu plan pasa a **Pro**.

**Si te lo rechazan**, el correo dice por qué (casi siempre es la foto o el nombre).
Lo corriges y lo vuelves a pedir. Si a la segunda tampoco, díselo al profesor.
