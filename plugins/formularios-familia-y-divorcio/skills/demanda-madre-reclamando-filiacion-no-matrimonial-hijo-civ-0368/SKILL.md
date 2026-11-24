---
name: demanda-madre-reclamando-filiacion-no-matrimonial-hijo-civ-0368
description: "Demanda de la madre reclamando filiación no matrimonial del hijo menor sin posesión de estado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de la madre reclamando filiación no matrimonial del hijo menor sin posesión de estado

> Formulario **CIV-0368** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda en reclamación de determinación de filiación no matrimonial, sin posesión de estado, interpuesta por la madre del hijo menor de edad.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de la madre reclamando filiación no matrimonial del hijo menor sin posesión de estado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de la madre reclamando filiación no matrimonial del hijo menor sin posesión de estado” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-madre-reclamando-filiacion-no-matrimonial-hijo-civ-0368`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (9 veces)
- [ ] NÚMERO (9 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] FECHA (5 veces)
- [ ] CALLE (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] CARGO (2 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] COLEGIO
- [ ] ENTIDAD BANCARIA
- [ ] LUGAR
- [ ] Nº DE CUENTA (IBAN)
- [ ] PLAZO
- [ ] SEDE

## Normas que cita el formulario

- art. 7.1 LEC
- art. 154 CC
- art. 133 CC
- art. 766 LEC
- art. 765 LEC
- art. 749.1 LEC
- art. 753 LEC
- art. 767 LEC
- art. 767.1 LEC
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

- Junto a «…FANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…2666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de Dña. [NOMBRE Y APELLIDOS], provista de D.N.I. n.º [NÚMERO], y domiciliada en esta ciudad, calle [CALLE], n.º [NÚMERO], que actúa como representante legal de su hijo menor [NOMBRE Y APELLIDOS], según acredito mediante poder telemáctico especial para pleitos que acompaño mediante copia auténtica y su reproducción, con ruego de que se testimonie en autos la segunda y se devuelva la copia, por necesitarla para otros usos, dirigida por el Letrado suscrito D./Dña. [NOMBRE Y APELLIDOS], ejerciente en el Iltre. Colegio de Abogados de [COLEGIO], con despacho abierto en [LOCALIDAD], calle [CALLE], n.º [NÚMERO], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito vengo a formular demanda en reclamación de determinación de filiación frente a D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], n.º [NÚMERO] y frente al Ministerio Fiscal, en base a los siguientes datos y argumentos:

HECHOS

PRIMERO.- Mi patrocinada y el hoy demandado D./Dña. [NOMBRE Y APELLIDOS], se conocieron en [LOCALIDAD], cuando ambos fueron destinados, la primera como [CARGO], y como [CARGO] el segundo en [LOCALIDAD], entablándose entre ellos amistad íntima, fruto de haber sido compañeros de la Facultad de Derecho de [LOCALIDAD], y de la coincidencia cotidiana, por compartir, inicialmente con otras dos personas, el inquilinato de la residencia temporal en la población, y alejados por razones laborales de su hasta entonces entorno familiar y social propio.

De dicha amistad derivó una relación amorosa que arrancó desde [FECHA] hasta hace aproximadamente siete meses en que, por divergencias surgidas entre ambos, se puso tempestuosamente fin a la misma, urgiéndose el traslado del demandado a su actual destino.

Durante el indicado tiempo han convivido en relación afectiva semejante al de las parejas casadas en la vivienda sita en calle [CALLE], n.º [NÚMERO] de [LOCALIDAD]

A la demostración de estos hechos se acompañan, como documentos nos. a [Nº DE DOCUMENTO], diversas cartas manuscritas del demandado dirigidas a la actora; como documentos [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO] dos juegos de fotografías de señaladas ocasiones; como documento n.º [NÚMERO], copia del contrato de arrendamiento de vivienda; como documentos nos. y [Nº DE DOCUMENTO], certificación de la entidad bancaria [ENTIDAD BANCARIA], de cotitularidad de la cuenta corriente [Nº DE CUENTA (IBAN)], y de la petición de consuno del crédito personal n.º [NÚMERO] de fecha [FECHA], etc)

SEGUNDO.- Cuando finalizaron las relaciones con mi mandante, el demandado D./Dña. [NOMBRE Y APELLIDOS] abandonó el domicilio de convivencia y se trasladó a nuevo empleo en [LOCALIDAD], habiendo entablado fulgurante relación con otra mujer que ha derivado en matrimonio, contraído en [LOCALIDAD], hace escasas fechas, el [FECHA] (se adjunta certificación del Registro Civil que lo acredita, como documento n.º [NÚMERO]).

TERCERO.- Al cabo de [PLAZO], ha nacido el hijo menor de mi patrocinada, al que se puso de nombre [NOMBRE Y APELLIDOS], y ha sido inscrito en el Registro Civil de [LOCALIDAD], según se demuestra con la certificación que se acompaña como documento n.º [NÚMERO].

CUARTO.- El menor [NOMBRE DEL MENOR], en cuya representación comparece la demandante es hijo del demandado, según el mismo no ignora, si bien ni siquiera ha concedido acceder a verle, resultando infructuosos los términos pacíficos de conseguir un reconocimiento, siquiera prescindiendo de innecesarios compromisos económicos por parte del padre.

Para acreditar estos asertos son anexos a este escrito la misiva enviada por mi mandante en fecha [FECHA] —documento n.º — y la contestación epistolar que cursó el demandado -documento n.º —.

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Es el orden civil de la Jurisdicción quien tiene confiada la competencia genérica para la tutela judicial del estado civil, y por ende, el conocimiento de las acciones de filiación, y corresponde la competencia objetiva y geográfica la Sección Civil del Tribunal de Instancia de esta circunscripción que por turno de reparto corresponda, conforme a los arts. 45 y 50.1 LEC, habida cuenta que se ejercita una pretensión que fija proceso por materia —no por cuantía— y que el fuero territorial general, a falta de prevención legal especial que aquí no se da, para las personas físicas, es el domicilio del demandado.

II.- CAPACIDAD Y LEGITIMACIÓN.

Todos los intervinientes detentan capacidad para ser parte, en cuanto que son personas físicas y la detenta siempre el Ministerio Fiscal cuando le asigna un papel procesal la ley (arts. 6.1.1.º y 6.º), y la falta de capacidad de obrar y procesal del menor [NOMBRE DEL MENOR], se suple con la representación de su madre, titular de la patria potestad (art. 7.1 y 2 LEC en relación con el art. 154 CCiv).

El hijo está legitimado activamente para reclamar la filiación no matrimonial sin posesión de estado, de acuerdo con el art. 133 CCiv, siendo que la acción no prescribe durante toda la vida del que se pretende hijo, como lo está pasivamente aquel a quien se atribuye la condición de padre (art. 766 LEC); correspondiendo la acción al hijo menor de edad, es ejercida por su madre, su representante legal, conforme al art. 765 LEC; el Ministerio Fiscal está legitimado de manera extraordinaria (art. 10 párrafo 2.º LEC), por aplicación del art. 749.1 LEC.

III.- PROCEDIMIENTO.

Con arreglo al art. 753 LEC, el proceso asignado para conocimiento de las acciones de filiación, es el juicio especial verbal con contestación escrita del Título I del Libro IV LEC, con sus matices de los arts. 767 y 768 LEC.

IV.- PRINCIPIO DE PRUEBA.

Se cumple la exigencia del art. 767.1 LEC, en cuanto que se presenta principio de prueba de los hechos en que se funda la demanda, en el sentido de abono de la seriedad del derecho en cuanto al fondo de la pretensión que se ejercita, como así se entiende resultan los documentos aportados, que acreditan la convivencia permanente de los progenitores durante el tiempo de la concepción, al cálculo biológico desde el día cierto de nacimiento del hijo.

V.- FONDO DEL ASUNTO.

El ámbito de este proceso es el coherente con la viabilidad amplísima —sólo vedada por el respeto a la cosa juzgada material— de solicitar de los tribunales la determinación legal de la filiación, informándose nuestro sistema jurídico por la indisponibilidad del objeto de una pretensión de filiación y la búsqueda de oficio de la verdad de la procreación, que autoriza unas facultades de relativa inquisición a los Jueces.

El art. 767.2 LEC establece que en los juicios sobre filiación será admisible la investigación de la paternidad y de la maternidad mediante toda clase de pruebas, incluidas las biológicas, que se entroniza como prueba hegemónica en este tipo de juicios.

Mi mandante solicitará la prueba heredo-biológica de la paternidad del demandado, en primer lugar porque no duda de la misma, y en segundo lugar, por su fiabilidad científica, y su aceptación por la doctrina legal (SSTS de 5 de noviembre de 1987) y 3 de diciembre de 1988).

Para el supuesto de que la parte demandada no se aviniere a dicha prueba biológica, habrá que conjugar dicha negativa con los otros medios de prueba aportados, teniendo en cuenta que la negativa a dichas pruebas biológicas, aunque no es base para derivar automáticamente un reconocimiento ficticio, es prueba presuntiva ‘ad hominem’ positivizada en el art. 767.4 LEC, en caso como el presente en que median otros variados y poderosos indicios de la paternidad, como es la convivencia con la madre en la época de la concepción, que expresamente menciona el art. 767.3 LEC (doctrina constitucional de STC 7/1994 y ATC 276/1996, y jurisprudencia de STS de 24 de octubre de 1996, rec. 3902/1992).

VI.- COSTAS.

El principio cuasiobjetivo del vencimiento expresado en el art. 394 LEC, no encuentra excepción en este género de pretensiones, por lo que el demandado vencido que se resistiera a la demanda ha de sufragar todas las costas procesales.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con sus copias y documentos que lo acompañan, se sirva admitir uno y otros, tenga por interpuesta la demanda de reclamación de filiación extramatrimonial sin que exista posesión de estado, en ejercicio del derecho del menor en potestad, y sustanciándola, con intervención del Ministerio Fiscal, seguido que sea el proceso por sus regulares trámites, se venga a dictar sentencia por la que se declare que el demandado es padre extramatrimonial del menor, y se practique la correspondiente inscripción en el Registro Civil, con expresa imposición de las costas a la parte demandada.

Es justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO: Que por necesitar para otros usos la copia de escritura de poder acreditativa de la representación del suscrito Procurador, intereso y

SUPLICO AL TRIBUNAL. Se sirva acordar su desglose y devolución a esta parte, dejando en autos testimonio de la misma.

Reitero Justicia en lugar y fecha ‘ut supra’.

Firma del Abogado/a	Firma del Procurador/a

========================================================================
