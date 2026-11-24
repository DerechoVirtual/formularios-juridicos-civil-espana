---
name: solicitud-medidas-judiciales-desacuerdo-ejercicio-civ-0185
description: "Solicitud de medidas judiciales por desacuerdo en el ejercicio de la patria potestad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de medidas judiciales por desacuerdo en el ejercicio de la patria potestad

> Formulario **CIV-0185** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de medidas judiciales por desacuerdo en el ejercicio de la patria potestad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de medidas judiciales por desacuerdo en el ejercicio de la patria potestad” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-medidas-judiciales-desacuerdo-ejercicio-civ-0185`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE DEL CENTRO (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] DÍA (3 veces)
- [ ] FECHAS (2 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] CORREO ELECTRÓNICO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] Nº

## Normas que cita el formulario

- art. 156 Código Civil
- art. 5 Ley Orgánica 1/2025

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

- Junto a «…NCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «… [NOMBRE Y APELLIDOS], ante la Sección Civil del Tribunal de Instancia de [SEDE]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

D. [NOMBRE Y APELLIDOS], actuando en su nombre y representación de [NOMBRE DEL REPRESENTADO/A], mayor de edad, y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS], ante la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda comparezco y, como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito y al amparo de lo dispuesto en el artículo 156 el C.C. y de los artículos 85 y 86 ambos de la 15/15, en la nueva redacción dada por la Ley 8/2021 de 2 de junio, promueve expediente de jurisdicción voluntaria para que se autorice judicialmente la estancia de los hijos menores de mi representada [NOMBRE DEL REPRESENTADO/A] durante los días [FECHAS] a [DÍA] del mes de julio en el Colegio [NOMBRE DEL CENTRO] a fin de cursar estudios de inglés, al oponerse el padre D. [NOMBRE Y APELLIDOS], en base a los siguientes

HECHOS

Que mi representada es madre del menor [NOMBRE DEL MENOR], de [Nº] años de edad, quien convive en su domicilio sito en [LOCALIDAD], ostentando la guarda del mismo y la patria potestad compartida con el padre [NOMBRE Y APELLIDOS], con quien no convive con el menor y la madre, y con quien mi representada convino un régimen de visitas consistente en fines de semana alternos desde las 20.00 horas del viernes a las 20.00 horas del domingo (acompaño como documentos [Nº DE DOCUMENTO] certificados de nacimiento del menor y de los padres, libro de familia y convenio suscrito entre los padres regulador de la guarda y régimen de visitas del menor).

El menor [NOMBRE DEL MENOR] está a punto de finalizar sus estudios de tercer curso de Educación Secundaria en el colegio [NOMBRE DEL CENTRO]

Mi representada, a fin de mejorar su nivel del idioma inglés, matriculó al menor en el colegio [NOMBRE DEL CENTRO] de la localidad de [LOCALIDAD], con la finalidad de hacer un curso intensivo de inglés desde los días [FECHAS] a [DÍA] del mes de julio en régimen de internado (acompaño como documentos [Nº DE DOCUMENTO] certificado de matriculación del menor en el centro de educación secundaria [NOMBRE DEL CENTRO] y en el curso intensivo de inglés impartido por el colegio [NOMBRE DEL CENTRO], así como folleto explicativo del curso de inglés de verano).

Al comunicar dicha decisión al padre, adoptada en beneficio exclusivo del menor, el padre mostró su rotunda oposición, habiendo remitido un requerimiento notarial para que mi representada se abstuviera de matricular al menor en el citado colegio, amenazándole con denunciarla por incumplir el régimen de visitas pactado (acompaño como documento [Nº DE DOCUMENTO] copia del requerimiento remitido por el padre del menor).

Ante esta situación y dado que el padre ha exteriorizado su desacuerdo con la decisión de la madre, adoptada en beneficio del menor y con la anuencia de éste, según se acreditará oportunamente, nos vemos en la obligación de instar el presente expediente a fin de que por V.I. se decida lo más idóneo en beneficio del menor, entendiendo que la realización del curso de inglés concertado por mi representada es lo más adecuado para su formación personal y educativa, comprometiéndose esta parte a asumir íntegramente el coste económico del curso que se pretende llevar a cabo.

Por lo expuesto, se solicita, de conformidad con el artículo 156 del Código Civil que se acuerde, tras oír al padre y al menor, autorizar la decisión de mi representada de matricular a su hijo en el curso de inglés antes mencionado.

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA. Son competentes las secciones civiles de los tribunales de instancia de esta ciudad, por ser la del domicilio del hijo, conforme a lo dispuesto en el art. 86.2 de la Ley de Jurisdicción Voluntaria.

II.- PROCEDIMIENTO. Debe seguirse el procedimiento de jurisdicción voluntaria regulado en los artículos 85 y siguientes de la Ley de Jurisdicción Voluntaria.

III.- LEGITIMACIÓN. Esta parte está legitimada conforme a lo dispuesto en el art. 156 del Código Civil y art. 86.3 de la Ley de Jurisdicción Voluntaria.

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD. La presente demanda cumple con los requisitos de procedibilidad exigidos por el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- FUNDAMENTOS DE FONDO. El art. 156 del Código Civil establece que, en caso de desacuerdo en el ejercicio de la patria potestad, el Juez decidirá después de oír a los padres y al hijo si tuviera suficiente juicio y en todo caso si es mayor de doce años, debiendo decidirse conforme al principio rector en la materia que es el de interés del menor y de acuerdo con lo dispuesto en el artículo 156, último párrafo, en cuanto a la prevalencia de la decisión respecto del progenitor con quien convive el menor.

Por lo expuesto,

AL TRIBUNAL SUPLICO: Que tenga por presentado este escrito con los documentos que se acompañan, lo admita, y tenga por promovido expediente de jurisdicción voluntaria en demanda de autorización de la matriculación del hijo menor en el curso de verano de inglés antes descrito, y practicadas las diligencias oportunas, incluida la audiencia de los padres y del menor que se interesa en el otrosí y con intervención del Ministerio Fiscal, y previos los demás trámites con arreglo a Derecho dicte resolución en la que se autorice la matriculación del menor en el curso de inglés interesado en el cuerpo de este escrito.

OTROSÍ PRIMERO DIGO que a efectos de comunicaciones designo el domicilio del letrado firmante de este escrito sito en [LOCALIDAD], así como la dirección de correo electrónico del mismo [CORREO ELECTRÓNICO] y el número de fax

SUPLICO AL TRIBUNAL: tenga por hecha la citada designación de domicilio.

OTROSÍ SEGUNDO DIGO: Que intereso, de conformidad con lo dispuesto en el artículo 85.1 de la Ley de Jurisdicción Voluntaria, que sean oídos los padres y el menor, comprometiéndose esta parte a la comparecencia de mi representada y del menor el día y hora que se señale, señalando como domicilio del padre el siguiente:

- D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD]

SUPLICO AL TRIBUNAL: Tenga por realizadas las manifestaciones, solicitando que el padre sea citado judicialmente para la práctica de la diligencia.

Es Justicia que insto en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma del solicitante y letrado.

========================================================================
