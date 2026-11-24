# Normas para agentes de IA · Club Mayores

Trabajas para una persona del equipo. El commit sale a su nombre: ella responde
de él y tiene que saber explicarlo. Habla siempre en castellano.

## Dónde va cada fichero

| Trabajo | Ruta |
|---|---|
| Entrevista a la asociación (AE1.1) | `docs/entrevistas/<usuario-de-github>.md` |
| IT y OT (AE1.2) | `docs/<usuario-de-github>/it-ot.md` |
| Investigación de un tema (AE2.1) | `docs/investigaciones/<tema>.md` |
| Decisión de plataforma y avisos (AE2.2) | `docs/decisiones/0001-plataforma.md` |
| Decisión de datos y alojamiento (AE3.1) | `docs/decisiones/0002-datos.md` |

Temas de investigación: `plataforma`, `avisos`, `accesibilidad`,
`datos-alojamiento`, `datos-personales`.

## Cuando te digan «entrégalo»

1. Comprueba que el fichero está en su ruta y con su nombre. Si no, dilo y
   propón moverlo.
2. Lee el fichero y avisa si encuentras algo de esta lista. Si lo hay, no subas
   nada hasta que la persona lo arregle:
   - restos de un chat pegados (`[span_1]`, «como modelo de lenguaje»…);
   - frases que hablan de otro proyecto;
   - trozos de plantilla sin rellenar;
   - nombres reales o datos personales (se escribe «socia de 78 años»);
   - menos de tres fuentes con enlace;
   - no dice para qué se ha usado la IA.
3. Pregunta: «¿Lo has leído entero y sabes explicarlo?». Sin un «sí», no sigas.
4. Si estás en `main`, crea la rama con `git switch -c <usuario>-<tema>`. Si la
   persona ya tiene una rama con su pull request abierta, trabaja en esa.
5. Enseña qué vas a subir (`git status` y `git diff --stat`) y espera un «sí».
6. Haz el commit, en castellano y diciendo qué añade:
   «Añade la investigación de avisos». Nunca «cambios» ni «arreglo».
7. Sube la rama y abre la pull request hacia `main` con
   `gh pr create --reviewer gabrirobleda`. En la descripción: qué es y para qué
   se ha usado la IA.
8. Da el enlace de la pull request. Ahí termina tu trabajo.

Si el profesor pide cambios, la persona corrige el fichero y te dice «sube los
cambios»: commit y push a la misma rama. La pull request se actualiza sola.

## Prohibido

- Subir a `main`, usar `--force` o `git reset --hard`, borrar ramas de otros.
- Aprobar o fusionar pull requests. Eso lo hace el profesor.
- Tocar ficheros que no sean el que se entrega.
- Subir contraseñas, claves, `.env` o datos reales de personas.
- Escribir tú el contenido del trabajo y subirlo sin que la persona lo lea.

## Si algo falla

- Explica el error en castellano antes de volver a intentarlo.
- Si hay un conflicto, no lo resuelvas a ciegas: enseña los dos lados y propón
  la solución.
