---
name: escrito-pidiendo-declaracion-jurada-como-diligencia-civ-1263
description: "Escrito pidiendo declaración jurada como diligencia preliminar y ofreciendo caución. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito pidiendo declaración jurada como diligencia preliminar y ofreciendo caución

> Formulario **CIV-1263** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito solicitando la práctica, como diligencia preliminar, de la declaración jurada de una persona acerca de su legitimación pasiva para un juicio ulterior en el que se le reclamará una cantidad. El solicitante ofrece caución.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito pidiendo declaración jurada como diligencia preliminar y ofreciendo caución» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito pidiendo declaración jurada como diligencia preliminar y ofreciendo caución” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:escrito-pidiendo-declaracion-jurada-como-diligencia-civ-1263`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] IMPORTE (2 veces)
- [ ] IMPORTE EN CIFRA (2 veces)
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] SEDE

## Normas que cita el formulario

- art. 85.1 LOPJ

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

Notas al pie del formulario original:
(1) * La solicitud de diligencias preliminares debe contener:

— Expresión de los fundamentos de las diligencias preliminares que se solicitan.

— Referencia circunstanciada del asunto objeto del juicio ulterior que se pretenda plantear.

* Junto con ella el solicitante debe ofrecer caución:

— Para responder de:

• Los gastos que se ocasionen a las personas que tengan que intervenir en las diligencias.

• Los daños y perjuicios que se les pueda ocasionar a dichas personas.

— Puede prestarse:

• En dinero efectivo.

• Mediante aval solidario de duración indefinida y pagadero a primer requerimiento emitido por entidad de crédito o sociedad de garantía recíproca.

• Por cualquier otro medio que garantice la inmediata disponibilidad de la cantidad de que se trate.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], según acredito con la copia de poder que se acompaña; ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que mediante el presente escrito solicito DILIGENCIAS PRELIMINARES al amparo del art. 256.1.1º de la L.E.C., pidiendo declaración jurada de D./Dña. [NOMBRE Y APELLIDOS] con domicilio en [LOCALIDAD], al proponerse mi mandante demandar en juicio ordinario al mismo; ello en base a los siguientes:

HECHOS

PRIMERO.- Mi representado era acreedor de D./Dña. [NOMBRE Y APELLIDOS], hoy fallecido, por la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) por suministro de mercancías.

SEGUNDO.- A la muerte de D./Dña. [NOMBRE Y APELLIDOS], éste no había satisfecho la deuda, que sigue pendiente.

TERCERO.- Al frente del negocio que ostentaba el fallecido D./Dña. [NOMBRE Y APELLIDOS] y para el que se suministraron por mi mandante los géneros que en su momento se acreditarán, se encuentra ahora su hijo D./Dña. [NOMBRE Y APELLIDOS] Por ello interesa al derecho de esta parte, a fin de reclamar su crédito en juicio ordinario ulterior, que se tome declaración jurada a D./Dña. [NOMBRE Y APELLIDOS] en relación a su legitimación pasiva en esta reclamación, para conocer si ha de ser soportada sólo por él o hay más herederos de D./Dña. [NOMBRE Y APELLIDOS]

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.-

Conforme al artículo 257.1 de la Ley de Enjuiciamiento Civil en relación con el art. 85.1º LOPJ, corresponde resolver esta petición al Tribunal de Instancia del domicilio de D./Dña. [NOMBRE Y APELLIDOS]

II.- PROCEDIMIENTO.-

Los artículos 258 y siguientes de la Ley de Enjuiciamiento Civil regulan la tramitación de las diligencias preliminares.

En su virtud,

SUPLICO AL TRIBUNAL:

Que teniendo por presentado este escrito, se sirva admitirlo y tenerme por comparecido y parte en la representación que ostento para que, previos los trámites legales oportunos, se acuerde la práctica como diligencia preliminar de juicio, de la declaración de D./Dña. [NOMBRE Y APELLIDOS], bajo juramento o promesa de decir verdad, acerca de su legitimación pasiva para un juicio ulterior en el que se le reclamará la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €).

Es de Justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO: Para responder de los gastos, así como de los daños y perjuicios que estas diligencias puedan ocasionar al requerido, ofrezco caución suficiente mediante dinero en efectivo (o aval bancario).

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por hecha la anterior manifestación y la acepte fijando la caución que deba prestar mi representado.

Es Justicia que reitero en el lugar y fecha "ut supra" indicados.

Firma del Abogado/a	Firma del Procurador/a
