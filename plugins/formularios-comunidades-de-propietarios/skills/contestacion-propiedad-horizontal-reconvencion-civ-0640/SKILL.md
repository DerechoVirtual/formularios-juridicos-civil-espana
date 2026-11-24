---
name: contestacion-propiedad-horizontal-reconvencion-civ-0640
description: "Contestación en propiedad horizontal con reconvención de reclamación de cantidades al propietario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación en propiedad horizontal con reconvención de reclamación de cantidades al propietario

> Formulario **CIV-0640** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación en propiedad horizontal con reconvención de reclamación de cantidades al propietario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación en propiedad horizontal con reconvención de reclamación de cantidades al propietario” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:contestacion-propiedad-horizontal-reconvencion-civ-0640`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NÚMERO (5 veces)
- [ ] FECHA (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] AÑO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] MES
- [ ] Nº
- [ ] SEDE
- [ ] TIPO DE PROCEDIMIENTO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 249.1.8.º LEC
- art. 394 LEC
- art. 406 LEC
- art. 21 LPH
- art. 9.1.e LPH
- art. 1100 CC
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…RO]/[AÑO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

Juicio [TIPO DE PROCEDIMIENTO] n.º [NÚMERO]/[AÑO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en representación de D. [NOMBRE Y APELLIDOS], que obra en su condición de Presidente de la Comunidad de Propietarios del edificio de la [DIRECCIÓN], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], comparezco en el presente procedimiento en el que se emplazó a mi representada el pasado [FECHA] y por medio de la presente paso a contestar a la demanda interpuesta contra mi principal y formulo reconvención, fundando la contestación en base a los siguientes:

HECHOS

ÚNICO.-En la acción ejercitada se impugnan los acuerdos adoptados en la Junta de la Comunidad que es mi principal al entender que la citación para la misma se realizó en forma incorrecta ante el desconocimiento que dice haber tenido de ella el actor. No obstante lo anterior en fecha [FECHA], se envió al demandante por medio de correo certificado con acuse de recibo la pertinente citación al domicilio que había proporcionado a la Comunidad, carta que resultó devuelta al ser desconocido en el lugar y sin que hubiere comunicado el Sr. ningún cambio de este elemento a la Comunidad. A tal efecto se adjunta como documento n.º [NÚMERO] la pertinente carta con la nota del empleado de correos en la que hace constar la circunstancia de ser el destinatario desconocido, habiéndose colocado asimismo los avisos de celebración de la Junta en lugares públicos dentro del edificio así como en todos los buzones de los vecinos. Ello conlleva la que se estima plena legalidad de la Junta que en su momento se celebró y cuya acta se adjunta como documento n.º [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

PRIMERO.- Procedimiento.-Se acepta la tramitación de la causa por los trámites del juicio ordinario con fundamento en el art. 249.1.8.º LEC y asumiendo las alegaciones en este sentido vertidas en el escrito de demanda.

SEGUNDO.- Fondo de la reclamación.-Se estima improcedente el acceder a la acción de impugnación solicitada ya que la citación a la Junta que se impugna se verificó en el domicilio que el Sr. había dado a la comunidad lo que implica la idoneidad de la misma con fundamento en los arts. 16.2 y 9.1.h) LPH ya que se intentó la citación sin efecto y se colocó el anuncio de la Junta en los lugares de paso general de todos los vecinos.

TERCERO.- En materia de costas el art. 394 LEC.

En base a lo anterior,

SUPLICO AL TRIBUNAL, que tenga por presentado este escrito junto con sus copias, teniendo a esta parte por personada en las presentes actuaciones entendiéndose conmigo las siguientes diligencias y por contestada a la demanda interpuesta contra mi principal y tras la pertinente tramitación se sirva dictar sentencia por la que se desestime la demanda presentada contra mi principal con imposición de costas al demandante.

RECONVENCIÓN

HECHOS

ÚNICO.-Que D. es titular de la vivienda sita en [LOCALIDAD], según resulta de la certificación del Registro de la Propiedad [LOCALIDAD] que se adjunta como documento n.º [NÚMERO], estando pendiente de pago la suma de [IMPORTE] por contribución a los gastos generales y al fondo de reserva tal y como resulta de la certificación del administrador de la Comunidad que se adjunta como documento n.º [NÚMERO], habiéndose acordado en la Junta de [FECHA] cuya acta se une como documento n.º [NÚMERO] el reclamar tales cuotas pendientes de pago.

FUNDAMENTOS DE DERECHO

PRIMERO.- Competencia.-La tiene el Tribunal al que me dirijo al ser el que está conociendo del asunto en el que el litigio se ha suscitado, siendo el procedimiento el adecuado no solamente por la operatividad de los arts. 406 y 407 LEC, sino por no ser obligado el acudir a la vía del proceso monitorio del art. 21 LPH.

SEGUNDO.- Fondo de la reclamación.-Lo es el art. 9.1.e) y f) LPH que fijan la obligación de los diversos propietarios de contribuir al pago de los gastos generales del edificio y a la dotación del fondo de reserva.

TERCERO.- En cuanto a los intereses se solicitan los mismos desde la presente reconvención al cumplirse con ella los requisitos de la mora con fundamento en el art. 1100 CC.

CUARTO.- En materia de costas el art. 394 LEC.

En base a lo anterior,

SUPLICO AL TRIBUNAL, se tenga por presentado este escrito y documentos al mismo adjuntos y por formulada demanda reconvencional contra el demandante [ÓRGANO], se sirva admitirla y tras la adecuada tramitación se dicte sentencia por la que se condene al reconvenido a abonar a mi principal la cantidad de [IMPORTE] Euros intereses desde la presente reconvención y costas.

OTROSÍ PRIMERO DIGO que fijo la cuantía de la reconvención en la cantidad de [IMPORTE] euros, por aplicación de lo dispuesto en el artículo 251.1 de la LEC.

[NOMBRE Y APELLIDOS], a [DÍA] de [MES] de [AÑO]

Firma Abogado	Firma Procurador

========================================================================
