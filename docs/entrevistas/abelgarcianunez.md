# Entrevista a la Asociación: Club de Mayores "Nuestra Señora del Rosario" y Propuesta de Transformación Digital

**Módulo:** Digitalización aplicada (1665) · 2º DAM[span_1](start_span)[span_1](end_span)  
**Autor / Alumno:** Abel García Núñez[span_2](start_span)[span_2](end_span)  
**Fecha:** 09/10/2026[span_3](start_span)[span_3](end_span)  
**Ubicación del archivo en el repositorio:** `docs/entrevistas/abelgarcianunez.md`[span_4](start_span)[span_4](end_span)

---

## 1. Introducción y Metodología

Para comprender la realidad operativa de una entidad sin ánimo de lucro de carácter social y analógico, se ha realizado una entrevista semiestructurada a un miembro de la junta directiva de un hogar del pensionista y club de mayores de nuestro entorno (en adelante, la "socia de 78 años", miembro del órgano de secretaría y tesorería). El objetivo es analizar los flujos de trabajo actuales, identificar cuellos de botella e implantar una perspectiva de digitalización y entornos IT ajustada a las necesidades del proyecto de gestión de vehículos y actividades que vertebra nuestro TFG.

Como apoyo en la estructuración de la síntesis de datos y en la redacción técnica de este informe se ha empleado inteligencia artificial (utilizada estrictamente como asistente de redacción y estructuración conceptual, bajo supervisión humana total y comprensión de cada línea de código/texto generada, cumpliendo con la exigencia metodológica de la tarea).

---

## 2. Análisis de la Organización Actual (Cómo Funciona Hoy)

En la actualidad, el funcionamiento diario del club de mayores descansa casi de manera absoluta en procedimientos manuales y físicos:

*   **Convocatorias y Avisos:** Las reuniones de la junta directiva se convocan de manera verbal o mediante llamadas telefónicas individuales. Los avisos generales a los socios (excursiones, cambios de horario en el centro, torneos de brisca o lotería) no se digitalizan; se publican en un tablón de corcho físico situado en la entrada del local o se difunden mediante el boca a boca.
*   **Inscripciones:** Para apuntarse a cualquier actividad (por ejemplo, una comida de hermandad o un viaje subvencionado), los socios deben acudir físicamente al centro en horario de apertura y rellenar una hoja de papel o la secretaria anota el nombre a mano en un cuaderno cuadriculado.
*   **Cuotas y Gastos:** El cobro de la cuota anual de socio (fijada en una cantidad simbólica) se realiza mayoritariamente en efectivo durante los primeros meses del año, o bien mediante entregas en mano a la tesorera. La tesorería lleva el control contable anotando los ingresos y los gastos (facturas de luz, agua, café y mantenimiento del local) en un libro de cuentas físico de formato apaisado. Los recibos de pagos a proveedores se archivan en carpetas de cartón con fundas de plástico.

---

## 3. Procesos Digitalizables vs. Falsa Digitalización (Escanear no es Digitalizar)

### El error común: escanear la libreta
Un error frecuente al abordar la transformación digital de entidades tradicionales consiste en creer que digitalizar un proceso equivale a convertir el soporte físico en un archivo digital estático (por ejemplo, hacer una fotografía o escanear con el móvil las páginas del cuaderno de contabilidad o de la lista de socios en formato PDF o imagen). 

*   **Por qué no es digitalización:** Escanear la libreta genera un documento inalterable y aislado. Sigue exigiendo introducir los datos a mano previamente, no previene errores humanos de cálculo, no permite realizar búsquedas automatizadas eficientes, no actualiza de forma concurrente el estado de tesorería y no automatiza avisos ni validaciones. El dato sigue "atrapado" en una imagen estática.

### Procesos reales susceptibles de digitalización
1.  **Registro y Censo de Socios:** Migrar de la libreta física a una base de datos relacional (ej. gestionada mediante una aplicación con backend en Firebase Firestore o almacenamiento estructurado), lo que permite consultar al instante quién está al corriente de pago, su número de socio o sus datos de contacto de emergencia.
2.  **Gestión de Tesorería y Recibos:** Sustituir el libro de contabilidad manual por un software de gestión financiero-contable automatizado que calcule balances mensuales, registre ingresos por categorías y emita comprobantes digitales.
3.  **Canales de Comunicación Dinámicos:** Implementar un sistema de notificaciones automatizadas o un grupo de difusión moderado, combinando el tablón tradicional con un canal digital accesible para familiares o socios familiarizados con dispositivos móviles.

---

## 4. Reorganización de la Junta Directiva (Presidencia, Tesorería y Secretaría)

La introducción de un entorno digital integrado cambiará sustancialmente las funciones y la carga de trabajo de los miembros de la junta directiva (presidencia, tesorería y secretaría), optimizando los recursos humanos disponibles:

