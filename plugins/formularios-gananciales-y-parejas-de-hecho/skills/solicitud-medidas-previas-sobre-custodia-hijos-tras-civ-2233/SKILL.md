---
name: solicitud-medidas-previas-sobre-custodia-hijos-tras-civ-2233
description: "Solicitud de medidas previas sobre la custodia de los hijos tras la ruptura de la pareja de hecho. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de medidas previas sobre la custodia de los hijos tras la ruptura de la pareja de hecho

> Formulario **CIV-2233** del plugin **Gananciales, regímenes económicos y parejas de hecho** (`formularios-gananciales-y-parejas-de-hecho`) · Civil › Familia · normativa revisada el 25-11-2026.

## Qué es

Escrito solicitando la guarda y custodia de los hijos menores como medida previa a la presentación de la demanda en este sentido, en el supuesto de ruptura de unión de hecho.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de medidas previas sobre la custodia de los hijos tras la ruptura de la pareja de hecho» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de medidas previas sobre la custodia de los hijos tras la ruptura de la pareja de hecho” para mi caso». También puedes invocarla directamente con `/formularios-gananciales-y-parejas-de-hecho:solicitud-medidas-previas-sobre-custodia-hijos-tras-civ-2233`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-gananciales-y-parejas-de-hecho:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Gananciales, regímenes económicos y parejas de hecho) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] FECHA (2 veces)
- [ ] COMPLETAR
- [ ] LUGAR
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 158 Código Civil
- art. 160 Código Civil

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

Notas al pie del formulario original:
(1) El art. 89.6 LOPJ recoge las competencias civiles de las Secciones de Violencia sobre la Mujer de los Tribunales de Instancia, cuando concurran simultáneamente los requisitos enunciados en el art. 89.7 LOPJ.

En consonancia con estas reformas de índole competencial, se procedió a la modificación del Real Decreto 355/2004, de 5 de marzo, por el que se regula el Registro central para la protección de las víctimas de la violencia doméstica, por Real Decreto 513/2005, de 9 de mayo, de manera que se contempla, de forma expresa, el acceso a la información obrante en el Registro por parte de los órganos judiciales del orden civil que conozcan de procesos de familia.

(2) La regulación específica de las parejas no casadas es hoy una realidad en algunas Comunidades Autónomas:

Andalucía: Ley 5/2002, de 16 de diciembre, de Parejas de Hecho, Decreto 35/2005, de 15 de febrero, por el que se constituye y regula el Registro de Parejas de Hecho

Aragón: Título VI del Libro II del Código del Derecho Foral de Aragón

Asturias: Ley 4/2002, de 23 de mayo, de parejas estables

Cantabria: Ley 1/2005, de 16 de mayo, de Parejas de Hecho de la Comunidad Autónoma de Cantabria

Castilla-La Mancha: Decreto 124/2000, de 11 de julio, registro de parejas de hecho

Castilla y León: Decreto 117/2002, de 24 de octubre, registro de uniones de hecho

Cataluña: Capítulo IV del título III del libro segundo del Código Civil de Cataluña

Extremadura: Ley 5/2003, de 20 de marzo, de parejas de hecho

Galicia: Disp. Adic. 3.ª Ley 2/2006, de 14 de junio, de Derecho Civil de Galicia

Islas Baleares: Ley 18/2001, de 19 de diciembre, de parejas estables

Islas Canarias: Ley 5/2003, de 6 de marzo, de parejas de hecho

Madrid: Ley 11/2001, de 19 de diciembre, de uniones de hecho

Navarra: Ley Foral 6/2000, de 3 de julio, igualdad jurídica de las parejas estables

País Vasco: Ley 2/2003, de 7 de mayo, de parejas de hecho

Valencia: Ley 5/2012, 15 octubre, de la Generalitat, de Uniones de Hecho Formalizadas de la Comunitat Valenciana, Decreto 34/2022 de 1 de abril, del Consell, por el que se regulan la organización y el funcionamiento del Registro de Uniones de Hecho Formalizadas, así como los procedimientos de inscripción, modificación y cancelación de uniones en el mismo.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
