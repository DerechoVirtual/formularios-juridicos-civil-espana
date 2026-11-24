---
name: contestacion-reconvencion-pide-alimentos-hijo-mayor-civ-0030
description: "Contestación a la reconvención que pide alimentos para un hijo mayor de edad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la reconvención que pide alimentos para un hijo mayor de edad

> Formulario **CIV-0030** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la reconvención que pide alimentos para un hijo mayor de edad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la reconvención que pide alimentos para un hijo mayor de edad” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-reconvencion-pide-alimentos-hijo-mayor-civ-0030`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº (4 veces)
- [ ] AÑO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] CURSO
- [ ] DÍA
- [ ] ESTUDIOS CURSADOS
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] PROFESIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 750 LEC
- art. 770 LEC
- art. 93 Código Civil
- art. 152.5 Código Civil
- art. 142 Código Civil
- art. 394 LEC

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

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «….3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., cuya representación tengo acreditada en los presentes autos, comparezco en este TRIBUNAL con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, formulo dentro del plazo legal CONTESTACIÓN A LA DEMANDA RECONVENCIONAL, instada por D./Dª [NOMBRE Y APELLIDOS] en autos de juicio núm. [Nº DE PROCEDIMIENTO]/[AÑO], con base en los siguientes

HECHOS:

PRIMERO.- Si bien el hijo común de las partes, de [Nº] años de edad y soltero, para el que se solicita la pensión de alimentos en la demanda reconvencional se encuentra matriculado en la Facultad de [ESTUDIOS CURSADOS], lo cierto es que lleva ya más de [Nº] años cursando tales estudios con escaso aprovechamiento. En esos [Nº] años no ha pasado del [CURSO] curso. La única causa de ello es su falta de diligencia y aplicación al estudio, pues le resulta más cómodo vivir a expensas de sus padres. Aunque su madre está dispuesta a tolerar esta situación, no ocurre lo mismo con mi representado, que se niega a favorecer esta situación pasiva de lucha por la vida de su hijo y además, no tiene obligación de alimentarlo en tal situación.

Como justificación de los anteriores hechos, se acompañan como DOCUMENTOS Nº [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO], los siguientes:

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

Competencia, procedimiento y legitimación

Conformes con la competencia objetiva y territorial del Tribunal, la legitimación de las partes, y el procedimiento.

Representación y defensa

Mi mandante comparece representado/a y defendido/a, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en el artículo 750 LEC, en relación con el artículo 770 LEC en la nueva redacción dada por la Ley 8/2021 de 2 de junio.

Derecho sustantivo

El art. 93-II del Código Civil, se remite en relación con la fijación de alimentos en favor de hijos mayores de edad en los procesos de crisis matrimonial, a los arts. 142 y ss. del mismo Cuerpo Legal, que regulan la llamada obligación legal de alimentos entre parientes.

El art. 152.5 del Código Civil dispone que cesará la obligación de dar alimentos "cuando el alimentista sea descendiente del obligado a dar alimentos, y la necesidad de aquél provenga de mala conducta o falta de aplicación al trabajo, mientras subsista esta causa".

Y el art. 142 del Código Civil se refiere a la obligación de sufragar los gastos de instrucción y educación de los hijos mayores de edad cunado no hayan terminado su formación, pero sólo por "causa que no les sea imputable".

Por otra parte, son numerosas las sentencias del Tribunal Supremo que considera que la necesidad es imputable al propio hijo mayor de edad cuando proviene de su falta de interés en conseguir medios de vida, por resultar más cómodo para él seguir viviendo a expensas de sus padres. En este sentido, entre muchas otras, puede citarse la STS 184/2001 de 1 de marzo de 2001.

Costas

Las costas deben imponerse al demandante conforme al art. 394 de la Ley de Enjuiciamiento Civil.

Iura novit curia y las demás normas que resulten procedentes

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

Que tras admitir este escrito con los documentos que lo acompañan, tenga por interpuesta en tiempo y forma CONTESTACIÓN A LA DEMANDA RECONVENCIONAL instada de contrario y, previos los trámites procesales oportunos, dicte en su día sentencia por la que se desestimen las pretensiones de la reconvención, esto es, la solicitud de la parte reconviniente de fijación de una pensión de alimentos a cargo de mi representado y en favor del hijo mayor de edad de las partes. Así mismo, se solicita la imposición de las costas a la parte reconviniente, conforme a lo dispuesto en el art. 394 LEC.

En [LOCALIDAD], a [DÍA], de [MES], de [AÑO]

Firma y número del Letrado	Firma del Procurador

========================================================================