*   **Secretaría:** 
    *   *Tareas que desaparecen:* Copiar a mano las listas de asistentes, redactar actas físicas en papel con riesgo de pérdida y transcribir fichas de inscripción.
    *   *Tareas que cambian:* Se encarga de validar altas de socios directamente en la interfaz de la aplicación, mantener actualizada la base de datos de contactos y redactar las actas en formato digital (markdown o procesador de textos indexado).
*   **Tesorería:**
    *   *Tareas que desaparecen:* Realizar sumas manuales en el libro de cuentas, puntear recibos de papel uno a uno y buscar errores de cuadre en sumatorios aritméticos.
    *   *Tareas que cambian:* Introduce los importes de cobros y pagos en el sistema informático. La aplicación calcula de forma automática y matemática los totales, saldos y desgloses por conceptos, aplicando criterios estrictos de precisión (como truncamientos decimales exactos en los cálculos medios, evitando desviaciones contables).
*   **Presidencia:**
    *   *Tareas que desaparecen:* Dedicar gran parte de su tiempo a mediar en conflictos de información (por ejemplo, discusiones sobre quién pagó antes una excursión) o a la burocracia de recopilar papeles.
    *   *Tareas que cambian:* Accede a cuadros de mando (dashboards) visuales e informes periódicos generados por el sistema para tomar decisiones estratégicas fundamentadas (ej. viabilidad económica de organizar una nueva actividad basándose en el histórico de gastos reales).

---

## 5. Identificación del Entorno IT en la Asociación

Dentro de la estructura organizativa de la asociación, distinguimos claramente los componentes que configuran un **entorno IT (Information Technology / Tecnología de la Información)** frente a la operación física del centro:

*   **Departamento de Gestión Administrativa y Atención al Socio (Entorno IT):** Corresponde al espacio lógico donde se procesa, almacena y recupera toda la información digital de la entidad. Incluye el software de gestión de socios, la base de datos centralizada de cuotas, el registro informático de contabilidad y los canales de comunicación telemática.
*   **Justificación de su naturaleza IT:** Este entorno se encarga del tratamiento de la información abstracta (datos de identidad, estados financieros, estadísticas de participación y generación de reportes). No opera directamente sobre maquinaria física industrial u operativa (lo que constituiría un entorno OT, como los sistemas de climatización o apertura automática de puertas del hogar del pensionista), sino que se centra en el ciclo de vida del dato administrativo para la toma de decisiones directivas.

---

## 6. Alternativas Valoradas y Justificación de la Decisión

Para solucionar la gestión de datos de la asociación, se evaluaron dos alternativas tecnológicas:
1.  **Alternativa 1 (Hojas de cálculo locales / Excel):** Uso de archivos de hoja de cálculo tradicionales almacenados localmente en un ordenador compartido del centro.
    *   *Desventajas:* Alto riesgo de sobreescritura accidental, falta de control de accesos concurrentes, dificultad para escalar a dispositivos móviles y ausencia de validación estricta de tipos de datos.
2.  **Alternativa 2 (Aplicación modular estructurada con persistencia en base de datos - Elección adoptada):** Desarrollo de una solución software a medida (en la línea de los módulos desarrollados en el TFG para gestión de flotas y registros), estructurada con capas de lógica diferenciadas y almacenamiento persistente estructurado.
    *   *Justificación:* Permite garantizar la integridad referencial, aplicar un control riguroso de errores de entrada, separar claramente la interfaz de usuario de la lógica de negocio y asegurar la escalabilidad futura para integrar notificaciones y estadísticas automatizadas.

---

## 7. Fuentes Bibliográficas y de Información

1.  **Ministerio de Asuntos Económicos y Transformación Digital (España):** *Guía de Digitalización para Pequeñas Empresas y Entidades sin Fines de Lucro*. Disponible en: [https://www.acelerapyme.gob.es](https://www.acelerapyme.gob.es)[span_5](start_span)[span_5](end_span)
2.  **Asociación de la Tercera Edad "Nuestra Señora del Rosario":** *Memoria anual de gestión y actas de organización interna (datos recabados mediante entrevista directa presencial a miembro de la Junta Directiva)*. Septiembre de 2026.
3.  **Tecnologías de la Información (IT) y Operación (OT) en Entornos Productivos:** *Documentación técnica de referencia de la Unidad de Trabajo 1 (UT1), I.E.S. Fray Diego Tadeo González*. Curso 2026/2027[span_6](start_span)[span_6](end_span).

---

## 8. Declaración de Uso de Inteligencia Artificial

De conformidad con los requisitos de la rúbrica[span_7](start_span)[span_7](end_span), se explicita que la inteligencia artificial (Gemini) se ha empleado exclusivamente como **asistente de apoyo en la estructuración de contenidos, revisión de la terminología técnica de entornos IT y redacción formal** de este documento Markdown. El análisis de los procesos reales, la extracción de datos de la entrevista y la validación de la solución técnica adoptada han sido realizados de forma autónoma por el alumno autor, comprendiendo íntegramente el contenido expuesto.
