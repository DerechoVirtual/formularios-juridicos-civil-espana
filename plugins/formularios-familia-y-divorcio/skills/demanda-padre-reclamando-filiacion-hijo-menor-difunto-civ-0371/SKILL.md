---
name: demanda-padre-reclamando-filiacion-hijo-menor-difunto-civ-0371
description: "Demanda del padre reclamando filiación de hijo menor difunto e impugnando otra filiación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda del padre reclamando filiación de hijo menor difunto e impugnando otra filiación

> Formulario **CIV-0371** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda en reclamación de determinación legal de filiación no matrimonial interpuesta por el padre en relación al hijo menor de edad fallecido, e impugnación de la filiación contradictoria.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda del padre reclamando filiación de hijo menor difunto e impugnando otra filiación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda del padre reclamando filiación de hijo menor difunto e impugnando otra filiación” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-padre-reclamando-filiacion-hijo-menor-difunto-civ-0371`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] CALLE (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] COLEGIO
- [ ] LUGAR
- [ ] NOMBRE DEL MENOR
- [ ] Nº
- [ ] Nº DE COLEGIADO
- [ ] SEDE

## Normas que cita el formulario

- art. 6.1.1 LEC
- art. 766 LEC
- art. 749.1 LEC
- art. 753 LEC
- art. 767 LEC
- art. 767.1 LEC
- art. 73.1 LEC
- art. 767.2 LEC
- art. 767.4 LEC
- art. 767.3 LEC
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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…ompetencia objetiva y geográfica a la Sección Civil del Tribunal de Instancia de»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], provisto de D.N.I. nº [NÚMERO], y domiciliado en esta ciudad, calle [CALLE], nº [NÚMERO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, dirigido por el Letrado suscrito D./Dña. [NOMBRE Y APELLIDOS], colegiado nº [Nº DE COLEGIADO] del Iltre. Colegio de Abogados de [COLEGIO], con despacho abierto en [LOCALIDAD], calle [CALLE], nº [NÚMERO], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito vengo a formular demanda en reclamación de determinación legal de filiación e impugnación de la contradictoria frente a D./Dña. [NOMBRE Y APELLIDOS], en su calidad de heredero de su hijo menor que falleció en su potestad [FECHA], con domicilio en [LOCALIDAD], calle [CALLE], nº [Nº], y frente al Ministerio Fiscal, en base a los siguientes datos y argumentos:

HECHOS

PRIMERO.- Dña. contrajo matrimonio canónico con D. [NOMBRE Y APELLIDOS], el demandado, en [LOCALIDAD], el día [FECHA], a cuya acreditación se acompaña certificación expedida por el Registro Civil de [LOCALIDAD], como documento nº [Nº DE DOCUMENTO].

SEGUNDO.- Dña. dio a luz un hijo, de nombre [NOMBRE Y APELLIDOS], que fue inscrito como hijo matrimonial de la dicha y el demandado D [NOMBRE Y APELLIDOS], por haber contraído dichas personas matrimonio después del nacimiento y haber sido reconocido por el demandado expresamente ante el Encargado del Registro Civil, y para su demostración adjunto certificación de nacimiento del Registro Civil de [LOCALIDAD], que hace documento nº [Nº DE DOCUMENTO].

TERCERO.- En desdichado accidente de tráfico automovilístico, el pasado día [FECHA], encontraron la muerte, los indicados madre e hijo, mientras éste era menor de edad y estaba en la potestad de sus padre.

Se acompañan los respectivos certificados de defunción del Registro Civil de [LOCALIDAD], como documentos nos. y [Nº DE DOCUMENTO]). Según se observa, el hijo falleció horas después que la madre.

CUARTO.- El menor [NOMBRE DEL MENOR] fue en realidad hijo de mi patrocinado y la finada Dña. [NOMBRE Y APELLIDOS], fruto de la convivencia de ambos en el tiempo de la concepción, a cuya acreditación se adjuntan reconocimiento explícito en documento privado (documento nº [Nº DE DOCUMENTO])

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Es el orden civil de la Jurisdicción quien tiene confiada la competencia genérica para la tutela judicial del estado civil, y por ende, el conocimiento de las acciones de filiación, y corresponde la competencia objetiva y geográfica a la Sección Civil del Tribunal de Instancia de esta circunscripción que por turno de reparto corresponda, conforme arts. 45 y 50.1 LEC, habida cuenta que se ejercita una pretensión que fija proceso por materia -no por cuantía- y que el fuero territorial general, a falta de prevención legal especial que aquí no se da, para las personas físicas, es el domicilio del demandado.

II.- CAPACIDAD Y LEGITIMACIÓN.

Todos los intervinientes detentan capacidad para ser parte, en cuanto que son personas físicas y la detenta siempre el Ministerio Fiscal cuando le asigna un papel procesal la ley (arts. 6.1.1º y 6º LEC).

El padre está legitimado activamente para reclamar la filiación no matrimonial sin posesión de estado, de acuerdo con la interpretación conjunta de arts. 131, 133 y 134.pfo.1º CCiv (SSTS de 24 de junio de 1996, Rec. 3379/1992 y STS 14 de abril de 1998, Rec. 472/1996). Lo está pasivamente aquel a quien se atribuye la condición de hijo cuya paternidad se reclama (art. 766 LEC), y correspondiendo la acción contra el hijo menor de edad que ha fallecido, la legitimación pasiva es ejercida por su padre, heredero, todo con arreglo al art. 766 LEC. El Ministerio Fiscal está legitimado de manera extraordinaria (art. 10.pfo.2º LEC), por aplicación del art. 749.1 LEC.

III.- PROCEDIMIENTO.

Con arreglo al art. 753 LEC, el proceso signado para conocimiento de las acciones de filiación, es el juicio especial verbal con contestación escrita del Título I del Libro IV LEC, con sus matices de arts. 767 y 768 LEC.

IV.- PRINCIPIO DE PRUEBA.

Se cumple la exigencia del art. 767.1 LEC, en cuanto que se presenta principio de prueba de los hechos en que se funda la demanda, como así debe entenderse resultar de la documental aportada, que acreditando la convivencia permanente de ambos progenitores durante el tiempo de la gestación y nacimiento, y el reconocimiento explícito de la madre.

V.- ACCIONES ACUMULADAS.

Reclamación de paternidad e impugnación de filiación contradictoria son pretensiones acumulables, al amparo de los arts. 131, 134.pfo.1º y 140 CCiv, y no incompatibles conforme art. 73.1 LEC. Se postula la nulidad de la filiación contradictoria por ser nulo el reconocimiento efectuado (arts. 119 y 120 y ss. CCiv) en el que falta el presupuesto fáctico de la paternidad; debe citarse aquí el art. 108 C.C. en cuanto establece que la filiación por naturaleza puede ser matrimonial y no matrimonial; no siendo por naturaleza, la filiación matrimonial deviene nula y su reconocimiento ineficaz.

VI.- INVESTIGACION DE LA PATERNIDAD.

El art. 767.2 LEC establece que en los juicios sobre filiación será admisible la investigación de la paternidad y de la maternidad mediante toda clase de pruebas, incluidas las biológicas.

Mi mandante está dispuesto y se ofrece a dichas pruebas, en primer lugar porque no duda de su propia paternidad y en segundo lugar por la fiabilidad de las mismas y su aceptación por la doctrina legal, que las ha considerado fiables en alto grado: 99,98% [SSTS de 12 de noviembre de 1987 ) o 3 de diciembre de 1988 ].

Para el supuesto de que la parte demandada no se aviniere a dicha prueba biológica, y que nada tiene de inviable por la muerte, toda vez que no ha desaparecido el cuerpo, habrá que conjugar dicha negativa con los otros medios de prueba aportados, teniendo en cuenta que la negativa a dichas pruebas biológicas, aunque no es base para derivar automáticamente un reconocimiento ficticio, es prueba presuntiva ‘ad hominem’ positivizada en art. 767.4 LEC, en caso como el presente en que median otros variados y poderosos indicios de la paternidad, como es la convivencia con la madre en la época de la concepción, que expresamente menciona el art. 767.3 LEC (doctrina constitucional de STC 7/94, Rec. 1407/1992 y STC 276/96, Rec. 4443/1995 y jurisprudencia de STS de 29 de marzo, 14 de junio, Rec. 3214/1992 y STS 24 de octubre de 1996, Rec. 3902/1992).

VII.- COSTAS.

No hay salvedad legal al principio objetivista del vencimiento en este género de procesos, debiéndose aplicar conforme a las reglas del art. 394 LEC.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con sus copias y documentos que lo acompañan, se sirva admitir uno y otros, tenga por interpuesta la demanda de reclamación de filiación extramatrimonial sin que existiera posesión de estado y acumulada impugnación de filiación legalmente determinada, y sustanciándola, con intervención del Ministerio Fiscal, por los trámites de juicio declarativo especial, se venga a dictar sentencia por la que se declare que el demandante era padre extramatrimonial del difunto menor D. [NOMBRE Y APELLIDOS], procediéndose a practicar la correspondiente inscripción en el Registro Civil; con expresa imposición de las costas a demandado que se opusiere.

Es de Justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO: Que por necesitar para otros usos la copia de escritura de poder acreditativa de la representación del suscrito Procurador, intereso y

SUPLICO AL TRIBUNAL. Se sirva acordar su desglose y devolución a esta parte, dejando en autos testimonio de la misma.

Reitero Justicia en lugar y fecha ‘ut supra’.

Firma del Abogado/a	Firma del Procurador/a

========================================================================
