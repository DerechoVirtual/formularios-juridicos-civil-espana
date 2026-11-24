---
name: demanda-juicio-ordinario-impago-generos-suministrados-civ-0809
description: "Demanda de juicio ordinario por impago de géneros suministrados, con intereses desde la compraventa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario por impago de géneros suministrados, con intereses desde la compraventa

> Formulario **CIV-0809** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario por impago de géneros suministrados, con intereses desde la compraventa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario por impago de géneros suministrados, con intereses desde la compraventa” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-impago-generos-suministrados-civ-0809`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DOMICILIO
- [ ] DÍA
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A

## Normas que cita el formulario

- art. 51 LEC
- art. 249.2 LEC
- art. 5 Ley Orgánica 1/2025
- art. 63 CC
- art. 394 LEC
- art. 7.2 Ley 10/2012

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

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A] según se acredita por certificación del registro electrónico de apoderamientos judiciales que acompaño o mediante designación apud acta ante el Letrado/a de la Administración de Justicia de [LOCALIDAD], bajo la dirección letrada de D/Dª [NOMBRE Y APELLIDOS], Abogado/a del Iltre. Colegio de [LOCALIDAD], ante el Tribunal comparezco y como mejor en derecho proceda formulo demanda de juicio ordinario en ejercicio de acción de reclamación de cantidad frente a la mercantil [DENOMINACIÓN SOCIAL] SA domiciliada en [DOMICILIO] en base a los siguientes hechos y fundamentos de derecho:

HECHOS

ÚNICO.-Que mi mandante verificó unos suministros de [DESCRIPCIÓN DEL BIEN] a la mercantil [DENOMINACIÓN SOCIAL] siendo los mismos entregados a satisfacción de la demandada según resulta de los albaranes aportados como documentos n.º [NÚMERO] expidiéndose las pertinentes facturas por importes de [IMPORTE] Euros que se adjuntan como documentos n.º [NÚMERO] sin que las mismas hayan sido abonadas.

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

PRIMERO.- Competencia.-Corresponde a los Tribunales de [LOCALIDAD] al ser el lugar en el que tiene su domicilio la mercantil demandada (art. 51 LEC).

SEGUNDO.- Legitimación.-Le corresponde a esta parte ante su condición de suministradora del producto cuyo importe se reclama (arts. 325 y ss. CCom).

TERCERO.- Procedimiento.-Es el juicio ordinario con fundamento en el art. 249.2 LEC dado el importe reclamado de [IMPORTE] Euros que excede de los 15.000 Euros a partir de los que se deben seguir las reclamaciones por las normas del juicio ordinario.

CUARTO.- Cumplimiento de los requisitos de procedibilidad.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

QUINTO.- Fondo de la reclamación.-Al ser calificable la relación existente entre las partes de contrato de suministro, figura que las SSTS 30 noviembre 1984 y 8 julio 1988 entre otras han definido como afín a la compraventa y por el que una de las partes se obliga a cambio de un precio a realizar en favor de otra, prestaciones periódicas o continuas, cuya función es la satisfacción de necesidades continuas para atender al interés duradero del acreedor. A esta figura le son de aplicación subsidiaria los preceptos referentes a la compraventa mercantil (arts. 325 y ss. CCom) reclamándose en esta causa el precio así como los intereses a contar desde el día siguiente al señalado para el vencimiento de las facturas que se adjuntan (art. 63 CCom).

SEXTO.- En materia de costas el art. 394 LEC señala que las de primera instancia se imponen a la parte que vea en primera instancia rechazadas sus pretensiones

En base a lo anterior,

SUPLICO AL TRIBUNAL: Que tenga por presentada la presente demanda con los documentos a ella adjuntos y por parte en la representación que ostento y tras la pertinente tramitación se dicte por ese Tribunal sentencia por la que se condene a la mercantil [DENOMINACIÓN SOCIAL] a abonar a mi mandante la cantidad de [IMPORTE] Euros más los intereses desde la fecha de vencimiento de las facturas adjuntas a esta demanda, todo ello con imposición de costas a los demandados.

OTROSÍ DIGO: Se fija la cuantía del presente procedimiento en [IMPORTE] Euros, valor de la cosa reclamada.

En base a lo anterior

SUPLICO AL TRIBUNAL se tenga por efectuada la anterior manifestación a los efectos pertinentes.

OTROSÍ DIGO.-Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 300 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En base a lo anterior

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

a [DÍA] de [MES] de [AÑO]

Firma Abogado	Firma Procurador

========================================================================
