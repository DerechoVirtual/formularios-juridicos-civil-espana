---
name: demanda-fiscal-impugnando-reconocimiento-paternidad-civ-0369
description: "Demanda del fiscal impugnando un reconocimiento de paternidad que encubre una adopción ilícita. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda del fiscal impugnando un reconocimiento de paternidad que encubre una adopción ilícita

> Formulario **CIV-0369** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de acción de impugnación de la paternidad no matrimonial interpuesta por el Ministerio Fiscal frente a un supuesto reconocimiento de filiación paterna como medio de adopción ilícita de un menor por precio. Solicitud de prueba biológica anticipada, medida cautelar inmediata sin caución y nombramiento de defensor judicial.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda del fiscal impugnando un reconocimiento de paternidad que encubre una adopción ilícita» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda del fiscal impugnando un reconocimiento de paternidad que encubre una adopción ilícita” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-fiscal-impugnando-reconocimiento-paternidad-civ-0369`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (18 veces)
- [ ] NÚMERO (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE DEL MENOR (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] FECHA (3 veces)
- [ ] SEDE (3 veces)
- [ ] APELLIDOS (2 veces)
- [ ] CALLE
- [ ] DÍA
- [ ] LUGAR
- [ ] NACIONALIDAD
- [ ] NOMBRE DE LA CLÍNICA
- [ ] Nº
- [ ] Nº DE ARTÍCULO

## Normas que cita el formulario

- art. 85.1 LOPJ
- art. 50.1 LEC
- art. 6.1.6 LEC
- art. 124 LOPJ
- art. 137 CC
- art. 766 LEC
- art. 753 LEC
- art. 405 LEC
- art. 748.2 LEC
- art. 767.1 LEC
- art. 764.1 LEC
- art. 140 CC
- art. 293 LEC
- art. 767.2 LEC
- art. 767.4 LEC
- art. 728.3 LEC

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

- Junto a «…CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA Q.P.T.R.C. DE LOS DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…en la Sección de Instrucción del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA Q.P.T.R.C. DE LOS DE [SEDE]

EL FISCAL DEL TRIBUNAL SUPERIOR DE JUSTICIA DE LA COMUNIDAD AUTÓNOMA DE, ante el Tribunal al cual tengo el honor de dirigirse, comparezco y como mejor en Derecho proceda, DIGO:

Que formulo DEMANDA DE ACCIÓN DE IMPUGNACIÓN DE LA PATERNIDAD NO MATRIMONIAL del menor [NOMBRE DEL MENOR] contra Don [NOMBRE Y APELLIDOS], Doña [NOMBRE Y APELLIDOS], y el menor [NOMBRE DEL MENOR], en base a los siguientes

HECHOS

PRIMERO.- El día [FECHA], Doña [NOMBRE Y APELLIDOS], ingresó como paciente en la Clínica [NOMBRE DE LA CLÍNICA], sita en la calle [CALLE], nº [NÚMERO] de [LOCALIDAD], donde dio a luz un varón mediante parto inducido, siendo dada de alta al de dos días, el [DÍA] del mismo mes y año.

SEGUNDO.- El mismo día en que abandonaba el centro hospitalario, Doña [NOMBRE Y APELLIDOS] entregó a su hijo recién nacido a la pareja de hecho formada por Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS], quienes previamente habían abonado a la primera cierta cantidad de dinero.

TERCERO.- Al día siguiente, Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS] acudieron al Registro Civil de [LOCALIDAD], donde inscribieron al menor como [NOMBRE Y APELLIDOS], haciendo constar la filiación paterna en favor de Don [NOMBRE Y APELLIDOS], y la filiación materna en favor de Doña [NOMBRE Y APELLIDOS].

Se acompaña certificación literal de nacimiento como DOCUMENTO Nº [Nº DE DOCUMENTO].

CUARTO.- Por estos hechos se siguen Diligencias Previas nº [NÚMERO] /, en la Sección de Instrucción del Tribunal de Instancia de [SEDE], plaza n.º [Nº] , por un presunto delito contra las relaciones familiares previsto en los artículos 220 y siguientes del Código Penal, cuyo testimonio se aporta como DOCUMENTO Nº [Nº DE DOCUMENTO].

En el dicho testimonio aparece el parte clínico del alumbramiento, y los pormenores de la transacción prohibida y sus intermediarios.

QUINTO.- Como puede observarse de la simple lectura de la declaración que Doña [NOMBRE Y APELLIDOS] efectuó el [FECHA], en calidad de detenida, ante la Sección de Instrucción del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO], entre la citada y Don [NOMBRE Y APELLIDOS], no ha existido relación alguna a la pueda obedecer la concepción del menor.

Siendo de esta forma evidente la más absoluta discordancia entre el Registro y la realidad extrarregistral de la generación, es por lo que este Ministerio Fiscal, principal garante de los intereses del menor, ejercita la acción de impugnación de la paternidad inscrita.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

La competencia objetiva corresponde a los Tribunales de Instancia (arts. 85.1 LOPJ y 45 LEC), y la territorial corresponde al Tribunal al que nos dirigimos, en virtud de lo dispuesto en los arts. 50.1 y 2 LEC, habida cuenta del domicilio de los residentes en España, el lugar en que se halla Doña Catalina [APELLIDOS], nacional de [NACIONALIDAD], domiciliada en el extranjero, y 53.2 LEC, que permite elegir al demandante el lugar del domicilio de cualquiera de ellos.

II.- CAPACIDAD Y POSTULACIÓN.

El Ministerio Fiscal tiene capacidad para ser parte en los procesos civiles en armonía con art. 6.1.6º LEC, de modo que ostenta capacidad procesal, sin tener que intermediarse sus individuos con otros profesionales del Derecho, cuando está prevista su intervención legalmente, en cuyo caso su actuación es preceptiva en defensa de la legalidad, promoviendo la acción de la Justicia (arts. 124 CE, 541 LOPJ, y 3 Estatuto orgánico), siendo el caso de actuación como parte procesal.

III.- LEGITIMACIÓN.

El Ministerio Fiscal está legitimado activamente conforme a lo dispuesto en el art. 137 CCiv, y 765.1 LEC, puesto que compete acción de impugnación al menor Armando [APELLIDOS], en cuya representación, indistintamente con sus representantes legales en potestad, corresponde al Ministerio Fiscal.

La legitimación pasiva corresponde a Don [NOMBRE Y APELLIDOS] y a Doña [NOMBRE Y APELLIDOS], y al menor [NOMBRE Y APELLIDOS], todo ello a tenor del art. 766 LEC, puesto que son quienes aparecen como progenitores y como hijo en virtud de la filiación legalmente determinada, tratándose de determinar la filiación biológica.

IV.- PROCEDIMIENTO.

Los trámites a seguir serán los del propio del juicio verbal con las especialidades que se prevén en el art. 753 LEC, que suponen traslado para posible contestación escrita conforme a art. 405 LEC, que es el del Título I del Libro IV LEC, sin precepto en contrario aplicable a los litigios con objeto del art. 748.2º LEC.

V.- PRESUPUESTO DE PROCEDIBILIDAD.

En cumplimiento de lo dispuesto, en el art. 767.1 LEC, como requisito preliminar del proceso, de la necesidad de acompañar a la demanda un principio de prueba de los hechos en que se funde, con lo que se trata de avanzar el juicio de seriedad en cuanto al buen derecho del fondo de la pretensión en trámite de admisión de la demanda, se presentan los siguientes documentos:

l.- Certificación literal de la inscripción de nacimiento del menor [NOMBRE DEL MENOR] (DOCUMENTO Nº [Nº DE DOCUMENTO]).

2.- Testimonio de las Diligencias Previas que se siguen ante la Sección de Instrucción del Tribunal de Instancia nº [NÚMERO], bajo nº [NÚMERO] / (DOCUMENTO Nº [Nº DE DOCUMENTO]).

VI.- Arts. 108 y ss. del CCiv, en cuanto al fondo material del asunto.

Para los procesos en que se ejercitan acciones de filiación, el principio en esta materia es la búsqueda a todo trance de la verdadera filiación natural o biológica, y por ende, la indisponibilidad del objeto del proceso, y la búsqueda de oficio de la autenticidad de la procreación, contando el Tribunal con posibilidades inquisitivas, siendo regla la viabilidad de solicitar de los tribunales la determinación legal de la filiación o la impugnación de la legalmente determinada (art. 764.1 LEC), con la sola salvedad del respeto a la cosa juzgada material, ya que la investigación de la paternidad es de oportunidad procesal única, pero que en el presente supuesto no se ha producido, sino que se insta ahora.

En armonía con la antedicha regulación sustantiva, las acciones de impugnación pueden ejercitarse por quienes se encuentran en la situación jurídica de padre, hijo y cualquiera a quien perjudique, si se trata de impugnar la paternidad no matrimonial (art. 140 CCiv), por lo que interesando al orden público la impugnación por el hijo, a la luz de los hechos, y siendo recién nacido, la ejercita el Ministerio Público.

Por lo expuesto,

EL FISCAL respetuosamente interesa que,

habiendo por presentado este escrito, se sirva admitirlo con los documentos que se acompañan, y siguiendo el procedimiento por todos sus regulares trámites, se dicte sentencia en definitiva que declare la nulidad de la inscripción de paternidad del menorverificada a favor de D. [NOMBRE Y APELLIDOS], estando y pasando por la misma los codemandados, y haciéndolo constar a los efectos oportunos en el Registro Civil de [LOCALIDAD], mediante el oportuno mandamiento cancelatorio.

Es de Justicia que se pide en [LUGAR], a [FECHA].

OTROSÍ PRIMERO DIGO: Al amparo de lo dispuesto en el art. 293 LEC, se interesa la práctica, como prueba anticipada, de la prueba biológica relativa a la paternidad de D. respecto del menor [NOMBRE DEL MENOR], medio probatorio pericial destacado por el art. 767.2 LEC, debiéndose admitir por el temor fundado de la dificultad y retardo de practicarse en su momento procesal ulterior, habida cuenta que la negativa injustificada a someterse a las pruebas biológicas permitirá al Tribunal declarar la nulidad de la filiación inscrita, siempre que no se haya demostrado su genuidad por otros medios, supuesto de presunción ‘ad hominem’ positivizada que debe seguir las directrices de la doctrina constitucional de STC 7/94 de 17 de enero, y STC 276/96 de 2 de octubre (art. 767.4 LEC).

OTROSÍ SEGUNDO DIGO: Como medida cautelar al amparo de lo dispuesto en el art. 150 del Reglamento del Registro Civil y en los arts [Nº DE ARTÍCULO] 727.5º, 728.1 y 768.1 LEC, se interesa proceda a ordenarse la anotación preventiva de la demanda en el Registro Civil de [LOCALIDAD], al margen de la inscripción de nacimiento del menor

La medida parece imperativa, en los procesos impugnatorios, y en el caso se excusa la previa audiencia de la parte contraria, por concurrir razones de urgencia, y sin perjuicio de la comparecencia del art. 768.3.pfo.2º LEC, en que se podrá requerir a propósito de la prueba anticipada al codemandado Don [NOMBRE Y APELLIDOS]

No procede exigir caución a quien solicita la tutela cautelar, dado que ostenta legitimación extraordinaria por intereses políticos, que es el caso excepcional avanzado por art. 728.3 LEC, y que prevé el 768.3.pfo.3º LEC.

OTROSÍ TERCERO DIGO: Al amparo de lo dispuesto en los arts. 7.1 y 2, y 8.l y 2 LEC, procédase al nombramiento de un defensor judicial del menor.

Del TRIBUNAL nuevamente interesa EL FISCAL, se sirva tener por causadas las peticiones antecedentes, y resuelva de conformidad con lo pedido, por ser de justicia de hacerse, en cuanto a lo principal y otrosíes en el lugar y fecha indicados "ut supra".

Firma del Fiscal

========================================================================
