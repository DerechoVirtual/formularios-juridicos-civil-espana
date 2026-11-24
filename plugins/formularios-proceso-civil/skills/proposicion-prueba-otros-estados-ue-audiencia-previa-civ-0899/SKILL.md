---
name: proposicion-prueba-otros-estados-ue-audiencia-previa-civ-0899
description: "Proposición de prueba en otros Estados de la UE en la audiencia previa del juicio ordinario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Proposición de prueba en otros Estados de la UE en la audiencia previa del juicio ordinario

> Formulario **CIV-0899** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito de proposición de prueba en la audiencia previa del proceso ordinario cuando la prueba (documental o testifical) debe practicarse en otro Estado miembro de la Unión Europea, conforme al Reglamento (UE) 2020/1783, solicitando su práctica por el órgano requerido, por obtención directa o por videoconferencia (formulario adaptado a la reforma procesal de la LO 1/2025).

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Proposición de prueba en otros Estados de la UE en la audiencia previa del juicio ordinario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Proposición de prueba en otros Estados de la UE en la audiencia previa del juicio ordinario” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:proposicion-prueba-otros-estados-ue-audiencia-previa-civ-0899`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IDIOMA (4 veces)
- [ ] DOMICILIO (3 veces)
- [ ] LOCALIDAD Y ESTADO MIEMBRO (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] ÓRGANO JURISDICCIONAL REQUERIDO Y DIRECCIÓN (2 veces)
- [ ] AUTORIDAD EXTRANJERA QUE CUSTODIA EL DOCUMENTO
- [ ] LOCALIDAD
- [ ] MEDIOS DE PRUEBA
- [ ] NÚMERO
- [ ] ÓRGANO COMPETENTE Y DIRECCIÓN

## Normas que cita el formulario

- art. 429 LEC

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: el original ilustraba el modelo con un caso concreto (Suecia, Alemania y Países Bajos); los órganos extranjeros, localidades e idiomas pasan a campos. Comprobar en el Atlas Judicial Europeo el órgano competente, los idiomas admitidos y los formularios del Reglamento aplicables en cada Estado miembro.

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

PROPOSICIÓN DE PRUEBA

De conformidad con la previsión contenida en el artículo 429 de la LEC, se proponen los siguientes medios de prueba:

DOCUMENTAL.– Consistente en requerir de [AUTORIDAD EXTRANJERA QUE CUSTODIA EL DOCUMENTO] de [LOCALIDAD Y ESTADO MIEMBRO], a fin de que aporte [DOCUMENTO QUE SE INTERESA: p. ej., certificación del pago durante los últimos [NÚMERO] años del impuesto de bienes inmuebles de naturaleza urbana sitos en ese municipio que haya abonado D. [NOMBRE Y APELLIDOS], con domicilio en [DOMICILIO]].

De cara a la práctica de la prueba se interesa que la misma se lleve a cabo en la forma prevista en el Reglamento (UE) 2020/1783 del Parlamento Europeo y del Consejo, de 25 de noviembre de 2020, relativo a la cooperación entre los órganos jurisdiccionales de los Estados miembros en el ámbito de la obtención de pruebas en materia civil o mercantil, enviando el formulario A previsto en tal Reglamento al órgano señalado en el mismo ([ÓRGANO JURISDICCIONAL REQUERIDO Y DIRECCIÓN]), debidamente traducido al [IDIOMA], comprometiéndose esta parte, una vez el mismo esté preparado, a su traducción.

TESTIFICAL.– Del testigo D. [NOMBRE Y APELLIDOS], con domicilio en [DOMICILIO] de [LOCALIDAD Y ESTADO MIEMBRO].

De cara a la práctica de la prueba se interesa que la misma se lleve a cabo en la forma prevista en el Reglamento (UE) 2020/1783, enviando el formulario A previsto en tal Reglamento al Tribunal [ÓRGANO JURISDICCIONAL REQUERIDO Y DIRECCIÓN], debidamente traducido al [IDIOMA] y concediendo a las partes el plazo de tres días legalmente fijado a los efectos de presentar las preguntas que se proponen formular, acompañadas de la traducción a [IDIOMA].

Respecto de su ejecución, esta parte interesa asimismo que en el formulario de solicitud se indique la intención de estar presente en el momento de la práctica por medio de [MEDIO: p. ej., su representante o letrado / videoconferencia]. Esta parte se ofrece a llevar a cabo la traducción del formulario y preguntas que esta parte presente, así como el traslado de la petición de cooperación al órgano requerido, interesando que las preguntas que se vayan a formular por las demás partes sean presentadas acompañadas de la correspondiente traducción.

TESTIFICAL POR MEDIOS TÉCNICOS: VIDEOCONFERENCIA.– Del testigo D. [NOMBRE Y APELLIDOS], con domicilio en [DOMICILIO] de [LOCALIDAD Y ESTADO MIEMBRO].

De cara a la práctica de la prueba se interesa que la misma se lleve a cabo en la forma prevista en el Reglamento (UE) 2020/1783, aplicando el mecanismo de obtención de pruebas por el órgano jurisdiccional requirente previsto en el artículo 19 del mismo. A tal efecto se solicita que se envíe el formulario I previsto en tal Reglamento al órgano competente ([ÓRGANO COMPETENTE Y DIRECCIÓN]), debidamente traducido al [IDIOMA], comprometiéndose esta parte a verificar tal traducción.

Este mecanismo se estima que es el más idóneo al garantizar la inmediación y la posibilidad de permitir a las partes y al tribunal que conoce de la causa formular directamente las preguntas y aclaraciones que se estimen necesarias al testigo, de forma que se obtenga un conocimiento más completo de las cuestiones suscitadas. Con la finalidad de evitar costes, se interesa que, conforme a la previsión contenida en el artículo 20 del Reglamento, se haga uso del mecanismo de la videoconferencia, de forma que al testigo domiciliado en [LOCALIDAD] se le pueda recibir declaración el mismo día fijado para el juicio en las presentes actuaciones, haciéndose desde la sede de este tribunal, por las partes y el juzgador, las preguntas que se estimen oportunas y se declaren pertinentes, aportando esta parte el intérprete el día del juicio.

OTROS MEDIOS DE PRUEBA.– [OPCIONAL — si ha lugar] En su caso, se propondrían otros medios de prueba: [MEDIOS DE PRUEBA].
