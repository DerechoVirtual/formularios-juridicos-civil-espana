---
name: escrito-tutor-pidiendo-autorizacion-judicial-demandar-civ-0375
description: "Escrito del tutor pidiendo autorización judicial para demandar en nombre del tutelado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del tutor pidiendo autorización judicial para demandar en nombre del tutelado

> Formulario **CIV-0375** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del tutor pidiendo autorización judicial para demandar en nombre del tutelado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del tutor pidiendo autorización judicial para demandar en nombre del tutelado” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:escrito-tutor-pidiendo-autorizacion-judicial-demandar-civ-0375`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] MES (5 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] COLEGIO (3 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] CALLE
- [ ] FECHA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] NIF
- [ ] NÚMERO

## Normas que cita el formulario

- art. 224 Código Civil
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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de D./Dª [NOMBRE Y APELLIDOS], como tutor/a de D./Dª [NOMBRE Y APELLIDOS], con DNI/NIF [NIF] y domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], según se acredita por certificación del registro electrónico de apoderamientos judiciales que se acompaña (o mediante designación apud acta ante el Letrado de la Administración de Justicia de [LOCALIDAD]) o según consta acreditado en el expediente de jurisdicción voluntaria, bajo la dirección técnica de D./Dª [NOMBRE Y APELLIDOS], Letrado del Ilustre Colegio de [COLEGIO], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito, en la representación que acredito, formulo SOLICITUD EN PROCEDIMIENTO DE JURISDICCIÓN VOLUNTARIA DE AUTORIZACIÓN PARA ENTABLAR DEMANDA EN NOMBRE DEL TUTELADO, conforme con lo dispuesto en el art. 287.7º en relación con lo dispuesto en el art. 224 del Código Civil y en los artículos 61 y ss. de la Ley de la Jurisdicción Voluntaria, con base en los los siguientes

HECHOS

PRIMERO.- Mi representado fue nombrado tutor de D./Dª [NOMBRE Y APELLIDOS], por este Tribunal, por auto de fecha [DÍA] de [MES] de [AÑO], tomando posesión de su cargo el día [FECHA] de [MES] de

SEGUNDO.- En el ejercicio de su cargo de tutor, revisando los documentos, cuantas y asuntos del tutelado, ha constatado que en la escritura de partición de la herencia del padre de éste/a, otorgada por los coherederos ante D./Dª [NOMBRE Y APELLIDOS], Notario del Ilustre Colegio de [COLEGIO], en fecha [DÍA] de [MES] de [AÑO], con número de protocolo [Nº DE PROTOCOLO], antes, por tanto, de que mi representado ejerciera el cargo de tutor, existe una lesión en más de la cuarta parte atendido el valor atribuido a la finca sita en [LOCALIDAD], adjudicada al tutelado, que fue claramente sobrevalorada en el inventario de la herencia. Se cuantifica la lesión en [IMPORTE] euros.

Han resultado infructuosos los intentos, por parte de mi representado, por llegar a un acuerdo extrajudicial con los coherederos del tutelado.

Dado que no han transcurrido todavía cuatro años desde el otorgamiento de la citada escritura de partición, la acción rescisoria por causa de lesión no ha caducado, considerando mi representado que es de interés para el tutelado interponerla.

Son aplicables a los hechos expuestos, los siguientes

FUNDAMENTOS DE DERECHO

I. JURISDICCIÓN Y COMPETENCIA.-Es competente el Tribunal de Instancia al que me dirijo, conforme a lo dispuesto en los arts. 2 y 62.1 de la Ley de la Jurisdicción Voluntaria, por ser el correspondiente al domicilio del menor.

II. PROCEDIMIENTO.-Deben seguirse los trámites establecidos en los artículos 17 a 22 y 63 y ss. de la Ley de la Jurisdicción Voluntaria.

III. CAPACIDAD.-Tiene mi mandante capacidad para promover este procedimiento, conforme a lo dispuesto en los artículos 6 y ss LEC.

IV. LEGITIMACIÓN.-Mi mandante está legitimado activamente, como representante legal del menor (o persona con la capacidad judicialmente modificada), para promover este procedimiento, conforme al artículo 271.6º del Código civil y al artículo 62.2 de la Ley de la Jurisdicción Voluntaria.

V. REPRESENTACIÓN Y DEFENSA.-En virtud de los artículos 3 y 62.3 de la Ley de la Jurisdicción Voluntaria, es preceptiva la intervención de Abogado y Procurador, al exceder el valor del acto para el que se insta el presente expediente de 6.000 euros.

VI. INTERVENCIÓN DEL MINISTERIO FISCAL.-Debe intervenir y ser oído el Ministerio Fiscal conforme a lo dispuesto en los artículos 4 y 30.1 de la Ley de la Jurisdicción Voluntaria.

VII. DERECHO SUSTANTIVO.- El art. 287.7º del Código civil, aplicable a la tutela por remisión del art. 224 del mismo texto legal, dispone que el tutor necesita autorización judicial para entablar demanda en nombre de la persona a la que presta apoyo, salvo en los asuntos urgentes o de escasa cuantía.

VIII. GASTOS.-Se rigen por lo dispuesto en el artículo 7 de la Ley de la Jurisdicción Voluntaria.

IX.-Iura novit curia y los demás que resulten procedentes.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito, con sus copias, se sirva admitirlo y, estimando lo que en él se solicita y previos los trámites legales oportunos, autorice a D./Dª [NOMBRE Y APELLIDOS], como tutor de D./Dª [NOMBRE Y APELLIDOS], para interponer, en nombre y representación de éste, demanda de rescisión por lesión de la partición de herencia formalizada mediante escritura otorgada ante D./Dª [NOMBRE Y APELLIDOS], Notario del Ilustre Colegio de [COLEGIO], en fecha [DÍA] de [MES] de [AÑO], con número de protocolo [Nº DE PROTOCOLO], por convenir así a los intereses del tutelado.

OTROSÍ DIGO: Se acompañan los siguientes documentos para acreditar los hechos expuestos:

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
