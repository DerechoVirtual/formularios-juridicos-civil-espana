---
name: divorcio-contencioso-conyuges-extranjeros-comunitarios-civ-0296
description: "Divorcio contencioso de cónyuges extranjeros comunitarios (demanda). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Divorcio contencioso de cónyuges extranjeros comunitarios (demanda)

> Formulario **CIV-0296** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de divorcio en procedimiento contencioso de cónyuges extranjeros comunitarios.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Divorcio contencioso de cónyuges extranjeros comunitarios (demanda)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Divorcio contencioso de cónyuges extranjeros comunitarios (demanda)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:divorcio-contencioso-conyuges-extranjeros-comunitarios-civ-0296`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (9 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] CALLE (4 veces)
- [ ] FECHA (4 veces)
- [ ] AÑO (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PAÍS (2 veces)
- [ ] COLEGIO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL HIJO/A 2
- [ ] PAÍS DE LA LEY APLICABLE
- [ ] PETICIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 81.2.º CC
- art. 86 CC
- art. 36.1 LEC
- art. 9.2 LOPJ
- art. 45 LEC
- art. 85.1 LOPJ
- art. 86 LOPJ
- art. 769 LEC
- art. 23.1 LEC
- art. 31.1 LEC
- art. 770 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 9.2 CC
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «… SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [SEDE], Q.P.T.R.C.»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

AL TRIBUNAL DE INSTANCIA [ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [SEDE], Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de Doña [NOMBRE Y APELLIDOS], de nacionalidad [NACIONALIDAD], vecina de [LOCALIDAD], con domicilio en [LOCALIDAD], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo dirección del Letrado D./Dña. [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito interpongo DEMANDA CONTENCIOSA DE DIVORCIO contra Don [NOMBRE Y APELLIDOS], de nacionalidad [NACIONALIDAD], con domicilio actual en [LOCALIDAD], calle [CALLE] n.° [NÚMERO], en base a los siguientes

HECHOS

PRIMERO.- Matrimonio.

Mi representada y Don [NOMBRE Y APELLIDOS], contrajeron matrimonio civil en la ciudad de [LOCALIDAD], sita en [LOCALIDAD], inscrito en el Registro Civil de dicha localidad, según se acredita mediante la certificación de dicho Registro Civil que se aporta como documento número 1 de la presente demanda.

SEGUNDO.- Hijos.

De dicho matrimonio nacieron dos hijos, en fecha [FECHA], que en la actualidad cuenta con 21 años de edad y [NOMBRE DEL HIJO/A 2], en fecha [FECHA], que en la actualidad cuenta con 18 años de edad. Por tanto los dos hijos habidos del matrimonio son mayores de edad.

Se acompañan los certificados de nacimiento como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

TERCERO.- Domicilio conyugal.

El domicilio conyugal ha venido trasladándose según las circunstancias familiares, hasta el año [AÑO] el matrimonio residió en [PAÍS], país de origen de ambos, y en el año [AÑO] el matrimonio se trasladó a vivir a España, fijando el domicilio conyugal en la calle [CALLE] de [LOCALIDAD], en vivienda en régimen de alquiler. Se acompañan el libro de familia, certificado de empadronamiento, y pasaporte de la actora como documentos números [Nº DE DOCUMENTO], [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

Desde el día [FECHA] cesó la convivencia entre mi patrocinada y el hoy demandado Don [NOMBRE Y APELLIDOS], habiendo abandonado este último el domicilio familiar, trasladándose a vivir con su hermano, y mi mandante ocupa el domicilio conyugal, junto a los dos hijos habidos del matrimonio.

El demandado reside desde entonces en [LOCALIDAD], calle [CALLE], conforme acredito con certificado de empadronamiento que se acompaña como documento número [Nº DE DOCUMENTO].

CUARTO.- Petición de divorcio y efectos.

Es voluntad de mi representada disolver su matrimonio por divorcio y que se adopten las siguientes medidas [PETICIÓN]

Se acompaña, como exige el art. 81.2.º "in fine" CCiv, al que reenvía el art. 86 CCiv, propuesta fundada de las medidas que han de regular los efectos derivados del divorcio (documento número [Nº DE DOCUMENTO]).

QUINTO.- Sobre el proceso de negociación previo y medios de solución de controversias de manera amistosa y extrajudicial

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Competencia internacional.

La resolución de la pretensión de divorcio pertenece a la jurisdicción, y a tenor del art. 36.1 LEC, la extensión y límites de la jurisdicción de los tribunales civiles españoles se determinará por lo dispuesto en la Ley Orgánica del Poder Judicial y en los tratados y convenios internacionales en los que España sea parte.

Dicha normativa viene constituida por el Reglamento (UE) 2019/1111 del Consejo, de 25 de junio de 2019, relativo a la competencia, el reconocimiento y la ejecución de resoluciones en materia matrimonial y de responsabilidad parental, y sobre la sustracción internacional de menores.

En materia de matrimonio, el art. 3.a).i) del Reglamento atribuye competencia para resolver las cuestiones relativas al divorcio, la separación judicial o la nulidad del matrimonio de los cónyuges, a los órganos jurisdiccionales del Estado miembro en cuyo territorio se encuentre la residencia habitual de los cónyuges.

Competencia genérica.

Está atribuida al orden civil de jurisdicción, conforme al art. 9.2 LOPJ.

Competencia objetiva.

Por lo tocante a la competencia objetiva corresponde a los Tribunales de Instancia -art. 45 LEC en relación con el art. 85.1º LOPJ-, y con arreglo a la especialización ex art. 86 LOPJ, a las Secciones de Familia, Infancia y Capacidad que hay en esta ciudad.

Competencia territorial interna.

Se asigna desde el art. 769 LEC, a los Tribunales del último domicilio del matrimonio.

II.- PARTES

Capacidad.

Las partes poseen capacidad para ser parte y procesal, en cuanto que personas físicas mayores de edad en pleno ejercicio de sus derechos civiles (arts. 6.1.1.º y 7.1 LEC).

Legitimación.

Ostentan las partes legitimación ordinaria por ocupar la posición de cónyuges en la situación jurídica de relación matrimonial (art. 10 párrafo 1.º LEC), siendo el objeto de la pretensión la disolución vincular por divorcio.

Postulación.

Esta parte, como será debido para la personación que convenga a la contraria, comparece por medio de Procurador de los Tribunales habilitado ante el tribunal (art. 23.1 LEC), y bajo la dirección del Letrado en ejercicio (art. 31.1 LEC).

III.- PROCEDIMIENTO

El procedimiento a través del que ha de sustanciarse la pretensión es el recogido en el art. 770 LEC.

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- FONDO DEL ASUNTO

Derecho aplicable.

AL DIVORCIO

En virtud de lo dispuesto en el art. 8.a) del Reglamento (UE) 1259/2010 del Consejo, de 20 de diciembre de 2010, por el que se establece una cooperación reforzada en el ámbito de la ley aplicable al divorcio y a la separación judicial, resulta de aplicación la ley española, por ser la ley de la residencia habitual de los cónyuges en el momento de la interposición de la demanda.

AL RÉGIMEN ECONÓMICO MATRIMONIAL

En aplicación del art. 9.2 CCiv, resulta de aplicación la ley [PAÍS DE LA LEY APLICABLE], por ser la ley personal común de los cónyuges al tiempo de contraer matrimonio.

Se aporta como documento número 9 traducción al español de la legislación de [PAÍS] en vigor.

Pretensiones ejercibles.

El fondo de la pretensión consiste en la declaración de divorcio, a fin de la disolución del matrimonio, a instancia de uno de los cónyuges, de conformidad con el art. 81.2.º CCiv, por remisión del art. 86 CCiv, después de transcurridos tres meses desde la celebración del matrimonio sin que puedan oponerse por el otro cónyuge, no expresamente conforme ninguna causa de oposición material, al fundarse en la voluntad de no permanecer casado, como corolario legal del derecho del art. 32 CE a contraer matrimonio.

VI.- COSTAS

Deberá ser impuesto a la contraparte el reembolso de las costas del proceso, en virtud de lo establecido en el art. 394 LEC.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito de demanda junto con sus documentos y copias, se sirva admitirlo, y habiéndome por personado y parte por quien comparezco, y por formulada demanda de divorcio matrimonial contra Don [NOMBRE Y APELLIDOS], y seguido que sea el trámite legal oportuno, dicte sentencia por la que:

1.- Se declare la disolución del matrimonio por divorcio de Dony Doña [NOMBRE Y APELLIDOS]
2.- Se acuerden las siguientes medidas

Todo ello con expresa condena en costas a la parte contraria, si se opusiera.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
