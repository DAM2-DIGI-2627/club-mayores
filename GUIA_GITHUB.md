# Guía de GitHub para el equipo

Lo justo para trabajar juntos sin pisarnos. Si algo no está aquí, búscalo, y
cuando lo encuentres **añádelo a esta guía con una pull request**.

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

## 2. El ciclo de cualquier cambio

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

1. Nada entra en `main` sin PR aprobada por **otra persona**. GitHub lo impide igualmente.
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
