---
name: escrito-ejecutante-pidiendo-mejorar-embargo-pensiones-civ-1471
description: "Escrito del ejecutante pidiendo mejorar el embargo por pensiones alimenticias o compensatorias. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del ejecutante pidiendo mejorar el embargo por pensiones alimenticias o compensatorias

> Formulario **CIV-1471** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del ejecutante pidiendo mejorar el embargo por pensiones alimenticias o compensatorias» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del ejecutante pidiendo mejorar el embargo por pensiones alimenticias o compensatorias” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-ejecutante-pidiendo-mejorar-embargo-pensiones-civ-1471`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] AÑO (3 veces)
- [ ] SEDE (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] Nº DE REGISTRO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] COLEGIO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO]

Procedimiento: /

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

Dª/D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], cuyas demás circunstancias constan en este Tribunal, representación que tengo acreditada en autos, bajo la dirección técnica de D./Dª [NOMBRE Y APELLIDOS], Letrado del Ilustre Colegio de Abogados de [COLEGIO], comparezco ante el Tribunal y como mejor proceda en Derecho DIGO

Que por el presente escrito, siguiendo instrucciones de mi mandante, formulo SOLICITUD DE MEJORA DE EMBARGO para hacer efectivas las cantidades debidas e impagadas en concepto de pensiones alimenticias (o pensión compensatoria, o ambas), conforme a los siguientes

HECHOS

El día [DÍA] de [MES] de [AÑO] este Tribunal despachó ejecución sobre los bienes propiedad del ejecutado para cubrir un importe adeudado de [IMPORTE] euros de principal y [IMPORTE] euros presupuestados para intereses y costas. En la misma resolución se decretó el embargo del saldo en las cuentas corrientes de las que pudiera ser titular el ejecutado en diversas entidades bancarias, así como de los inmuebles que constaran inscritos a su nombre en los Registros de la Propiedad que se señalaba.

En relación con el embargo de saldo en cuentas corrientes, tras remitir los correspondientes oficios a las entidades bancarias, sólo se ha hallado una (o las que corresponda) a nombre del ejecutado en la entidad [DENOMINACIÓN SOCIAL] con un saldo de [IMPORTE] euros ( €) (o con saldos de [IMPORTE] euros [ €] y [IMPORTE] euros [ €], respectivamente), que ha sido retenido a disposición de este Tribunal, pero que resulta claramente insuficiente para cubrir la cantidad debida.

Han resultado, por otra parte, infructuosas las gestiones realizadas en el Registro de la Propiedad de [LOCALIDAD] (de [Nº DE REGISTRO] y de [Nº DE REGISTRO], en su caso), en que no consta ningún inmueble inscrito a nombre del ejecutado.

[ELEGIR UNA OPCIÓN: Conocimiento de nuevos bienes obtenidos por el ejecutado / Conocimiento de nuevos bienes obtenidos por el ejecutado: empleo / Conocimiento de nuevos bienes obtenidos por el ejecutado: sentencia favorable / — y además elegir: Procedencia de la mejora de embargo / Retención salarial / Libramiento de exhorto]

Se acompañan los siguientes documentos para acreditar los hechos expuestos:

Resultan aplicables a los hechos expuestos, los siguientes

FUNDAMENTOS DE DERECHO

El artículo 612 de la Ley de Enjuiciamiento Civil establece, en su número 1 que "el ejecutante podrá pedir la mejora o la modificación del embargo o de las medidas de garantía adoptadas cuando un cambio de las circunstancias permita dudar de la suficiencia de los bienes embargados en relación con la exacción de la responsabilidad del ejecutado".

[ELEGIR UNA OPCIÓN: Procedencia de la mejora de embargo / Retención salarial / Libramiento de exhorto]

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito junto con sus documentos y copias, lo admita y, estimando lo que en él se solicita, dicte providencia en la que acuerde la mejora de embargo de bienes del deudor D./Dª [NOMBRE Y APELLIDOS] en cuantía suficiente para cubrir la cantidad de [IMPORTE] euros ( €); y expida oficio a la empresa [DENOMINACIÓN SOCIAL], para la retención mensual en lo sucesivo de la parte que corresponda de los ingresos del ejecutado (o libre exhorto a la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO], a fin de que, en relación al procedimiento que en la actualidad se sigue a instancia del ejecutado contra D./Dª [NOMBRE Y APELLIDOS], autos nº [Nº DE PROCEDIMIENTO]/[AÑO], en su día retenga y ponga a disposición de este Tribunal la cantidad de [IMPORTE] euros ( €).

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
