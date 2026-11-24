---
name: demanda-ejecutiva-acuerdo-mediacion-sobre-alimentos-civ-1469
description: "Demanda ejecutiva de un acuerdo de mediación sobre alimentos del hijo mayor de edad (Ley 5 de 2012). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva de un acuerdo de mediación sobre alimentos del hijo mayor de edad (Ley 5 de 2012)

> Formulario **CIV-1469** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva de un acuerdo de mediación sobre alimentos del hijo mayor de edad (Ley 5 de 2012)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva de un acuerdo de mediación sobre alimentos del hijo mayor de edad (Ley 5 de 2012)” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-acuerdo-mediacion-sobre-alimentos-civ-1469`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (10 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] MES (4 veces)
- [ ] AÑO (3 veces)
- [ ] COLEGIO (3 veces)
- [ ] DÍA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] CALLE
- [ ] DATOS DE LA ESCRITURA
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROTOCOLO
- [ ] NÚMERO

## Normas que cita el formulario

- art. 575 LEC
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…CIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]

Procedimiento: /

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], representación que acreditaré mediante comparecencia apud acta cuando sea requerido para ello, bajo la dirección técnica de D./Dª [NOMBRE Y APELLIDOS], Letrado del Ilustre Colegio de Abogados de [COLEGIO], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito formulo DEMANDA EJECUTIVA contra D./Dª [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., en calidad de deudor, según el título ejecutivo que luego se dirá, en reclamación de las responsabilidades que se concretan en el suplico de esta demanda ejecutiva,

La demanda se interpone con base en los siguientes

HECHOS

TÍTULO EJECUTIVO: El título en que se funda la presente demanda es el ACUERDO OBTENIDO EN PROCESO DE MEDIACIÓN FAMILIAR FORMALIZADO EN ESCRITURA PÚBLICA de fecha [DÍA] de [MES] de [AÑO], otorgada ante D./Dª [NOMBRE Y APELLIDOS], Notario del Ilustre Colegio de [COLEGIO], número de protocolo

En virtud de dicho acuerdo, el/la demandado/a viene obligado a satisfacer a mi representado/a, su hijo/a mayor de edad, la suma de [IMPORTE] EUROS CON [IMPORTE] CÉNTIMOS DE EURO MENSUALES ( €) en concepto de pensión de alimentos, que debe ser ingresada en la cuenta corriente señalada al efecto.

Se acompaña primera copia de la escritura pública que se ejecuta como DOCUMENTO NÚMERO [Nº DE DOCUMENTO]

SUMA ADEUDADA: El/La demandado/a ha dejado de satisfacer las siguientes mensualidades: resultando infructuosas las gestiones extrajudiciales llevadas a cabo por mi representado con el fin de obtener el pago.

De acuerdo con ello, se reclaman en la presente demanda, las siguientes cantidades:

1) La suma de [IMPORTE] euros ( €) de principal, correspondiente a la pensión de alimentos de los meses de [MES]

2) Además, en el acuerdo mediado que se ejecuta se establece que la cantidad mensual a abonar por el ejecutado deberá actualizarse anualmente de acuerdo con la variación experimentada por el IPC. Al haberse cumplido una anualidad de vigencia del acuerdo mediado, sin que el ejecutado haya procedido a actualizar las cantidades debidas, se reclama dicha actualización, de conformidad con el siguiente desglose: En consecuencia, el demandado debe abonar la cantidad de [IMPORTE] euros ( €) en concepto de diferencia entre las cantidades satisfechas los meses en que ha procedido al pago y las debidas en virtud de la actualización de la pensión de acuerdo con el IPC.

Se acompañan como DOCUMENTOS NÚMEROS [Nº] los documentos acreditativos del incremento del IPC durante los ejercicios indicados.

3) Se reclaman, igualmente, otros [IMPORTE] euros ( €) correspondientes al interés legal incrementado en dos puntos, de acuerdo con lo dispuesto en el artículo 576.1 y 3 de la Ley de Enjuiciamiento Civil, de acuerdo con el siguiente desglose:

4) Además se reclaman por la presente demanda, las cantidades correspondientes a las mensualidades que vayan venciendo durante la substanciación de este procedimiento y no satisfaga el ejecutado, conforme a lo dispuesto en el artículo 578 de la Ley de Enjuiciamiento Civil.

5) Finalmente, se reclaman otros [IMPORTE] euros ( para intereses presupuestados y costas de la ejecución, que, sin perjuicio de ulterior liquidación, se establecen prudencialmente en la suma indicada, que no excede del 30% del principal, límite señalado por el artículo 575 de la LEC.

Los Hechos expuestos se basan en los siguientes

FUNDAMENTOS DE DERECHO

Es competente el Tribunal al que me dirijo, por ser el del lugar en que se firmó el acuerdo de mediación (se entiende por tal, el acuerdo alcanzado por las partes tras el proceso de mediación, elevado a escritura pública), a tenor de lo dispuesto en el artículo 545.2 de la Ley de Enjuiciamiento Civil, en relación con el art. 85.1º LOPJ.

La acción ejercitada mediante la presente demanda es la acción ejecutiva contra deudor obligado a la prestación que se reclama, fundada en un acuerdo de mediación elevado a escritura pública [DATOS DE LA ESCRITURA] de acuerdo con la Ley 5/2012, de 6 de julio, de mediación en asuntos civiles y mercantiles, y de conformidad con el artículo 517 de la Ley de Enjuiciamiento Civil.

Los artículos 575, 576 y 578 de la Ley de Enjuiciamiento Civil invocados en el cuerpo del presente escrito.

"Iura novit curia", y cuantos otros resulten de aplicación.

En virtud de lo expuesto:

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito, con los documentos y copias que se acompañan, lo admita, tenga al procurador que suscribe por comparecido y parte en la representación que acredita, y por interpuesta DEMANDA EJECUTIVA contra D./Dª [NOMBRE Y APELLIDOS], con el fin de hacer efectivos los acuerdos alcanzados en proceso de mediación formalizados en escritura pública de fecha [DÍA] de [MES] de [AÑO], otorgada ante D./Dª [NOMBRE Y APELLIDOS], Notario del Ilustre Colegio de [COLEGIO], número de protocolo [Nº DE PROTOCOLO], y dicte auto por el que despache ejecución contra los bienes del demandado en cantidad suficiente para cubrir la suma de [IMPORTE] euros ( €) de principal, más otros [IMPORTE] euros ( €) en concepto de diferencia entre las cantidades satisfechas los meses en que ha procedido al pago de la pensión de alimentos y las debidas en virtud de la actualización de dicha pensión de acuerdo con el IPC, más otros [IMPORTE] euros ( €) en concepto de intereses vencidos, y [IMPORTE] euros ( €) para intereses presupuestados y costas de la ejecución; y sin necesidad de requerimiento previo se embarguen bienes del ejecutado en cantidad suficiente para cubrir las cantidades reclamadas y, previos los trámites legales oportunos, se proceda a realizar tales bienes para satisfacer con su producto las cantidades adeudadas por mi representado y reclamadas por el presente escrito.

PRIMER OTROSÍ DIGO: Se señalan como bienes del ejecutado susceptibles de embargo de los que tiene conocimiento mi representado, a los efectos de dar cumplimiento a la exigencia contenida en el artículo 549 de la Ley de Enjuiciamiento Civil, los siguientes

SEGUNDO OTROSÍ DIGO: Dado que el valor de los bienes antes señalados no parece suficiente para hacer frente a la totalidad de lo adeudado, solicito, con amparo en el art. 590 de la Ley de Enjuiciamiento Civil, que se remita oficio a las siguientes entidades bancarias, con las que, según le consta a mi representado por haber tenido conocimiento de ello en su ámbito familiar, el ejecutado ha venido manteniendo relaciones, con el fin de que comuniquen la posible existencia de [DESCRIPCIÓN DEL BIEN], de titularidad del ejecutado, ordenándoles, en su caso, el embargo del saldo obrante en las mismas, que será puesto a disposición de este Tribunal con el fin de satisfacer las cantidades debidas a mi representado:

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
