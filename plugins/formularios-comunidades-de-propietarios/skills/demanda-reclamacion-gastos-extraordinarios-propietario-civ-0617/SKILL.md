---
name: demanda-reclamacion-gastos-extraordinarios-propietario-civ-0617
description: "Demanda de reclamación de gastos extraordinarios a un propietario de una comunidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reclamación de gastos extraordinarios a un propietario de una comunidad

> Formulario **CIV-0617** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reclamación de gastos extraordinarios a un propietario de una comunidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reclamación de gastos extraordinarios a un propietario de una comunidad” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:demanda-reclamacion-gastos-extraordinarios-propietario-civ-0617`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] AÑO
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] FECHA
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO
- [ ] PORCENTAJE

## Normas que cita el formulario

- art. 9 LPH
- art. 10 LPH
- art. 52.1.8.º LEC
- art. 249.2 LEC
- art. 5 Ley Orgánica 1/2025
- art. 9.1.e LPH
- art. 17.2 LPH
- art. 1100 CC
- art. 394 LEC
- art. 251.1 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en representación de D. [NOMBRE Y APELLIDOS], que obra en su condición de Presidente de la Comunidad de Propietarios del edificio de la [DIRECCIÓN], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], formulo demanda de juicio ordinario [Nº DE PROCEDIMIENTO], en reclamación de [IMPORTE] euros contra D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD] () en base a los siguientes

HECHOS

El día [FECHA] se celebró Junta de la Comunidad que represento en la que el punto del orden del día número [NÚMERO] la realización de obras consistentes en instalación de ascensor, plataforma elevadora y silla de personas con discapacidad y reparación de cubierta, con un presupuesto de [IMPORTE] euros, y aprobándose que se abonaría por una derrama extraordinaria de cada uno de los propietarios cuyo pago se realizaría en el mes de

Dicha propuesta fue aprobada por mayoría de los asistentes que, a su vez, representan la mayoría de cuotas de participación.

A efectos acreditativos del contenido del acuerdo y del resultado de la votación se adjunta como documento n.º [NÚMERO] copia del acta de tal Junta.

Llegado el vencimiento de la derrama, el demandado D. [NOMBRE Y APELLIDOS], titular de la vivienda [DESCRIPCIÓN DEL BIEN], al que corresponde un porcentaje de participación del [PORCENTAJE] %, no satisfizo el importe de la cuota de [IMPORTE] euros (Se adjunta como documento n.º [NÚMERO] nota registral acreditativa de la titularidad de la vivienda y de la cuota de participación).

Por medio de la presente demanda se insta, al amparo de lo dispuesto en los artículos 9, 10 y 17 de la LPH, el pago de la derrama por gastos extraordinarios aprobada en la antedicha Junta de Propietarios, por darse las mayorías exigidas para este tipo de acuerdos, que mejoran la accesibilidad del edificio, y que por ello son necesarias y obligatorias. El referido acuerdo comunitario, adoptado asimismo en cumplimiento de la obligación establecida en el artículo 10 de la LPH, redactado por Ley 8/2013, comporta para el propietario demandado la obligación de contribuir, con arreglo a la cuota de participación asignada a su vivienda en el título constitutivo del régimen de propiedad horizontal, a los gastos de dichas obras de instalación de ascensor, plataforma elevadora y silla de personas con discapacidad así como las necesarias para la subsanación de los defectos ruinógenos afectantes a la cubierta, que ascienden a la cantidad de [IMPORTE] euros.

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

Competencia

Corresponde a los Tribunales de [LOCALIDAD] al ser el lugar en el que se encuentra la finca (art. 52.1.8.º LEC).

Legitimación

Le corresponde a esta parte la legitimación activa en su condición de Comunidad de Propietario del edificio en régimen de propiedad horizontal y la pasiva al propietario demandado, conforme a lo que disponen los artículos 9,10 y 17 de la LPH.

Procedimiento

Debe seguirse el procedimiento según la cuantía, conforme a lo previsto en el artículo 249.2 de la LEC

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Fondo de la reclamación

Lo es el art. 9.1.e) y f) LPH que fijan la obligación de los diversos propietarios de contribuir al pago de los gastos generales del edificio y a la dotación del fondo de reserva; los artículos 10.1 y 10.2 de la LPH, redactados por Ley 8/2013, que prescriben la obligación de los propietarios de costear Los trabajos y las obras que resulten necesarias para el adecuado mantenimiento y cumplimiento del deber de conservación del inmueble y de sus servicios e instalaciones comunes, así como las obras y actuaciones que resulten necesarias para garantizar los ajustes razonables en materia de accesibilidad universal; y el artículo 17.2 de la LPH.

En cuanto a los intereses se solicitan los mismos desde la presente demanda al cumplirse con ella los requisitos de la mora con fundamento en los artículos 1100 y 1108 del CC.

En materia de costas, el artículo 394 LEC, debiéndose imponer las costas a los demandados.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentada la presente demanda con los documentos a ella adjuntos y sus copias, en la representación que ostento, y se tenga por formulada demanda de juicio ordinario (o verbal) en reclamación de la cantidad de [IMPORTE] euros, contra la demandada cuyas demás circunstancias personales constan en el encabezamiento de este escrito y tras los trámites correspondientes, dicte sentencia por la que se condene a la demandada a abonar a mi principal la cantidad de [IMPORTE] euros, más los intereses correspondientes, y al pago de las costas del proceso.

OTROSÍ PRIMERO DIGO que fijo la cuantía de la demanda en la cantidad reclamada de [IMPORTE] euros, por aplicación de lo dispuesto en el artículo 251.1 de la LEC.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

El Abogado	El Procurador

========================================================================
