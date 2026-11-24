---
name: demanda-nulidad-matrimonial-error-identidad-cualidades-civ-0331
description: "Demanda de nulidad matrimonial por error en la identidad o cualidades del cónyuge, con indemnización. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de nulidad matrimonial por error en la identidad o cualidades del cónyuge, con indemnización

> Formulario **CIV-0331** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de nulidad de matrimonio por error en la identidad de la persona del otro contrayente o en las cualidades personales del otro cónyuge determinantes de la prestación del consentimiento, con solicitud de indemnización compensatoria para el cónyuge de buena fe.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de nulidad matrimonial por error en la identidad o cualidades del cónyuge, con indemnización» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de nulidad matrimonial por error en la identidad o cualidades del cónyuge, con indemnización” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-nulidad-matrimonial-error-identidad-cualidades-civ-0331`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] NÚMERO (5 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] CALLE (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] AÑOS
- [ ] CARRERA UNIVERSITARIA
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] IMPORTE EN CIFRA
- [ ] LUGAR

## Normas que cita el formulario

- art. 73.4.ª CC
- art. 770 LEC
- art. 74 CC
- art. 76 CC
- art. 749.1 LEC
- art. 251 LEC
- art. 252 LEC
- art. 76 Código Civil
- art. 4.1 LO 1/2025
- art. 73 Código Civil
- art. 98 CC
- art. 97 CC
- art. 97.2 CC
- art. 97.8 CC
- art. 755 LEC
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

- Junto a «…ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [LOCALIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

SOLICITUD DE INDEMNIZACIÓN COMPENSATORIA PARA EL CÓNYUGE DE BUENA FE

AL TRIBUNAL DE INSTANCIA [ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de Dña. [NOMBRE Y APELLIDOS], provista de D.N.I. n.º [NÚMERO], con domicilio en [LOCALIDAD], calle [CALLE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo dirección de la Letrada D./Dña. [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [DIRECCIÓN], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, siguiendo la instrucción de mi mandante, vengo a formular demanda de NULIDAD DE MATRIMONIO frente a su esposo D. [NOMBRE Y APELLIDOS], con domicilio actual en [DOMICILIO], y frente al MINISTERIO FISCAL, ejercitando acción por causa prevista en el art. 73.4.ª CCiv, y con base a los siguientes datos y argumentos:

HECHOS

PRIMERO.- Mi representada contrajo matrimonio civil con D. [NOMBRE Y APELLIDOS], el [FECHA], en la localidad de [LOCALIDAD], inscrito en el Registro Civil de [LOCALIDAD], según certificación de matrimonio que se acompaña como documento n.º [NÚMERO].

SEGUNDO.- De dicho matrimonio no ha habido descendencia, toda vez que su matrimonio no ha podido consumarse por incapacidad del demandado. Se acompaña certificación médica del facultativo D. [NOMBRE Y APELLIDOS] como documento n.º [NÚMERO].

TERCERO.- Habiendo consultado mi representada a distintos especialistas, todos coinciden en la imposibilidad de consumar su matrimonio, debido a la enfermedad que padece su esposo y que no conoció hasta después del matrimonio, ya que la misma provenía de la infancia del demandado.

Que dicha enfermedad ya la padecía el cónyuge demandado antes de contraer matrimonio, aunque no informó de ella a mi mandante, se acredita con los certificados médicos a los que mi patrocinada ha tenido acceso, y que se aportan como documentos núms. y [Nº DE DOCUMENTO], y en los que se prueba que el demandado padecía la enfermedad desde su infancia. Este hecho fue también ocultado a mi mandante por los familiares más allegados a su esposo.

Y como consecuencia fue celebrado este matrimonio por error en la identidad de la persona del demandado, en cuanto a la apreciación de las cualidades de su esposo que son causa determinante en la prestación del consentimiento.

CUARTO.- Mi mandante siempre ha actuado de buena fe, creyendo sinceramente que el matrimonio era válido, hasta que se le ha desengañado recientemente.

Siendo estudiante universitaria de la carrera de [CARRERA UNIVERSITARIA], interrumpió sus estudios por razón de casarse con el demandado, careciendo de rentas o patrimonio privativo, mientras que éste goza de una holgada posición económica. Resulta el demandado administrador y gerente de la empresa [DENOMINACIÓN SOCIAL], sita en [LOCALIDAD], dedicada a la fabricación de plástico (Se acompaña copia simple de las inscripciones correspondientes a la citada mercantil en el Registro Mercantil de [LOCALIDAD], donde aparece la escritura fundacional y las autoliquidaciones de Impuesto de Sucesiones de los años [AÑOS], documento n.º [NÚMERO]), y es titular de varios inmuebles (Se adjuntan también copias simples de las inscripciones en el Registro de la Propiedad de tres fincas, documentos núms. a [Nº DE DOCUMENTO]).

FUNDAMENTOS DE DERECHO

I.- Es competente el Tribunal de Instancia del lugar del último domicilio del matrimonio, conforme al art. 769.1.pfo.1.º LEC.

II.- El procedimiento adecuado es el del art. 770 LEC, para conocer de las demandas de nulidad del matrimonio.

III.- Mi mandante ostenta la capacidad procesal necesaria, conforme al artículo 6.1.1.º de la Ley de Enjuiciamiento Civil.

IV.- Tienen legitimación ordinaria por hallarse en la situación jurídica de relación matrimonial ambos cónyuges (arts. 74 CCiv en relación con art. 76 CCiv; y 10.1 LEC), siendo el objeto de la pretensión la declaración de nulidad del vínculo, y la tiene extraordinaria por interés público, como interviniente, el Ministerio Fiscal (art. 749.1 LEC).

V.- Mi mandante comparece representada por Procurador legalmente habilitado para actuar ante este Tribunal, y asistida por Abogado, conforme a lo dispuesto en el artículo 750.1 de la Ley de Enjuiciamiento Civil.

VI.- Se fija la cuantía de la demanda, en lo que tiene de estimable, por razón de la pretensión de medida definitiva de indemnización pecuniaria, acumulada a la declaración de nulidad vincular, en [IMPORTE] euros, en armonía con la regla 1.ª del art. 251 LEC y la regla 2.ª del art. 252 LEC.

VII.- Se interpone esta demanda dentro del plazo legalmente previsto en el artículo 76 del Código Civil, toda vez que no ha pasado un año de la celebración del matrimonio, y durante ese tiempo se ha podido constatar la enfermedad del demandado.

VIII.- La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional por tratarse de materias excluidas del requisito de procedibilidad de acuerdo con el art. 4.1 II LO 1/2025, entre las cuales se encuentra la nulidad matrimonial, en cuanto se trata de cuestión indisponible por las partes, siendo que la nulidad no depende de la voluntad de los cónyuges.

IX.- El fondo de la pretensión consiste en la declaración de nulidad del matrimonio, a instancia del cónyuge de buena fe, por concurrir la causa legal del art 73 del Código Civil apartado 4.º, al existir error de identidad que en su día hubiera determinado la no prestación del consentimiento.

X.- Se solicita, conforme al art. 98 CCiv, indemnización a favor de mi patrocinada del demandado, por relación a los criterios de la pensión compensatoria del art. 97 CCiv, que no tiene una naturaleza alimenticia, sino que se trata de una equitativa reparación económica equilibradora de los amplios y variados desajustes que puede ocasionar la nulidad del matrimonio, en los planos patrimonial y social, de los que estuvieron unidos en matrimonio [STS de 10 de marzo de 1992 ].

Teniendo en cuenta los criterios legales, ha de resaltarse que mi representada suscribió, a invitación del demandado, capitulaciones prenupciales que instauraron para el matrimonio la separación absoluta de bienes, por lo que, sin patrimonio común que dividir, la desaparición del vínculo representa para la misma, carente de toda renta, una distancia económica y de posición social con la del demandado, y con la que gozaba de casada, que hay obligación legal -restañadora, sin matiz sancionador por culpa- de reducir con una indemnización. Por lo que toca a su cuantía, se tiene en cuenta que el futuro laboral de mi patrocinada es oscuro, y precisamente por carecer de cualificación que hubiera derivado de sus estudios, si no se hubieran interumpido por causa del matrimonio simulado por el demandado (art. 97.2º CCiv), además del notable caudal y medios económicos de éste, al lado de las evidentes necesidades de la demandante (art. 97.8º CCiv).

Se menciona, en punto a la inscripción en el Registro Civil, el art. 755 LEC que autoriza inscribir de oficio las sentencias de nulidad y el artículo 260 del Reglamento del Registro Civil, aplicable por analogía, y que señala los requisitos necesarios para la inscripción.

XI.- Por aplicación del principio del vencimiento en punto a las costas procesales (art. 394 LEC), se debe condenar al demandado si se resiste a la demanda, dado que el obtener la razón precisando de un proceso no ha de suponer una merma patrimonial del que tiene razón.

Y demás normas y jurisprudencia de general y pertinente aplicación.

Por todo cuanto antecede,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, tenerme por comparecida y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, seguido que sea el oportuno procedimiento, se dicte en su día sentencia por la que se declare la nulidad del matrimonio de D. y Dña. [NOMBRE Y APELLIDOS], oficiándose al Registro Civil de [LOCALIDAD] para la anotación de su parte dispositiva en la inscripción correspondiente, y se acuerde el establecimiento de una indemnización compensatoria a favor de la demandante de [IMPORTE] EUROS ([IMPORTE EN CIFRA] €), a cargo del demandado, así como su condena en todas las costas del juicio.

Es Justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
