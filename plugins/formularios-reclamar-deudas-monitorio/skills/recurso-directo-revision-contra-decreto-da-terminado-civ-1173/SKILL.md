---
name: recurso-directo-revision-contra-decreto-da-terminado-civ-1173
description: "Recurso directo de revisión contra el decreto que da por terminado el proceso monitorio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso directo de revisión contra el decreto que da por terminado el proceso monitorio

> Formulario **CIV-1173** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso directo de revisión contra el decreto que da por terminado el proceso monitorio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso directo de revisión contra el decreto que da por terminado el proceso monitorio” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:recurso-directo-revision-contra-decreto-da-terminado-civ-1173`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 813 LEC
- art. 85.1 LOPJ
- art. 815 LEC
- art. 161.3 LEC
- art. 161 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], parte demandada en el procedimiento monitorio seguido ante ese órgano con el número [NÚMERO] a instancias de [NOMBRE DE LA PARTE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], y bajo la dirección letrada de D. [NOMBRE Y APELLIDOS], Abogado del Iltre. Colegio de Abogados de [COLEGIO], ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que habiendo sido notificado a esta representación el decreto de fecha [FECHA], dictado por el Letrado de la Administración de Justicia del órgano al que me dirijo, por el que se da por finalizado el procedimiento monitorio arriba referenciado al no haber comparecido mi representado, y entendiendo que dicha resolución no es ajustada a derecho, mediante el presente escrito, al amparo del art. 454 bis y 816.1 de la LEC, interpongo recurso directo de revisión de la mencionada resolución citando como infringido los artículos 813 y 815 en relación con el artículo 161, todos ellos de la Ley de Enjuiciamiento Civil, y el artículo 24 de la CE, al provocar una absoluta indefensión de esta parte, en base a los siguientes motivos:

PRIMERO.- En el decreto recurrido se acuerda dar por terminado el procedimiento con base al requerimiento de pago acordado por resolución del Letrado de la Administración de Justicia de fecha [FECHA], donde se acordaba practicar dicho requerimiento en el domicilio facilitado por el demandante en la petición inicial, sito en [LOCALIDAD] calle

Con ello se infringe el art. 813 de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ, que establecen la competencia exclusiva del Tribunal de Instancia del domicilio del deudor, el cual se encuentra en la localidad de [LOCALIDAD], calle [CALLE], tal como se constata claramente de los propios documentos aportados por el demandante, puesto que dicho domicilio consta en todos los albaranes, facturas y demás documentación aportada con la petición inicial.

Con independencia de la mala fe con que ha actuado el demandante, al facilitar un domicilio en el que no reside mi representado, por ser una segunda residencia de verano, lo cierto es que en la resolución de admisión debió controlarse de oficio la competencia, por ser cuestión de orden público, cuya ausencia queda más patente todavía cuando fue el propio demandante quien interesó que se notificara el decreto ahora recurrido en el domicilio real de mi representado, lo que pone de manifiesto que se infringió el referido art. 813 de la LEC.

A efectos acreditativos, aportamos como documento número 1 certificación de empadronamiento en el domicilio indicado.

Por tanto, se solicita que se revoque la resolución, por cuanto se infringe el art. 813 de la LEC invocado, a la vez que se ocasiona a esta parte una situación de evidente indefensión, con vulneración de su derecho fundamental del art. 24 de la CE.

SEGUNDO.- El decreto recurrido infringe lo dispuesto en el art. 815 de la LEC en relación con el art. 161 de la misma Ley procesal, puesto que el requerimiento no se ha practicado en la forma prevenida en el referido precepto, lo cual ha determinado que el procedimiento se haya seguido a espaldas de mi representado, dejándolo en una situación de absoluta indefensión, al no tener oportunidad de conocer que se seguía el presente procedimiento monitorio.

Al respecto, la práctica del requerimiento infringe lo dispuesto en el art. 161.3 de la LEC, por cuanto se entregó la comunicación al conserje del bloque de apartamentos donde mi representado reside en el periodo estival, no dándose el supuesto de hecho que habilitaba a tal entrega, puesto que el citado domicilio no es el lugar donde está empadronado mi mandante, según hemos acreditado en el anterior expositivo, ni se dan los demás supuestos que permiten la comunicación por entrega a un tercero según el citado apartado 3 del art. 161 de la LEC.

En consecuencia, debe revocarse el decreto también por este motivo, teniendo a esta parte por opuesta al requerimiento de pago y debiendo seguir el procedimiento la tramitación ordenada legalmente.

En su virtud,

SUPLICO AL TRIBUNAL que teniendo por presentado este escrito, con justificante de traslado, se sirva admitirlo, tener por interpuesto recurso directo de revisión contra el decreto dictado por el Letrado de la Administración de Justicia de ese órgano de fecha [FECHA] y, tras los trámites legales, se dicte por el Tribunal auto por el que se revoque y deje sin efecto el Decreto impugnado, acordando tener por opuesta a esta parte al requerimiento de pago formulado y dando al procedimiento la tramitación legamente prevenida.

OTROSÍ DIGO que, de conformidad con lo dispuesto en los apartados 4 y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 25 euros.

Por lo que SUPLICO AL TRIBUNAL que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso

En

========================================================================
