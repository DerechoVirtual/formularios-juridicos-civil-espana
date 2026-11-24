---
name: impugnacion-reparto-demanda-solicitud-nulidad-remision-civ-1016
description: "Impugnación del reparto de la demanda con solicitud de nulidad y remisión al órgano competente. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Impugnación del reparto de la demanda con solicitud de nulidad y remisión al órgano competente

> Formulario **CIV-1016** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito de parte impugnando el reparto de la demanda y solicitando se decrete la nulidad de lo actuado y remita la demanda al órgano competente.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Impugnación del reparto de la demanda con solicitud de nulidad y remisión al órgano competente» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Impugnación del reparto de la demanda con solicitud de nulidad y remisión al órgano competente” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:impugnacion-reparto-demanda-solicitud-nulidad-remision-civ-1016`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] SEDE (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] LUGAR

## Normas que cita el formulario

- art. 68.3 LEC

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

- Junto a «…repartida a la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

AL SERVICIO COMÚN DE REGISTRO Y REPARTO DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], según acredito mediante la escritura de poder otorgada al efecto, que tengo aceptada y acompaño para su unión a los autos por copia testimoniada bastante, con devolución del original por necesitarlo a otros usos; dirigidos mis poderdantes por la Letrado en ejercicio D./Dña. [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO], del Iltre. Colegio de [LOCALIDAD], con despacho abierto en [LOCALIDAD], calle [CALLE]; ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que mis patrocinados han formulado demanda de juicio ordinario que, turnada de reparto, ha correspondido a la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO], que ha incoado autos n.º [NÚMERO]/[AÑO], lo que vengo a impugnar en base a las siguientes

ALEGACIONES

PRIMERA

En la demanda presentada se ejercita frente a la mercantil [DENOMINACIÓN SOCIAL], acción de impugnación del acuerdo adoptado por el Consejo de Administración de fecha [FECHA], por antiestatutario.

Se aporta la copia de la dicha demanda con el sello de registro de presentación de fecha [FECHA], ante la secretaría de ese Servicio Común de Registro y Reparto del Tribunal de Instancia.

SEGUNDA

Ha tenido noticia esta parte que con fecha [FECHA], se formuló demanda por D./Dña. [NOMBRE Y APELLIDOS], en que se pedía la declaración de nulidad del mismo indicado acuerdo del órgano de administración de [DENOMINACIÓN SOCIAL], la cual fue repartida a la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] esta población, que tiene formados autos de juicio ordinario n.º [NÚMERO] /

TERCERA

Conforme al art. 76.2, párrafo 2.º LEC, la demanda de mi parte debió repartirse a la Sección Civil del Tribunal de Instancia n.º 2, por lo que se ha infringido norma imperativa de reparto que debe corregirse por la prevención del art. 68.3 LEC.

CUARTA

El presente escrito se presenta ante el Juez decano a fin de que corrija el reparto, puesto que, con arreglo a lo dispuesto en el art. 68.3 LEC, mi mandante está legitimado para proponer esta cuestión de competencia, puesto que es el demandante, y se produce en el momento inmediato a la presentación y del conocimiento del pleito al que debe acumularse.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, se sirva admitirlo, teniéndome por comparecido en la representación que ostento, a los solos efectos de plantear la presente impugnación de la decisión de reparto, y se resuelva repartir la demanda a la Sección Civil del Tribunal de Instancia n.ºde esta población, ordenando que se comunique a la Sección Civil del Tribunal de Instancia n.º [Nº], a fin de que decrete la nulidad de lo actuado y remita la demanda al órgano competente en concreto.

Es justo en [LUGAR], a [FECHA].

Firma del Abogado	Firma del Procurador/a

========================================================================
