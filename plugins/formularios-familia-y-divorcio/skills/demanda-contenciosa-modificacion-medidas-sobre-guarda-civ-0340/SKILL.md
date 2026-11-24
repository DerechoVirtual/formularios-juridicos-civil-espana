---
name: demanda-contenciosa-modificacion-medidas-sobre-guarda-civ-0340
description: "Demanda contenciosa de modificación de medidas sobre guarda y custodia con modificación provisional. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contenciosa de modificación de medidas sobre guarda y custodia con modificación provisional

> Formulario **CIV-0340** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda en procedimiento contencioso de modificación de medidas definitivas sobre guarda y custodia, con solicitud de modificación provisional.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contenciosa de modificación de medidas sobre guarda y custodia con modificación provisional» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contenciosa de modificación de medidas sobre guarda y custodia con modificación provisional” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-contenciosa-modificacion-medidas-sobre-guarda-civ-0340`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº (5 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] SEDE (3 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DEL HIJO/A (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] COLEGIO
- [ ] DATOS DE LA SENTENCIA
- [ ] DOMICILIO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NÚMERO
- [ ] TIPO DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 775.1 LEC
- art. 81 CC
- art. 749.2 LEC
- art. 770 LEC
- art. 775.2 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 90 CC
- art. 776.3.ª LEC
- art. 394 LEC
- art. 775.3 LEC
- art. 771 LEC
- art. 773.3 LEC
- art. 154 CC
- art. 158 CC

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…dictada por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según acredito con aportación de la copia de la escritura de poderes, a la que se acompaña reproducción para testimonio bastante en los autos y devolución de la auténtica, que se necesita para otros usos, y que es dirigido por el Letrado/a D./Dña. [NOMBRE Y APELLIDOS], ejerciente en el Iltre. Colegio de Abogados de [COLEGIO], y con despacho abierto en [LOCALIDAD], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito, formulo DEMANDA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS, contra Dña. [NOMBRE Y APELLIDOS], cuyo domicilio es [DOMICILIO], basándola en los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- Dña. [NOMBRE Y APELLIDOS] y mi representado se hallan separados en virtud de sentencia firme de fecha [FECHA], dictada por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] [DATOS DE LA SENTENCIA], en los autos de [TIPO DE PROCEDIMIENTO] n.º [Nº]

SEGUNDO.- En el fallo de la citada sentencia se adoptaron como medidas definitivas, entre otras, la de atribución de la guarda y custodia a la madre demandada del hijo común menor de edad [NOMBRE DEL HIJO/A], y un prolijo régimen de visitas, comunicación y estancia para el padre que retiene la cotitularidad de la patria potestad, en beneficio del menor.

TERCERO.- Dicha sentencia, que es firme y ejecutoria, no ha sido modificada por ninguna otra resolución firme. Se acompaña testimonio de la sentencia como DOCUMENTO N.º [Nº DE DOCUMENTO]

CUARTO.- En el momento de dictarse la sentencia de separación las circunstancias eran que los cónyuges no tenían en realidad domicilio familiar común, dado que el piso de alquiler en que vivían fue ocupado, después del nacimiento del hijo, por mi mandante, los breves días hasta que fue desahuciado, mientras que la esposa pasó a la casa de sus padres; mi mandante se hallaba en el desempleo; y el hijo tenía escaso año y medio de edad, atravesando una enfermedad grave.

QUINTO.- En la actualidad, el panorama es: a) la demandada jamás ha consentido que el actor ejercite el derecho de visitas que se le reconoció en la sentencia de mérito. Son tres los requerimientos judiciales que se han dirigido a la madre, e incluso tiene abiertas diligencias previas por la Sección de Instrucción del Tribunal de Instancia de [SEDE], por delito de desobediencia grave a la autoridad (DOCUMENTOS NÚMEROS [Nº] a [Nº]); b) mi representado trabaja, ha cumplido sus deberes de abono de pensión alimenticia, y reside en [LOCALIDAD]; c) el hijo tiene [Nº] años de edad, y según noticias indirectas, parece gozar de buena salud; d) la demandada ha abandonado la casa de sus padres y ha llevado consigo al hijo, no teniendo domicilio fijo en la ciudad de [LOCALIDAD] (se adjunta informe policial recabado en las citadas diligencias previas, como DOCUMENTO N.º [NÚMERO]); e) la demandada ha recaído en un problema con el alcohol, por el que ha hecho dejación de sus funciones maternales y se halla inmersa en un estado de desequilibrio de la personalidad, sumado al afán de sustraer al hijo del contacto con el padre.

SEXTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Conforme a lo establecido por el art. 775.1 LEC, en la redacción dada por la Ley 42/2015, de 5 de octubre, es competente para conocer del presente procedimiento el Tribunal al que me dirijo, por ser el que acordó la medida que se quiere modificar.

II.- LEGITIMACIÓN.

La legitimación activa y pasiva para intervenir en el procedimiento corresponde a ambos cónyuges (arts. 81, 86, 90 y 91 CC). Con arreglo al art. 749.2 LEC, deberá ser parte el Ministerio Fiscal, por existir hijos menores en el matrimonio.

III.- PROCEDIMIENTO.

La modificación de las medidas definitivas tiene asignado el procedimiento previsto en el art. 770 LEC, o lo que es lo mismo, el procedimiento principal de separación o divorcio de conformidad con lo establecido en el art. 775.2 LEC en la redacción dada por la Ley 15/2005, de 8 de julio.

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- FUNDAMENTOS DE DERECHO MATERIALES O SOBRE EL FONDO DEL ASUNTO.

Los arts. 90 y 91 CC señalan que las medidas que el Juez acuerde en defecto de acuerdo o las convenidas por los cónyuges, podrán ser modificadas judicialmente o por nuevo convenio cuando se alteren sustancialmente las circunstancias, prevención que es presupuesto de este proceso, según la mención explícita del art. 775.1 LEC.

Las medidas relativas al cuidado de los hijos comunes menores de edad, deben ser adoptadas siempre en su beneficio, como ha manifestado reiteradamente la jurisprudencia, debiendo prevalecer siempre el bienestar de los mismos.

En el caso presente, tanto es evidente que se han alterado sustancialmente las circunstancias, porque el padre está en una disposición física, psíquica y económica proclive a ocuparse de su hijo, y porque la madre ha degenerado en una situación de abandono de sus deberes materno-filiales, como es evidente que se ha producido una perniciosa y enfermiza evitación de cualquier comunicación del padre con el hijo, que a éste perjudica.

Por otro lado, la ejecución incumplida con reiteración puede recibir la sanción del art. 776.3.ª LEC, es decir, la modificación del régimen de guarda y custodia, lo que abona deba serlo en esta vía procesal, cuando se produce una modificación de la base fáctica sobre la que se proyectó la sentencia dictada en su día

VI.- COSTAS

No hay razón para inaplicar el principio del vencimiento en punto a costas procesales, en armonía con el art. 394 LEC, a fin de que esta parte salga indemne de que se le reconozca su derecho frente a la resistencia de la demandada.

En su virtud,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito junto con los documentos y copias que se acompañan, se sirva admitirlo, teniéndome por parte en la representación que acredito y por formulada demanda de modificación de medidas definitivas contra Dña. [NOMBRE Y APELLIDOS], y previos los trámites legales, se dicte sentencia por la que se acuerde la modificación de las medidas que se establecieron en la sentencia de separación sustituyéndolas por la de la atribución de la guarda y custodia del hijo menor [NOMBRE DEL HIJO/A] al actor, lo que determina la extinción por confusión de la obligación de pago de pensión alimenticia correspondiente a aquél, reconociéndose para la madre un régimen de visitas como el de la sentencia de separación para el progenitor no custodio, con expresa condena en costas a la parte demandada.

Es de Justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO: Que al amparo del art. 775.3 LEC, se solicitan mediante el presente escrito MEDIDAS PROVISIONALES DE LA MODIFICACIÓN DE LAS DEFINITIVAS, en base a los siguientes:

HECHOS

ÚNICO.-

Se tienen por reproducidos los hechos de la pretensión principal, destacando el interés urgente y prevalente del hijo menor de edad.

FUNDAMENTOS DE DERECHO

I.- El cónyuge que solicita la modificación de las medidas definitivas, está legitimado, siendo el procedimiento adecuado, en tanto que demandante de las mismas, el de la comparecencia del art. 771 LEC para medidas previas, conforme remisión del art. 773.3 LEC, que a su vez es el cauce a que se refiere el art. 775.3 LEC.

II.- Los requisitos institucionales de la tutela cautelar, amén de su necesaria jurisdiccionalidad, son la instrumentalidad y la urgencia, y sus presupuestos son la apariencia de buen derecho y el peligro de retardo.

Los menores de edad tienen una serie de derechos positivizados en la Ley Orgánica 1/1996 de 15 de enero, de protección jurídica del menor, y los titulares de la patria potestad, que son los padres, tienen el derecho-deber de ocuparse de que puedan ejercerlos (art. 154 CC), y como no lo hagan, la Ley encarga al Juez acordar medidas supletorias.

Conforme a la legitimación extraordinaria del art. 158 CC, cualquier pariente puede activarlas, y así obviamente el padre solicitando la guarda y custodia provisional. Todas las medidas del art. 158 CC pueden adoptarse dentro de cualquier proceso civil o penal o bien en un procedimiento de jurisdicción voluntaria.

Se alega una situación cuya apariencia de buen derecho ya se ha explicado, y cuya urgencia deriva de que en la ejecución de la mentada sentencia de separación se ha conocido de la táctica elusiva, y es el caso de la ignorada ubicación del menor, y sin llegar al extremo de resolver de plano, pues el asunto lleva meses preocupando la ejecución de la sentencia de mérito (la madre no ha permitido en absoluto por años las visitas del padre), procede una comparecencia para decidir un cambio inmediato de la guarda, que no perturbará al hijo, precisamente porque es la madre la que, con otra residencia alejada, cambio de escolarización, otro ambiente, otras costumbres, está perjudicando al niño.

En su virtud,

SUPLICO AL TRIBUNAL

que, teniendo por causadas las precedentes manifestaciones a los efectos oportunos, y por deducida solicitud de adopción de medidas provisionales, seguido que sea su pertinente trámite, se dicte Auto por el que se apruebe las la atribución provisional de titularidad de guarda y custodia del hijo menor al actor D. [NOMBRE Y APELLIDOS], sin perjuicio de la modificación de medidas definitivas, con condena en costas del incidente si la parte adversa se opusiera.

Reitero Justicia en lugar y fecha ut supra.

Firma del Abogado/a	Firma del Procurador/a

========================================================================
