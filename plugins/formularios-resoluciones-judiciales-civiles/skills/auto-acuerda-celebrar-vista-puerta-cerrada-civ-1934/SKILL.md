---
name: auto-acuerda-celebrar-vista-puerta-cerrada-civ-1934
description: "Auto que acuerda celebrar la vista a puerta cerrada. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que acuerda celebrar la vista a puerta cerrada

> Formulario **CIV-1934** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto acordando celebrar a puerta cerrada, con la sola presencia de las partes, sus representantes y defensores, la vista señalada en los autos.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que acuerda celebrar la vista a puerta cerrada» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que acuerda celebrar la vista a puerta cerrada” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-acuerda-celebrar-vista-puerta-cerrada-civ-1934`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (4 veces)
- [ ] LUGAR (3 veces)
- [ ] LOCALIDAD

## Normas que cita el formulario

- art. 138.2 LEC
- art. 138.3 LEC

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Auto acordando celebrar a puerta cerrada, con la sola presencia de las partes, sus representantes y defensores, la vista señalada en los autos.

Notas al pie del formulario original:
(1) Conforme a lo dispuesto en el art. 138.3 LEC, contra la presente resolución no cabe interponer recurso ordinario alguno.

========================================================================


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero el «Texto del formulario» (al final de este fichero) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea del «Texto del formulario» y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Texto del formulario

Lo que sigue, hasta el final de este fichero, es el formulario tal cual: desde su primera línea hasta la firma.

AUTO

En [LUGAR], a [FECHA].

Ilmo. Sr./a Magistrado-Juez D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

ANTECEDENTES DE HECHO

ÚNICO

Con fecha [FECHA] se presentó escrito por el Procurador/a Sr./a [NOMBRE Y APELLIDOS], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], antes de la celebración de la vista señalada para el día de la fecha, interesando se celebraría a puerta cerrada el acto por la índole de los hechos sobre los que depondrían las partes y testigos, acerca de la filiación extramatrimonial de D./Dña. [NOMBRE Y APELLIDOS]

No pudiéndose tramitar audiencia previamente, en el acto de la vista, tras oír a las partes, se resolvió admitiendo la petición deducida, y decretando la celebración a puerta cerrada.

FUNDAMENTOS DE DERECHO

PRIMERO

Preceptúa el art. 138.2 LEC, salvando el principio general de publicidad de actuaciones de prueba, vistas y comparecencias de parte, que tales actuaciones pueden, no obstante, celebrarse a puerta cerrada cuando: a) ello sea necesario para la protección del orden público o de la seguridad nacional en una sociedad democrática; b) los intereses de los menores o la protección de la vida privada de las partes y de otros derechos y libertades lo exijan o, c) en fin, en la medida en la que el tribunal lo considere estrictamente necesario, cuando por la concurrencia de circunstancias especiales la publicidad pudiera perjudicar a los intereses de la justicia.

A tal objeto, antes de acordar la celebración a puerta cerrada de cualquier actuación, el tribunal oirá a las partes que estuvieran presentes en el acto, y resolverá en forma de auto, no recurrible, sin perjuicio de formular protesta y suscitar la cuestión en el recurso procedente contra la sentencia definitiva (art. 138.3 LEC).

SEGUNDO

En consecuencia, planteada la petición, y oídas las partes, en el mismo acto de la vista que venía convocada se ha acordado la celebración de la vista en los presentes autos a puerta cerrada por concurrir el supuesto del mencionado apartado b), sin que se formulara protesta al respecto.

Es así que se pretende la fijación de la filiación extramatrimonial de D./Dña. [NOMBRE Y APELLIDOS], para lo cual hay que elucidar las relaciones íntimas de la madre difunta de aquélla con el demandado D./Dña. [NOMBRE Y APELLIDOS], que es persona con su propia familia, y ocupa el cargo de provicario de la Diócesis de [LOCALIDAD], de modo que, independientemente de lo que se acredite, las versiones que aparezcan en la vista pueden ocasionar un daño irreparable al derecho al honor e intimidad del demandado, y perjudicar la imagen de la institución eclesiástica sin necesidad.

En su virtud,

PARTE DISPOSITIVA

Se acuerda celebrar a puerta cerrada, con la sola presencia de las partes, sus representantes y defensores, la vista señalada en los presentes autos.

Así lo dispongo, mando y firmo.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Juez/a
