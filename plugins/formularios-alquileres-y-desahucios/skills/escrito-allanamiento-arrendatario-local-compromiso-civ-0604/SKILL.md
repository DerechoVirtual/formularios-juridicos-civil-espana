---
name: escrito-allanamiento-arrendatario-local-compromiso-civ-0604
description: "Escrito de allanamiento del arrendatario de un local con compromiso de desalojo voluntario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de allanamiento del arrendatario de un local con compromiso de desalojo voluntario

> Formulario **CIV-0604** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Escrito de la parte demandada en juicio de desahucio de finca urbana por falta de pago del arrendamiento de un local, por el que asume el compromiso de desalojar voluntariamente el local en el plazo de un mes desde la notificación de la demanda con la citación para la vista, a cambio de la condonación de la mitad de las cantidades adeudadas que justifican el desahucio y las costas del juicio (allanamiento).

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de allanamiento del arrendatario de un local con compromiso de desalojo voluntario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de allanamiento del arrendatario de un local con compromiso de desalojo voluntario” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:escrito-allanamiento-arrendatario-local-compromiso-civ-0604`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] LUGAR (2 veces)
- [ ] LOCALIDAD
- [ ] SEDE

## Normas que cita el formulario

- art. 437.3 LEC
- art. 438.5 LEC
- art. 21.1 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que he recibido resolución que admite la demanda de recuperación del local que ocupo en arrendamiento del Sr./a. [NOMBRE Y APELLIDOS], y además de requerirme para que desaloje el inmueble en el plazo de diez días y de citarme para el acto de la eventual vista para el día [FECHA], me advierte de que el demandante calcula las rentas y cantidades asimiladas debidas, las cuales fundamentan dicha recuperación, en la cantidad de [IMPORTE] euros, y de conformidad con el art. 437.3 LEC, anuncia el compromiso de condonada la mitad de dicha cifra total, así como las costas del juicio, bajo condición de que esta parte desaloje en el plazo de un mes desde la notificación de la demanda.

Advertida conforme al art. 438.5 II LEC por el Tribunal que acoger dicha oferta de la parte actora significará allanamiento pleno, en el plazo conferido de diez días desde el requerimiento, MANIFIESTO QUE ASUMO EL COMPROMISO DE DESALOJO VOLUNTARIO EN PLAZO DE QUINCE DÍAS DESDE HABÉRSEME NOTIFICADO LA DEMANDA CON LA CITACIÓN PARA LA EVENTUAL VISTA, A CAMBIO DE LA CONDONACIÓN DE LA MITAD DE CANTIDADES ADEUDADAS QUE JUSTIFICAN EL DESAHUCIO ( [IMPORTE] EUROS) Y LAS COSTAS DEL PRESENTE PROCESO.

Si no cumpliere el comparecido allanado se llevará a término el lanzamiento dentro de los quince días siguientes, sin trámite previo alguno, puesto que con arreglo al art. 447.1 párrafo 2.º LEC, en previsión de que no se verifique por el arrendatario el desalojo voluntario en el plazo señalado, se habrá de fijar con carácter subsidiario día y hora en que tendrá lugar, en su caso, el lanzamiento directo del demandado, que se llevará a término sin necesidad de ulteriores trámites en un plazo no superior en los quince días desde la finalización de dicho periodo voluntario.

En su virtud,

AL TRIBUNAL SUPLICO

que, teniendo por causadas las anteriores manifestaciones a los oportunos efectos, según lo prevenido en el art. 21.1 LEC, se proceda al dictado de sentencia de allanamiento, bajo compromiso de desalojo voluntario antes del [FECHA] (quince días desde la notificación de la demanda y citación), condonándose la cantidad de [IMPORTE] euros de la deuda con el actor D./Dña. [NOMBRE Y APELLIDOS], y sin imposición de costas, como es Justo en [LUGAR], a [FECHA].

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
