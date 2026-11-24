---
name: recurso-revision-contra-decreto-laj-da-terminado-civ-1303
description: "Recurso de revisión contra el decreto del LAJ que da por terminado el desahucio por enervación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de revisión contra el decreto del LAJ que da por terminado el desahucio por enervación

> Formulario **CIV-1303** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de revisión contra el decreto del LAJ que da por terminado el desahucio por enervación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de revisión contra el decreto del LAJ que da por terminado el desahucio por enervación” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-revision-contra-decreto-laj-da-terminado-civ-1303`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 454.b LEC
- art. 22.4 LEC

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

- Junto a «… [NÚMERO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

Proceso número [NÚMERO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], según tengo acreditado en los autos de proceso civil [Nº DE PROCEDIMIENTO] arriba referenciados, ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que habiendo sido notificado a esta representación el decreto de fecha [FECHA], dictado por el Letrado de la Administración de Justicia del órgano al que me dirijo, por el que se declara enervada la acción de desahucio por falta de pago de la renta arrendaticia en relación al inmueble [DESCRIPCIÓN DEL BIEN] ejercitada por esta representación mediante el presente escrito, al amparo del art. 454.bis LEC, interpongo recurso directo de revisión de la mencionada resolución citando como infringidos el mismo artículo 22.4 LEC, en base a los siguientes ALEGACIONES:

PRIMERO.- El decreto recurrido de fecha [FECHA] dispone la finalización del proceso de desahucio por enervación de la acción con infracción de lo dispuesto en el artículo 22.4 de la LEC, por cuanto que en este caso mi mandante se opuso expresamente a la enervación instada por el demandado, tan pronto como se le dio traslado del escrito, por lo que el cauce procesal que debió seguirse es el prevenido en el párrafo primero del referido artículo 22.4 de la LEC que preceptúa la convocatoria de vista ante el tribunal en el caso de que el demandante se opusiera a la enervación por no darse los requisitos establecidos legalmente, lo cual es además concorde con lo expresado en la demanda rectora de este proceso, donde esta parte había manifestado expresamente la improcedencia de la enervación por no darse las circunstancias establecidas en el artículo 22.4 de la LEC, tal como expondremos ampliamente a continuación.

En cualquier caso, la infracción procesal denunciada debe determinar la revocación del decreto dictado por el Letrado de la Administración de Justicia en cuanto que infringe el artículo 22.4 de la LEC, excediendo a las facultades legalmente conferidas al Letrado de la Administración de Justicia para la finalización del proceso, en tanto que la controversia sobre la enervación debe resolverla necesariamente el tribunal y no el Letrado de la Administración de Justicia.

SEGUNDO.- El decreto recurrido infringe asimismo lo dispuesto en el artículo 22.4, párrafo segundo, de la LEC en cuanto a los requisitos para que tenga lugar la enervación, por cuanto que el Letrado de la Administración de Justicia acepta la enervación con motivo de que en el anterior juicio de desahucio número [NÚMERO] seguido entre las partes, el demandado pagó la renta antes de ser citado para juicio, por lo que considera que no existe enervación en el proceso anterior, entendiendo que no se da la excepción recogida en el artículo 22.4, párrafo segundo, de la LEC. Sin embargo, tal interpretación infringe la interpretación sostenida por los Tribunales a partir de la Sentencia del Pleno del Tribunal Supremo de 20 de enero de 2009 en la cual que se indica que la mora del deudor comienza con la interposición de la demanda contra él y no con su emplazamiento, lo que es indudable que el pago verificado tras la presentación de la demanda ya es enervación.

En este caso, el demandado pagó en el anterior juicio de desahucio número [NÚMERO] tras la presentación de la demanda, por lo que es claro que se había producido una enervación anterior que impide que ahora pueda decretarse nuevamente la enervación, como expresamente establece el artículo 22.4, párrafo segundo, de la LEC, el cual resulta infringido por el decreto impugnado.

De acuerdo a ello, se solicita que se revoque la resolución, acordando la continuación del proceso, no dando lugar a la enervación de la acción.

En su virtud,

SUPLICO AL TRIBUNAL que teniendo por presentado este escrito, con justificante de traslado, se sirva admitirlo, tener por interpuesto recurso directo de revisión contra el decreto dictado por el Letrado de la Administración de Justicia de ese órgano de fecha [FECHA] y, tras los trámites legales, se dicte por el Tribunal auto por el que se revoque y deje sin efecto el Decreto impugnado, ordenando en su lugar la continuación del juicio por sus trámites.

OTROSÍ DIGO que, de conformidad con lo dispuesto en los apartados 4 y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 25 euros.

Por lo que SUPLICO AL TRIBUNAL que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso

En

========================================================================
