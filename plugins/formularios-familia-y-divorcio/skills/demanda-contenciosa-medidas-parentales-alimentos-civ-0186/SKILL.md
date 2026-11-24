---
name: demanda-contenciosa-medidas-parentales-alimentos-civ-0186
description: "Demanda contenciosa de medidas parentales, alimentos y vivienda tras ruptura de pareja (Cataluña). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contenciosa de medidas parentales, alimentos y vivienda tras ruptura de pareja (Cataluña)

> Formulario **CIV-0186** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda en procedimiento contencioso sobre adopción de medidas sobre responsabilidades parentales, pensión de alimentos y atribución del uso de la vivienda familiar tras ruptura de unión de hecho conforme a Derecho civil especial de Cataluña, con hijos menores y solicitud de medidas provisionales coetáneas

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contenciosa de medidas parentales, alimentos y vivienda tras ruptura de pareja (Cataluña)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contenciosa de medidas parentales, alimentos y vivienda tras ruptura de pareja (Cataluña)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-contenciosa-medidas-parentales-alimentos-civ-0186`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (9 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] NÚMERO (4 veces)
- [ ] CALLE (3 veces)
- [ ] FECHA (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº DE CUENTA (IBAN) (3 veces)
- [ ] BENEFICIARIO
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] NOMBRE DEL HIJO
- [ ] NOMBRE DEL MENOR
- [ ] PISO
- [ ] PORCENTAJE
- [ ] TOMO

## Normas que cita el formulario

- art. 234 CC
- art. 233 CC
- art. 769.3 LEC
- art. 749.2 LEC
- art. 770 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 394 LEC
- art. 773.1 LEC
- art. 771 LEC
- art. 773.3 LEC

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

- Junto a «…IÓN CIVIL DE [LOCALIDAD] SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DE [LOCALIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

AL TRIBUNAL DE INSTANCIA

SECCIÓN CIVIL DE [LOCALIDAD]

SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de Dña. [NOMBRE Y APELLIDOS] provista de D.N.I. n.º [NÚMERO], con domicilio en esta ciudad, calle [CALLE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo dirección del Letrado D./Dña. [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, siguiendo las instrucciones de mi mandante, vengo a formular DEMANDA CONTENCIOSA DE ADOPCIÓN DE MEDIDAS SOBRE RESPONSABILIDADES PARENTALES, PENSIÓN DE ALIMENTOS Y ATRIBUCIÓN DEL USO DE LA VIVIENDA FAMILIAR TRAS RUPTURA DE UNIÓN DE HECHO, frente a D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], y el Ministerio Fiscal.

La demanda se basa en los siguientes hechos y razonamientos jurídicos:

HECHOS

PRIMERO.- Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS], formaron familia natural desde la fecha [FECHA], en la que iniciaron su relación paramatrimonial con intención de permanencia y consolidación, como se acredita mediante certificación expedida por el Registro Municipal de Uniones Civiles del Ayuntamiento de [LOCALIDAD] que se acompaña como documento n.º [NÚMERO].

SEGUNDO.- Fruto de esta unión nació un hijo, de nombre [NOMBRE DEL HIJO], nacido el [FECHA], inscrito en el Registro Civil de [LOCALIDAD], Libro [LIBRO], Tomo [TOMO], Folio [FOLIO], por consiguiente menor de edad; aparece inscrito como hijo de mis mandantes, según se demuestra con la certificación literal de nacimiento que se acompaña como documento n.º [Nº DE DOCUMENTO]

TERCERO.- El pasado mes de [MES] cesó la convivencia entre mi patrocinada y el hoy demandado D. [NOMBRE Y APELLIDOS], habiendo abandonado este último el domicilio que la pareja venía compartiendo, trasladándose a vivir con sus padres en [LOCALIDAD], que es el domicilio arriba reseñado.

Desde entonces, mi mandante ocupa junto al hijo habido del matrimonio el domicilio familiar, perteneciente en plena propiedad y por mitades indivisas a ambos cónyuges.

Adjunto certificado de empadronamiento y escritura pública de propiedad de la vivienda familiar, donde consta que es propiedad indivisa de ambos por partes iguales (documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]).

CUARTO.- El hijo menor de edad ha estado siempre en compañía de la madre, mi mandante, y es lo conveniente que quede bajo la guarda individual o exclusiva de ella, que ha sido quien ha dedicado toda su vida al cuidado del hogar; y asimismo debe atribuírsele el uso de la vivienda familiar por razón de la guarda del hijo.

De acuerdo con lo establecido en el art. 233-8.2 del Libro II del Código Civil de Cataluña aprobado por Ley 25/2010 de 29 de julio (en adelante, CCC), por remisión del art. 234-7 CCC, se acompaña propuesta de plan de parentalidad para el ejercicio de las responsabilidades parentales con respecto a la guarda, cuidado y educación de los hijos comunes, conforme al art. 233-9 CCC, como documento n.º [Nº DE DOCUMENTO]

QUINTO.- El demandado percibe unos ingresos de [IMPORTE] euros mensuales como trabajador de la empresa [DENOMINACIÓN SOCIAL], mientras que mi representada carece de cualificación profesional de cualquier tipo, por haber dedicado su vida, desde su matrimonio, al cuidado de la casa y de la familia, habiendo tenido que recurrir a la realización de trabajos de empleada de hogar, en forma discontinua, que le han permitido atender las necesidades vitales de sus hijos y los gastos de la casa, con la ayuda de sus padres. Se adjunta, al objeto de demostrar las rentas de la unidad familiar, copias de la declaración -conjunta- del I.R.P.F. del año pasado y el anterior, como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

SEXTO.- Los gastos precisos para la atención de las necesidades ordinarias y extraordinarias del hijo ascienden, aproximadamente, a [IMPORTE] € mensuales, que se desglosan en los siguientes conceptos:

a) Educación:
b) Vestido:
c) Otros gastos:

Se aportan para justificar los gastos referidos los documentos números [Nº DE DOCUMENTO]

Conforme a lo dicho, procede fijar en la cantidad de [IMPORTE] euros mensuales la pensión alimenticia que corresponde pagar al demandado.

Esta pensión se pagará por meses anticipados, dentro de los cinco primeros días de cada mes, mediante ingreso en [Nº DE CUENTA (IBAN)] Para su actualización, deberá estarse a las variaciones que experimenten los índices de precio al consumo, según el Instituto Nacional de Estadística u organismo que le sustituya, y a los posibles aumentos de sueldo que obtuviera el demandado (se indicará su periodicidad, modalidad de pago, criterios de actualización y, en su caso, garantías para su pago).

SÉPTIMO.- Por todo el relato fáctico expuesto, una vez finalizada formalmente la relación afectiva, conforme a lo establecido por el art. 234-4-1a) CCC y puesto que han resultado infructuosos todos los intentos pacíficos de solucionar la situación ante las continuas promesas incumplidas por el demandado, interesa al derecho de mi mandante, garantizar el ejercicio de la guarda y custodia de su hija menor, dada la irregular situación familiar planteada y el perjuicio que se le pueda irrogar en su desarrollo afectivo y emocional, y garantizar los derechos económicos que le asisten, viéndose obligada a la interposición de esta demanda ante la negativa del demandado a abonar cantidad alguna en este concepto.

OCTAVO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Conforme a lo establecido en el art. 769.3 LEC(en su caso, en relación con el artículo 1.2 del RD 1322/81 de 3 de julio) como fuero de competencia territorial se fija la circunscripción del Juez competente para conocer del proceso en el partido del último domicilio común de los progenitores.

II.- PARTES.

Mis representados se hallan legitimados por haber formado parte de la unión de hecho y en su condición de padres del menor, habida cuenta que son los que se hallan en la situación jurídica respectiva del derecho-deber de velar por los hijos menores no emancipados y alimentarlos (arts. 236-1 y 236-17.1 CCC).

Con arreglo al art. 749.2 LEC, deberá ser parte el Ministerio Fiscal, por existir hijos menores.

III.- PROCEDIMIENTO.

En cuanto al procedimiento a seguir, resulta de aplicación el trámite previsto en el art. 770 LEC, en virtud de la remisión que establece la DA 5.ª CCC.

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- FONDO DE LA PRETENSIÓN.

El art. 234-7 CCC regula el ejercicio de la guarda de los hijos y relaciones personales tras la extinción de la pareja estable, con remisión a los genéricos arts. 233-8 a 233-13 CCC sobre las relaciones parentales tras las rupturas matrimoniales.

Respecto a la atribución del uso de la vivienda familiar, rige lo dispuesto en el art. 234-8 que se remite a su vez a lo establecido en los apartados 6.º y 7.º del art. 233-20 y los arts. 233-21 a 233-25.

VI.- COSTAS.

Las costas procesales deben ser impuestas a la parte demandada, por criterio del íntegro vencimiento, en atención al art. 394 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, tenerme por comparecido y parte en la representación que ostento, y seguido que sea el procedimiento por sus pertinentes trámites, con citación del Ministerio Fiscal, se sirva dictar Sentencia por la que, estimando la presente demanda, reconociendo la ruptura de la pareja estable existente hasta ahora entre las partes, se acuerden los siguientes efectos:

1.- Atribución de la guarda individual del hijo menor [NOMBRE DEL MENOR] a la demandante, conforme al plan de parentalidad para el ejercicio de las responsabilidades parentales propuesto por esta parte.
2.- Atribución del uso exclusivo de la vivienda familiar sita en la calle [CALLE], n.º [NÚMERO], piso [PISO], a la demandante y a su hijo menor, así como del ajuar doméstico en ella existente.
3.- Establecimiento de una pensión alimenticia, a favor de [BENEFICIARIO] de euros mensuales, a cargo del demandado D. [NOMBRE Y APELLIDOS], pagadera por meses anticipados, mediante ingreso en la cuenta corriente [Nº DE CUENTA (IBAN)], y actualizable anualmente conforme a las variaciones que experimente el Índice de Precios al Consumo que publique el Instituto Nacional de Estadística, u organismo oficial que lo sustituya.

En todo caso, se pronuncie el reintegro de las costas con cargo a la parte demandada, si se opusiere.

Es justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO: Que al amparo del art. 773.1 LEC, y del art. 233-1 CCC, no habiéndose adoptado con anterioridad, se solicitan mediante el presente escrito MEDIDAS PROVISIONALES coetáneas a la admisión de la demanda, en base a los siguientes:

HECHOS

PRIMERO.- El hijo menor común de la pareja ha permanecido siempre en compañía de la madre, y es lo conveniente que continúe con ella, habida cuenta de su edad y las circunstancias que rodean a la presente ruptura, pareciendo suficiente la fijación de un derecho provisional de comunicación y estancia sin pernocta del padre con su hijo, en casa de los abuelos donde éste reside, los sábados de todas las semanas de diez a veinte horas, por lo menos hasta la resolución definitiva.

SEGUNDO.- Puesto que el interés familiar más necesitado de protección es el del hijo en potestad, tanto él como mi representada deben continuar en el uso de la vivienda familiar.

TERCERO.- Como quiera que mi representada carece de ingresos estables o de bienes rentables, constituyendo las fuentes del activo familiar el sueldo como trabajador por cuenta ajena del demandado, es necesaria su aportación con el [PORCENTAJE] % para hacer frente a los gastos familiares, toda vez que el demandado vive con sus padres, que gozan de asentada posición.

La dicha cantidad debiera ser directamente ingresada en la cuenta bancaria [Nº DE CUENTA (IBAN)], habida cuenta que todos los datos apuntan que el cumplimiento voluntario no es verosímil que se produzca, y en evitación de dilaciones y diligencias ejecutivas inútiles.

FUNDAMENTOS DE DERECHO

I.- El procedimiento adecuado es el del art. 771 LEC para medidas previas, conforme remisión del art. 773.3 LEC, en relación al art. 233-1 y DA 5.ª CCC.

II.- Esta pretensión consiste en la adopción de los efectos "ope legis"del art. 233-1.5 y medidas del art. 233-1.1 CCC, de cognición judicial, derivados de la tutela cautelar por la lesión que, de no adoptarse, pueden padecer las partes y los hijos menores, por la duración del proceso.

En su virtud,

SUPLICO AL TRIBUNAL

que, teniendo por causadas las precedentes manifestaciones a los efectos oportunos, y por deducida solicitud de adopción de medidas provisionales, seguido que sea su pertinente trámite, se dicte Auto por el que se aprueben las siguientes:

1.º Por lo que respecta a la forma en que el hijo debe convivir con los padres y debe relacionarse con aquél con quien no estén conviviendo:
2.º En cuanto a la forma en que debe ejercerse la potestad sobre el hijo:
3.º Respecto a la distribución del deber de alimentos en favor del hijo:

Reitero Justicia en lugar y fecha "ut supra".

Firma del Abogado/a	Firma del Procurador/a

========================================================================
