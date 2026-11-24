---
name: propuesta-modificacion-convenio-regulador-divorcio-no-civ-0356
description: "Propuesta de modificación del convenio regulador de divorcio no aprobado en la sentencia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Propuesta de modificación del convenio regulador de divorcio no aprobado en la sentencia

> Formulario **CIV-0356** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Propuesta de modificación del convenio regulador de divorcio no aprobado en la sentencia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Propuesta de modificación del convenio regulador de divorcio no aprobado en la sentencia” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:propuesta-modificacion-convenio-regulador-divorcio-no-civ-0356`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] FECHA (2 veces)
- [ ] LUGAR

## Normas que cita el formulario

- art. 777 LEC

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

- Ninguna.

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

Escrito aportando propuesta modificativa de convenio regulador de divorcio en relación al extremo que no fue aprobado por la sentencia de divorcio.

PROPUESTA DE CONVENIO REGULADOR que para su aprobación judicial formulan los cónyuges D./D.ª [NOMBRE Y APELLIDOS] y D./D.ª [NOMBRE Y APELLIDOS] respecto de la propuesta de convenio regulador ya acompañada con el escrito de solicitud de transformación del procedimiento al cauce del art. 777 LEC de fecha [FECHA], a fin de que el mismo se entienda modificado, en el sentido ordenado por la sentencia recaída, como a continuación se indica:

II.- Cuidado de los hijos, comunicación y estancias del padre con los hijos menores del matrimonio:
1.- Los cónyuges se comprometen a comunicarse con sus hijos comunes como hasta ahora han venido haciendo, siempre considerando el interés de los menores, y evitando cualquier actitud que interfiera el cariño y respeto de los hijos hacia ambos padres, atenidos a las siguientes reglas:
1.1. El progenitor que se encuentre con los hijos permitirá y facilitará en todo momento la comunicación con el otro, siempre que ésta no se produzca de forma caprichosa, injustificada o fuera de las horas normales para ello.
1.2. Cualquiera de los padres puede trasladarse con los menores de un lugar conocido a otro desconocido, pero deberá entonces inexcusablemente comunicarlo al otro y le dará también el nuevo teléfono, si lo hubiere.
1.3. En caso de enfermedad de los hijos, cualquiera de los progenitores deberá comunicárselo al otro, permitiendo visitarlos en su domicilio y, en todo caso, deberá considerar la opinión del otro en lo relativo a médicos, tratamientos, hospitales, etc
2.- Sólo para la hipótesis de que llegue a faltar acuerdo entre partes, se establece el siguiente programa:

Semanal: El padre podrá tener consigo a los hijos un fin de semana de cada dos, de sábado a las diez horas hasta el domingo a las veinte horas, recogiéndolos y devolviéndolos en el domicilio de la madre.

Podrá igualmente tener consigo a los hijos una tarde entre semana, a convenir entre los miércoles y jueves, recogiéndolos en el colegio, y devolviéndolos en el domicilio de la madre.

Vacacional: Por Navidad, los hijos pasarán una mitad de sus vacaciones escolares con el padre y la otra mitad con la madre, a elección de la madre cual mitad los años pares, y del padre los impares. En Semana Santa, los hijos pasarán los años pares con la madre y los impares con el padre. Durante el período de vacaciones de verano escolares, correspondiente a los meses de julio y agosto, pasarán los hijos un mes con el padre y otro con la madre, de modo que ésta elegirá los años pares y el padre los impares.

Y para que así conste, otorgan la presente propuesta modificativa, cuya conformidad firman, después de leerla por sí mismos cada uno de los cónyuges, y que tiene efectos desde la firma,

En [LUGAR], a [FECHA].

Firmado	Firmado
D./D.ª [NOMBRE Y APELLIDOS]	D./D.ª [NOMBRE Y APELLIDOS]

========================================================================
