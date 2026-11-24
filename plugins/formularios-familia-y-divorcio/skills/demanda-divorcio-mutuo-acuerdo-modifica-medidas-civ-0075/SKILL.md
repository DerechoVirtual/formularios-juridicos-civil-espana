---
name: demanda-divorcio-mutuo-acuerdo-modifica-medidas-civ-0075
description: "Demanda de divorcio de mutuo acuerdo que modifica las medidas acordadas en la separación previa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio de mutuo acuerdo que modifica las medidas acordadas en la separación previa

> Formulario **CIV-0075** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio de mutuo acuerdo que modifica las medidas acordadas en la separación previa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio de mutuo acuerdo que modifica las medidas acordadas en la separación previa” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-mutuo-acuerdo-modifica-medidas-civ-0075`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] CALLE (2 veces)
- [ ] LIBRO (2 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] SEDE (2 veces)
- [ ] TOMO (2 veces)
- [ ] COLEGIO
- [ ] DESCRIBIR
- [ ] FECHA
- [ ] Nº DE DOCUMENTO

## Normas que cita el formulario

- art. 777 LEC
- art. 749.1 LEC
- art. 90.3 CC
- art. 81 Código Civil

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

- Junto a «…Antecedentes: Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…ÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA NUM DE [LOCALIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

Antecedentes:

Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]

Separación mutuo acuerdo /

A LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA NUM DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS] y de D./Dª [NOMBRE Y APELLIDOS], mayores de edad, con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta. y en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., respectivamente, cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello o bien: "representación que acredito mediante copia de poder para pleitos que ruego me sea devuelta una vez testimoniada en autos por necesitarla para otros usos", comparezco en este TRIBUNAL con la asistencia del Letrado D. /Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, interpongo DEMANDA DE DIVORCIO DE MUTUO ACUERDO CON SOLICITUD DE MODIFICACIÓN DE MEDIDAS ACORDADAS EN PROCESO PREVIO DE SEPARACIÓN MATRIMONIAL. La presente demanda se basa en los siguientes

HECHOS

Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS] contrajeron entre sí matrimonio civil en la ciudad de [LOCALIDAD], el día [DÍA] de [MES] de [AÑO] Dicho matrimonio consta inscrito en el Registro civil de dicha ciudad, al Tomo [TOMO], libro [LIBRO], página

Se acompaña como DOCUMENTO NUM. certificado literal de matrimonio, expedido por el Encargado del Registro Civil.

De dicho matrimonio nació en [LOCALIDAD] un hijo/a, [NOMBRE Y APELLIDOS] el día [DÍA] de [MES] de [AÑO], cuyo nacimiento consta inscrito en el Registro civil de dicha ciudad al Tomo [TOMO], libro [LIBRO], página

Se acompaña como DOCUMENTO NUM. certificado de nacimiento, expedido por el Encargado del Registro Civil.

Como consecuencia de la crisis de su matrimonio, mis representados formularon demanda de separación de mutuo acuerdo que se siguió ante la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia de [SEDE], plaza n.º esta ciudad, al número [Nº]/[AÑO] de procedimiento, recayendo sentencia de separación por la que además se homologaron las medidas propuestas en el convenio aportado por los demandantes.

En dicho convenio se acordó lo siguiente:

Se acompaña como DOCUMENTO NUM. testimonio de la sentencia y del convenio.

La situación de separación, con cese ininterrumpido de la convivencia, se ha mantenido hasta la actualidad, habiendo decidido mis representados solicitar el divorcio de mutuo acuerdo.

En relación con las medidas definitivas acordadas por los esposos en el convenio regulador de su separación matrimonial y homologadas por el Tribunal en el procedimiento de separación a que se ha hecho referencia en el HECHO TERCERO de esta demanda, mis representados, consideran que deben mantenerse algunas y modificarse otras.

En concreto, deben mantenerse tras el divorcio las medidas relativas a [DESCRIBIR]

Por el contrario, resulta conveniente en interés del hijo menor, tal y como se razonará a continuación, la modificación de las medidas relativas a su guarda y custodia y, en relación con ésta, a la forma de prestarle alimentos cada uno de los progenitores.

Desde que se dictó la sentencia de separación se ha producido una alteración sustancial de las circunstancias atendidas las cuales se acordó en su momento un régimen de guarda y custodia individual a favor de la madre, y la obligación del padre de satisfacer una pensión periódica de alimentos a su hijo/a.

En efecto, el/la menor ha alcanzado una edad y, como consecuencia de ella, un grado de madurez que hace aconsejable atender de modo razonable a sus preferencias, las cuales se decantan por la convivencia con ambos padres en un régimen de paridad.

Por otra parte, el padre del/de la menor, que por razones profesionales residía en una ciudad distinta a la de la madre de su hijo, con la que éste convive en la actualidad, ha trasladado su residencia, de modo definitivo, a la misma localidad y zona. Ambas residencias, dada su ubicación, permitirían al menor asistir con comodidad a su colegio actual y seguir relacionándose con los mismos amigos y compañeros.

Debe subrayarse que el hecho de residir anteriormente en otra ciudad fue la única circunstancia por la que mis representados convinieran en su momento que la madre quedara con la guarda y custodia individual.

La limitada relación que el actual régimen de visitas permiten al menor con su padre, ha generado en aquél, cuyo interés debe prevalecer sobre cualquier otro, un cuadro de ansiedad que se acredita con el informe médico que se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO], emitido por el Dr. que ha atendido al menor desde [FECHA], tal y como resulta del mismo informe. Este estado de frustración y ansiedad repercute negativamente en el desarrollo personal y afectivo del menor.

Estos hechos hacen conveniente la sustitución del régimen de guarda y custodia individual por otro de guarda y custodia compartida, en los términos que se contienen en el convenio regulador de los efectos del divorcio que se acompaña a esta demanda. Así mismo y en relación con lo anterior, procede sustituir el pago de la actual pensión de alimento a cargo del padre, que sólo tenía sentido en relación con el régimen de guarda y custodia individual, por la obligación de cada progenitor de mantener al menor durante el tiempo que conviva con él, además de satisfacer por mitad los gastos extraordinarios, tal y como se detalla, de nuevo, en el convenio regulador que se acompaña a esta demanda.

En cumplimiento de lo previsto en el artículo 777 de la LEC, adjunto aportamos como DOCUMENTO NUM. propuesta de Convenio Regulador de los efectos del divorcio.

A los anteriores hechos les son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

COMPETENCIA.-

Es competente la Sección Civil del Tribunal de Instancia a la que se dirige esta demanda, al amparo del artículo 769.2 de la L.E.C.

PROCEDIMIENTO.-

Deberá seguirse la demanda por los cauces procedimentales previstos para el divorcio de mutuo acuerdo en el artículo 777 de la LEC.

LEGITIMACIÓN.-

Están legitimados para instar la disolución de su matrimonio, por divorcio, ambos cónyuges debiendo se parte el Ministerio Fiscal al haber hijos menores de edad, al amparo del art. 749.1 de la LEC

CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.-

La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional, de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia, por tratarse en sí de un acuerdo consensual y voluntario entre las partes, necesitando únicamente la homologación del mismo por parte del Tribunal, siendo que el convenio regulador (arts. 775.2 y 777.9 LEC y art. 90.3 CCiv) se entiende acreditativo de haber realizado esa actividad negociadora.

ACCIÓN QUE SE EJERCITA

Se ejercita en la presente demanda acción de disolución del matrimonio por divorcio, al amparo de los artículo 81 y 86 del Código Civil, habiendo transcurrido más de tres meses desde la celebración del matrimonio.

Asimismo se solicita la homologación del convenio regulador de las medidas de divorcio que se acompaña.

DERECHO SUSTANTIVO

Arts. 81, 86, 90 y 92.5 del Código civil.

Iura novit curia y demás normas que resulten aplicables.

Por lo expuesto:

SUPLICO AL TRIBUNAL

Que tras admitir este escrito con los documentos que lo acompañan, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta DEMANDA DE DIVORCIO DE MUTUO ACUERDO y, previa ratificación de los demandantes a presencia judicial y visto bueno del Ministerio Fiscal, dicte sentencia por la que, estimando íntegramente la demanda, se decrete la disolución por divorcio del matrimonio contraído por mis representados entre sí, con aprobación de las medidas que se contienen en el convenio regulador, acordándose lo procedente para su constancia en el Registro civil.

En [LOCALIDAD], a [DÍA], de [MES], de [AÑO]

Firma y número del Letrado

Firma del Procurador

========================================================================
