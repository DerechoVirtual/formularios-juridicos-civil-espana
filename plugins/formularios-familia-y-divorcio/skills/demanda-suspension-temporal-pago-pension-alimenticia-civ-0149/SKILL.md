---
name: demanda-suspension-temporal-pago-pension-alimenticia-civ-0149
description: "Demanda de suspensión temporal del pago de la pensión alimenticia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de suspensión temporal del pago de la pensión alimenticia

> Formulario **CIV-0149** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de suspensión temporal del pago de la pensión alimenticia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de suspensión temporal del pago de la pensión alimenticia” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-suspension-temporal-pago-pension-alimenticia-civ-0149`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] IMPORTE (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] SEDE (4 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] CALLE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] COLEGIO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] Nº
- [ ] PROFESIÓN

## Normas que cita el formulario

- art. 250.1.8 LEC
- art. 6 LEC
- art. 10 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 146 CC
- art. 394 LEC
- art. 253 LEC
- art. 251.7 LEC

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

- Junto a «…A, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…cida en sentencia dictada por el Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], comparezco en este TRIBUNAL con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, interpongo DEMANDA DE JUICIO VERBAL, en solicitud de SUSPENSIÓN TEMPORAL DE LA OBLIGACIÓN DE PAGO DE LA PENSIÓN ALIMENTICIA EN FAVOR DE HIJO MAYOR DE EDAD (debe tenerse en cuenta que, según jurisprudencia consolidada, si el hijo fuese menor de edad, normalmente no prosperaría la solicitud de suspensión del pago de la pensión, ni siquiera cuando el progenitor se encontrase en paro o sus ingresos se redujesen al mínimo) establecida en sentencia dictada por el Tribunal de Instancia de [SEDE], plaza n.º [Nº] en juicio de alimentos núm. [Nº DE PROCEDIMIENTO]/[AÑO], contra D./Dª [NOMBRE Y APELLIDOS], mayor de edad, con domicilio a efectos de citación y emplazamiento en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta.. La presente demanda se basa en los siguientes

HECHOS

PRIMERO.- En fecha [DÍA] de [MES] de [AÑO], se dictó por el Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO], sentencia en el seno del procedimiento núm. [Nº DE PROCEDIMIENTO]/[AÑO], en la que se condenó a mi representado/a a satisfacer una pensión de alimentos en favor de su hijo/a mayor de edad, D./Dª [NOMBRE Y APELLIDOS], por cuantía de [IMPORTE] euros ( €) mensuales.

Se acompaña testimonio de la citada sentencia, en el que consta su firmeza, como DOCUMENTO Nº [Nº DE DOCUMENTO]

SEGUNDO.- Desde que se dictó la citada sentencia se ha producido una alteración sustancial de las circunstancias que se tuvieron en cuenta para fijar la referida pensión de alimentos. Ello es resultado de haber perdido mi representado/a el puesto de trabajo fijo que tenía, como consecuencia de un expediente de regulación de empleo en la empresa donde prestaba sus servicios, entrando en situación de paro laboral, sin que el subsidio de desempleo que cobra, de [IMPORTE] euros ( €) mensuales baste, ni siquiera, parta cubrir sus propias necesidades. Además, la citada empresa ha incumplido los compromisos económicos contraídos con los afectados.

Se acompaña como DOCUMENTO Nº certificado expedido por el INEM acreditativo de las percepciones económicas de mi representado/a, y se dejan señalados los archivos de la Sección de lo Social del Tribunal de Instancia de [SEDE], plaza n.º esta ciudad, donde se tramita el expediente de regulación de empleo y extinción de las relaciones laborales.

TERCERO.- Los hechos anteriores inciden directamente en la capacidad económica de mi representado.

Por otra parte, su hijo, mayor de edad, es joven y capaz de buscar un empleo.

Por ello, se solicita la suspensión de la obligación de satisfacer la pensión de alimentos en favor del hijo mayor de edad mientras dure la situación de paro laboral de mi representado/a.

CUARTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

I. JURISDICCIÓN.- Es competente la jurisdicción civil, de acuerdo con lo establecido en los arts. 9.2, 21.1 y 22 ter/quater Ley Orgánica del Poder Judicial en relación con el art. 36 de la Ley de Enjuiciamiento Civil.

II. COMPETENCIA.- Es competente el Tribunal al que me dirijo, en virtud de lo establecido en el art. 50 y concordantes de la Ley de Enjuiciamiento Civil.

III. PROCEDIMIENTO.- La presente demanda debe sustanciarse por los trámites del juicio verbal, en virtud de lo dispuesto en el artículo 250.1.8º LEC.

IV. CAPACIDAD.- Ambas partes tienen capacidad para serlo, conforme a lo dispuesto en los artículos 6 y ss LEC.

V. LEGITIMACIÓN.- Están legitimados activa y pasivamente, el/la demandante y el/la demandada, conforme al art. 10 LEC. El primero, como obligado al pago de alimentos por sentencia firme y, el segundo, como beneficiario de los mismos, de acuerdo con los arts. 142 y ss. CC.

VI. REPRESENTACIÓN Y DEFENSA.- El/La demandante comparece representado y defendido, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en los artículos 23.1 y 31.1 LEC.

VII. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII. DERECHO SUSTANTIVO.- Los arts. 142 y ss del Código civil, que regulan la obligación legal de alimentos; en especial los arts. 146 y 147 CC.

De la exposición fáctica se desprende que se ha producido una alteración sustancial de las circunstancias económicas de mi representado/a en comparación con las que se tuvieron en cuenta al fijar el montante de la pensión que, al menos temporalmente, le impide hacer frente al pago de la pensión alimenticia en favor del demandado que, aunque hijo suyo, es mayor de edad y no se encuentra en peor situación económica que mi mandante, ni en cuanto a los ingresos de que dispone, ni en relación a sus posibilidades de encontrar medios con los que atender a sus necesidades.

Puede citarse jurisprudencia para reforzar los argumentos legales.

IX. COSTAS.- Procede imponerlas a la parte cuyas pretensiones hubieran sido totalmente rechazadas, en virtud de lo dispuesto en el art. 394 LEC.

Por lo expuesto

SUPLICO AL TRIBUNAL:

Que tras admitir este escrito con los documentos que lo acompañan y sus copias, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta DEMANDA DE JUICIO VERBAL contra D./Dª [NOMBRE Y APELLIDOS], PARA LA SUSPENSIÓN DEL PAGO DE LA PENSIÓN DE ALIMENTOS impuesta en sentencia dictada por el Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO], en fecha [DÍA] de [MES] de [AÑO], en procedimiento núm. [Nº DE PROCEDIMIENTO]/[AÑO]; y, previos los trámites legales que procedan, dicte resolución por la que se acuerde la suspensión del pago de la citada pensión, al menos mientras persista la situación de desempleo de mi representado/a y no recupere la capacidad económica con que contaba en el momento de fijarse aquélla pensión; o, subsidiariamente, de no estimarse esta pretensión, que se reduzca el montante de la pensión alimenticia a [IMPORTE] euros ( €) mensuales, para corregir el desequilibrio producido por la sustancial alteración de las circunstancias que se tuvieron en cuenta en el momento de establecer la pensión.

OTROSÍ DIGO.- En cumplimiento de lo dispuesto en el art. 253 LEC, esta parte fija la cuantía del procedimiento, calculada de acuerdo con lo dispuesto en el art. 251.7 LEC en [IMPORTE] euros.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
