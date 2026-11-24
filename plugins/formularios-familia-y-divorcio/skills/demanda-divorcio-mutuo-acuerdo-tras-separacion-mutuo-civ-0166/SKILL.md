---
name: demanda-divorcio-mutuo-acuerdo-tras-separacion-mutuo-civ-0166
description: "Demanda de divorcio de mutuo acuerdo tras una separación de mutuo acuerdo previa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio de mutuo acuerdo tras una separación de mutuo acuerdo previa

> Formulario **CIV-0166** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Antecedentes Al Tribunal Procurador, representación Asistencia letrada y acción que se ejercita: divorcio de mutuo acuerdo HECHOS FUNDAMENTOS DE DERECHO Suplico Firmas

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio de mutuo acuerdo tras una separación de mutuo acuerdo previa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio de mutuo acuerdo tras una separación de mutuo acuerdo previa” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-mutuo-acuerdo-tras-separacion-mutuo-civ-0166`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] AÑO (5 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] LIBRO (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] SEDE (3 veces)
- [ ] TOMO (3 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] Nº (2 veces)
- [ ] PÁGINA (2 veces)
- [ ] COLEGIO
- [ ] LUGAR
- [ ] NÚMERO

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…AMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «….3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…petente la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia de»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO]

Separación mutuo acuerdo /

A LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], y de D./Dª [NOMBRE Y APELLIDOS], cuya representación acredito mediante escritura de poder que acompaño, comparezco en este TRIBUNAL y como mejor proceda en Derecho DIGO:

Que mediante el presente escrito, y con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], formulo demanda de divorcio de mutuo acuerdo en base a los siguientes:

HECHOS

Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS] contrajeron entre sí matrimonio civil en la ciudad de [LOCALIDAD], el día [DÍA] de [MES] de [AÑO] Dicho matrimonio consta inscrito en el Registro civil de dicha ciudad, al Tomo [TOMO], libro [LIBRO], página

Adjunto aportamos como DOCUMENTO NÚM. UNO certificado literal de matrimonio.

De dicho matrimonio nacieron en [LOCALIDAD] dos hijos, [NOMBRE DEL MENOR] el día [DÍA] de [MES] de [AÑO], y [NOMBRE DEL MENOR] el día [DÍA] de [MES] de [AÑO] Sus nacimientos constan inscritos en el Registro civil de dicha ciudad al Tomo [TOMO], libro [LIBRO], página [PÁGINA]; y al Tomo [TOMO], libro [LIBRO], página [PÁGINA], respectivamente.

Adjunto aportamos como DOCUMENTOS NÚMS. DOS y TRES sus respectivos certificados de nacimiento.

Habiendo devenido imposible, por razones que no vienen al caso, la convivencia matrimonial, mis mandantes formularon demanda de separación de mutuo acuerdo que se siguió ante la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia de [SEDE], plaza n.º esta ciudad, al número [Nº]/[AÑO] de procedimiento, recayendo sentencia de separación por la que además se homologaron las medidas propuestas en el convenio aportado por los demandantes.

Adjunto acompañamos como DOCUMENTO NÚM. CUATRO testimonio de la sentencia y del convenio.

En cumplimiento de lo previsto en el artículo 777 de la LEC, adjunto aportamos como DOCUMENTO NÚM. CINCO propuesta de Convenio Regulador de los efectos del divorcio.

A los anteriores hechos les son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

Competencia

Es competente la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia de la ciudad de [LOCALIDAD], al que por turno le corresponda, por hallarse el domicilio del matrimonio en el ámbito de su circunscripción, al amparo del artículo 769.2 de la L.E.C.

Procedimiento

Deberá seguirse la demanda por los cauces procedimentales previstos para el divorcio de mutuo acuerdo en el artículo 777 de la LEC.

Legitimación

Están legitimados para instar la disolución de su matrimonio, por divorcio, ambos cónyuges debiendo se parte el Ministerio Fiscal al haber hijos menores de edad, al amparo del art. 749.1 de la LEC.

Cumplimiento de los requisitos de procedibilidad

La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional, de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia, por tratarse en sí de un acuerdo consensual y voluntario entre las partes, necesitando únicamente la homologación del mismo por parte del Tribunal, siendo que el convenio regulador (arts. 775.2 y 777.9 LEC y art. 90.3 CCiv) se entiende acreditativo de haber realizado esa actividad negociadora.

Acción que se ejercita

Ejercitamos en la presente demanda acción de disolución del matrimonio por divorcio, al amparo de los artículos 81 y 86 del Código Civil, habiendo transcurrido más de tres meses desde la celebración del matrimonio.

Asimismo solicitamos la homologación del convenio regulador de las medidas de divorcio que se acompaña.

Por lo expuesto:

SUPLICAMOS AL TRIBUNAL tenga por presentado este escrito, me tenga por parte en la representación que, otorgada por Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS] asumo, entendiéndose conmigo las sucesivas actuaciones, por formulada demanda de divorcio de mutuo acuerdo, y previa ratificación de los demandantes a presencia judicial y visto bueno del Ministerio fiscal, se dicte sentencia por la que se decrete la disolución por divorcio del matrimonio contraído por mis mandantes entre sí, con aprobación de las medidas que se contienen en el convenio regulador, acordándose lo procedente para su constancia en el Registro civil.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número Letrado	Firma Procurador

========================================================================
