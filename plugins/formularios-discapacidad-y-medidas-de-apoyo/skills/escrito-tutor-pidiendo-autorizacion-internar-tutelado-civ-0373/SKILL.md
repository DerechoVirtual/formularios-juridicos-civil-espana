---
name: escrito-tutor-pidiendo-autorizacion-internar-tutelado-civ-0373
description: "Escrito del tutor pidiendo autorización para internar al tutelado en centro de educación especial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del tutor pidiendo autorización para internar al tutelado en centro de educación especial

> Formulario **CIV-0373** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del tutor pidiendo autorización para internar al tutelado en centro de educación especial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del tutor pidiendo autorización para internar al tutelado en centro de educación especial” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:escrito-tutor-pidiendo-autorizacion-internar-tutelado-civ-0373`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] Nº (4 veces)
- [ ] AÑO (3 veces)
- [ ] CALLE (3 veces)
- [ ] MES (3 veces)
- [ ] DÍA (2 veces)
- [ ] NIF (2 veces)
- [ ] NOMBRE DEL CENTRO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] COLEGIO
- [ ] DIAGNÓSTICO
- [ ] LUGAR
- [ ] MEDIO DE ACREDITACIÓN
- [ ] NOMBRE DEL MENOR
- [ ] Nº DE DOCUMENTO
- [ ] OTROS DATOS
- [ ] PLAZO

## Normas que cita el formulario

- art. 271.1 Código Civil
- art. 6 LEC

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

Notas al pie del formulario original:
(1) El art. 763 LEC regula el internamiento no voluntario por “transtorno psíquico”. Resulta aplicable también, en este caso, a las personas sometidas a patria potestad o a tutela. Sin embargo la doctrina discute si este precepto opera también respecto del internamiento involuntario que se efectúa por motivos de “educación o formación especial”, a los que alude el art. 271.1º CC, junto a los motivos de salud mental. En concreto no hay acuerdo entre los autores acerca de si la solicitud de internamiento del pupilo por razones de educación o formación especial debe seguir el procedimiento del art. 763 LEC o el procedimiento de la jurisdicción voluntaria. Este formulario responde a la primera tesis.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de D./Dª [NOMBRE Y APELLIDOS], como tutor/a de D./Dª [NOMBRE Y APELLIDOS], con DNI/NIF [NIF] y domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], cuya representación acreditará cuando sea requerido para ello mediante comparecencia apud acta/ [MEDIO DE ACREDITACIÓN], bajo la dirección técnica de D./Dª [NOMBRE Y APELLIDOS], Letrado del Ilustre Colegio de [COLEGIO], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito, en la representación que ostento y siguiendo instrucciones expresas de mi representado/a, formulo SOLICITUD DE INTERNAMIENTO NO VOLUNTARIO EN UN CENTRO DE EDUCACIÓN ESPECIAL del pupilo de mi mandante D./Dª [NOMBRE Y APELLIDOS], con DNI/NIF [NIF] y domicilio en [LOCALIDAD], calle, nº [Nº], conforme con lo dispuesto en el artículo 271.1º del Código Civil y en el art. 763 de la Ley de Enjuiciamiento Civil, con base en los siguientes

HECHOS

PRIMERO.- Mi representado fue nombrado tutor de D./Dª [NOMBRE Y APELLIDOS], por este Tribunal, por auto de fecha de [MES] de [AÑO], en los Autos de Tutela núm. [Nº], tomando posesión de su cargo el día [DÍA] de [MES] de [AÑO].

SEGUNDO.- El tutelado, D./Dª [NOMBRE Y APELLIDOS], ha asistido con regularidad, en régimen externo, al centro [NOMBRE DEL CENTRO], sito en [LOCALIDAD], calle [CALLE], nº [Nº], para recibir la educación especial adaptada al autismo [DIAGNÓSTICO] que padece. Sin embargo, el equipo médico que lo atiende aconseja que ingrese en régimen de internamiento en dicho Centro durante un período de [Nº] meses, con el fin de prestarle la mejor atención posible y mejorar los resultados obtenidos en su tratamiento. Las razones que aconsejan el ingreso se exponen con detalle en el Informe de los facultativos, que se acompaña como DOCUMENTO Nª [Nº DE DOCUMENTO].

Son aplicables a los hechos expuestos, los siguientes

FUNDAMENTOS DE DERECHO

I.JURISDICCIÓN Y COMPETENCIA.- Es competente el Tribunal de Instancia al que me dirijo, conforme a lo dispuesto en los arts. 9 y 21 de la Ley Orgánica del Poder Judicial, en cuanto a la competencia de los órganos Jurisdiccionales Civiles españoles, y al art. 756 de la Ley de Enjuiciamiento Civil, que atribuye la competencia territorial al Juez de Instancia del lugar en que resida la persona a la que se refiera la declaración que se solicite.

II. PROCEDIMIENTO.-Deben seguirse los trámites establecidos en art. 763 de la Ley de Enjuiciamiento Civil.

III. CAPACIDAD.-Tiene mi mandante capacidad para promover este procedimiento, conforme a lo dispuesto en los artículos 6 y ss LEC.

IV. LEGITIMACIÓN.-Mi mandante está legitimado activamente, como tutor del menor [NOMBRE DEL MENOR], para intar este procedimiento, conforme al artículo 271.1º del Código civil y a los artículos 757.4 y 763 de la Ley de Enjuiciamiento Civil. Corresponde la legitimación pasiva al pupilo en relación con el cual se solicita el internamiento.

V. REPRESENTACIÓN Y DEFENSA.-El/La solicitante comparece representado y defendido, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, pese a no ser preceptivo al no tratarse de un proceso contradictorio, sino de un autorización judicial.

VI. DERECHO SUSTANTIVO.-El art. 271.1º del Código Civil dispone que el tutor necesita autorización judicial para internar al tutelado en un establecimiento de salud mental o de educación o formación especial.

VII.-Iura novit curia y los demás que resulten procedentes.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito, se sirva admitirlo y, estimando lo que en él se solicita y previos los trámites legales oportunos, en especial las audiencias contempladas en el art. 763 de la Ley de Enjuiciamiento Civil, dicte resolución por la que autorice a D./Dª [NOMBRE Y APELLIDOS], como tutor de D./Dª [NOMBRE Y APELLIDOS], para internarlo durante un periodo de [PLAZO] en el Centro [NOMBRE DEL CENTRO], sito en [LOCALIDAD], calle [CALLE], nº [NÚMERO], u otro especializado en el tratamiento del autismo [OTROS DATOS], por convenir así a los intereses del tutelado.

OTROSÍ DIGO: Se acompañan los siguientes documentos para acreditar los hechos expuestos:

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador
