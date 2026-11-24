---
name: acta-inicial-contrato-mediacion-familiar-segun-civ-0015
description: "Acta inicial o contrato de mediación familiar según la normativa aragonesa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta inicial o contrato de mediación familiar según la normativa aragonesa

> Formulario **CIV-0015** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta inicial o contrato de mediación familiar según la normativa aragonesa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta inicial o contrato de mediación familiar según la normativa aragonesa” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:acta-inicial-contrato-mediacion-familiar-segun-civ-0015`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] AÑO (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] DATOS DEL MEDIADOR (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] Nº (2 veces)
- [ ] LUGAR
- [ ] PERIODICIDAD
- [ ] PLAZO

## Normas que cita el formulario

- art. 18 Ley 9/2011
- art. 7 Ley 9/2011

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].l año [AÑO]

REUNIDOS:

DON/DOÑA [NOMBRE Y APELLIDOS] y DON/DOÑA [NOMBRE Y APELLIDOS], como sujetos mediados.

Y DON/DOÑA [NOMBRE Y APELLIDOS], como profesional mediador [DATOS DEL MEDIADOR], [DATOS DEL MEDIADOR]

Todos ellos intervienen en su propio nombre y derecho y se reconocen la capacidad legal suficiente para celebrar el presente CONTRATO DE MEDIACIÓN y a tal efecto,

EXPONEN

ÚNICO.- DON/DOÑA [NOMBRE Y APELLIDOS] y DON/DOÑA [NOMBRE Y APELLIDOS], son cónyuges y se encuentran inmersos en una crisis matrimonial. Para intentar aproximar posturas y llegar, en su caso, a acuerdos relativos a la regulación de los efectos de esta crisis, han decidido, tras una sesión informativa celebrada en fecha [DÍA] de [MES] de [AÑO], someterse a un proceso de mediación, orientado como persona mediadora, por DON/DOÑA [NOMBRE Y APELLIDOS], que acepta ejercer tal función, conforme a las siguientes

ESTIPULACIONES

VOLUNTARIEDAD Y EVENTUAL DESISTIMIENTO.- Las partes mediadas declaran que inician y participan voluntariamente en el presente procedimiento de mediación, pudiendo desistir del mismo en cualquier momento, comunicándolo a la persona mediadora.

OBJETO DE LA MEDIACIÓN.- Constituye el objeto del presente procedimiento de mediación la aproximación de posturas y adopción, en su caso, de acuerdos relativos a los efectos de la crisis matrimonial de las partes mediadas.

OBLIGACIONES DE LAS PARTES MEDIADAS.- Las partes mediadas, se obligan a cumplir el procedimiento de mediación familiar en todos sus términos, a actuar de buena fe, de forma respetuosa y con predisposición a la búsqueda de acuerdos, a asistir personalmente a las sesiones del proceso de mediación, y a cumplir con las obligaciones establecidas en la Ley 9/2011, de 24 de marzo, de mediación familiar de Aragón.

OBLIGACIONES DE LA PERSONA MEDIADORA.- La persona mediadora, en el ejercicio de su actividad de mediación familiar, se obliga a facilitar la comunicación y la consecución de acuerdos entre las partes mediadas, a mantener la neutralidad e imparcialidad, así como la confidencialidad sobre la información obtenida durante el procedimiento de mediación, excepto cuando comporte amenaza para la vida o integridad física o psíquica de una persona y a cumplir cualquier otra obligación que le imponga la Ley 9/2011, de 24 de marzo, de mediación familiar de Aragón.

DURACIÓN.- El procedimiento de mediación se desarrollará a través de un máximo de [PLAZO] sesiones, que se celebrarán con la siguiente periodicidad: [PERIODICIDAD], sin que puedan exceder de [Nº] días desde la reunión inicial, sin perjuicio de la posibilidad de prórroga en los términos del art. 18 de la Ley 9/2011, de 24 de marzo, de mediación familiar de Aragón. Las sesiones se celebrarán en:

COSTE DE LA MEDIACIÓN:

Redacción del contrato de mediación: [IMPORTE] euros.

Coste por sesión: [IMPORTE] euros.

Otros gastos [IMPORTE]: euros.

Cualquier otro gasto no incluido en los anteriores, p.ej., honorarios, en su caso, de otras personas que asistan como consultores a las sesiones de mediación, deberán ser acordados por las partes.

Las partes deben satisfacer por partes iguales los costes de la mediación, con independencia de que se alcance o no un acuerdo como consecuencia de ésta.

Si la persona mediadora lo considera necesario, podrá solicitar una provisión de fondos. Si las partes o alguna de ellas no realizaran en plazo la provisión de fondos solicitada, el mediador podrá dar por concluida la mediación. No obstante, si alguna de las partes no hubiere realizado su provisión, el mediador, antes de acordar la conclusión, lo comunicará a la otra parte, por si tuviere interés en suplirla dentro del plazo que hubiera sido fijado, sin perjuicio de su derecho de reintegro frente a la contraparte.

PRINCIPIOS RECTORES.- El presente procedimiento se regirá por los principios regulados en el art. 7 de la Ley 9/2011, de 24 de marzo, de mediación familiar de Aragón.

Así lo declaran y asumen voluntariamente las partes mediadas y para que conste, se extiende y firma esta acta con un ejemplar para cada una de ellas, a un solo efecto, en el lugar y fecha indicados en el encabezamiento.

Firma de las personas mediadas Firma y nº [Nº] de Registro de la persona/s

========================================================================
