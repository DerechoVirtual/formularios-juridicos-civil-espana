---
name: demanda-juicio-ordinario-reclamar-derechos-sobre-civ-0082
description: "Demanda de juicio ordinario para reclamar derechos sobre bienes adjudicados como privativos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para reclamar derechos sobre bienes adjudicados como privativos

> Formulario **CIV-0082** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para reclamar derechos sobre bienes adjudicados como privativos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para reclamar derechos sobre bienes adjudicados como privativos” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-juicio-ordinario-reclamar-derechos-sobre-civ-0082`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] Nº (6 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] SEDE (4 veces)
- [ ] CALLE (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] TIPO Y Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] C.P.
- [ ] COLEGIO
- [ ] DÍA
- [ ] ENTIDAD BANCARIA
- [ ] FECHA
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] Nº DE COLEGIADO
- [ ] Nº DE COLEGIADO/A
- [ ] Nº REGISTRAL
- [ ] NÚMERO DE LA CALLE
- [ ] OTROS DATOS
- [ ] PISO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 253 LEC
- art. 5 Ley Orgánica 1/2025
- art. 399 LEC
- art. 348 Código Civil

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…matrimonial, que se siguió en el Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, con número de colegiado [Nº DE COLEGIADO/A] en representación de D./Dña. [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], con la dirección letrada del Abogado/a don./dña. perteneciente al Ilustre Colegio de Abogados de [COLEGIO] con el número [NÚMERO] ante el Tribunal comparezco y DIGO:

Que, por medio del presente escrito, formulo DEMANDA DE JUICIO ORDINARIO contra Don [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], núm. [Nº], piso [PISO], CP [C.P.], para hacer valer los derechos que a mi representada corresponden sobre un inmueble, cuyo valor es de [IMPORTE] euros, incluido indebidamente en la liquidación de la sociedad legal de gananciales disuelta que existió entre la demandante y el demandado.

Se basa la presente demanda en los siguientes,

HECHOS

PRIMERO Firme la disolución de la sociedad de gananciales que existía entre mi representada y el demandado, este último instó procedimiento para la liquidación de su régimen económico matrimonial, que se siguió en el Tribunal de Instancia de [SEDE], plaza n.º [Nº] [OTROS DATOS] con el número de autos

Terminó el procedimiento con la Sentencia, cuyo testimonio acompaño como Documento núm. 1.

En dicha Sentencia, a pesar de las alegaciones y acreditaciones de mi representada, se incluye como bien ganancial, que figura en el número [NÚMERO] del inventario, el siguiente inmueble:

Vivienda sita en la localidad de [LOCALIDAD] núm. [Nº] de la calle [CALLE], de [LOCALIDAD] con una superficie construida de [Nº] metros cuadrados.

Datos Registrales: finca núm. [Nº REGISTRAL]

SEGUNDO La casa descrita en el hecho anterior fue adquirida por mi representada, doña [NOMBRE Y APELLIDOS], en fecha [FECHA], por escritura que se acompaña como Documento núm. 2, con dinero de carácter privativo.

TERCERO Las pruebas de que el bien fue adquirido con fondos privativos de mi representada, son:

El pago se hizo mediante [ÓRGANO] cheques que fueron cargados en la cuenta corriente de mi representada, según certificado expedido por el Banco [ENTIDAD BANCARIA], que incluye fotocopias de los cheques atendidos, y que acompaño como Documento núm. 3.

Es evidente, pues, que los fondos empleados para la compra de tal inmueble eran donados a mi representada y, por ende, de carácter privativo. Y, por tanto, el bien adquirido con ellos, es decir, el inmueble descrito en el hecho primero, incluido en el inventario del procedimiento para la liquidación del régimen económico matrimonial de mi representada, que se siguió en el Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO] con el número de autos [TIPO Y Nº DE PROCEDIMIENTO], y cuya Sentencia se aporta como documento núm. [Nº DE DOCUMENTO]

Acompaño también, como Documentos núms., la liquidación del Impuesto sobre Transmisiones Patrimoniales y las facturas de Notario y Registro de la Propiedad, que coinciden con las cifras de los cheques librados contra la cuenta de mi representada.

CUARTO Queda acreditado, y se insistirá en ello en la fase probatoria, que el inmueble descrito en el hecho primero, no debe estar incluido en la liquidación de gananciales de mi representada con don [NOMBRE Y APELLIDOS], porque se trata de bien privativo, y así debe declararlo este Tribunal, por lo que habrá de omitirse en la liquidación de la sociedad de gananciales que unió la economía de demandante y demandado, cuya liquidación habrá de ser recalculada sin el importe de la partida del inventario correspondiente y manteniendo en lo demás las bases señaladas en la Sentencia recaída en autos [TIPO Y Nº DE PROCEDIMIENTO], del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO DE LA CALLE]

QUINTO En cumplimiento del artículo 253 LECiv, se fija la cuantía de este juicio en [IMPORTE] euros, que es, a la vez, el valor que se le da en el inventario de la liquidación de gananciales que erróneamente lo incluye.

SEXTO Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A) FUNDAMENTOS DE DERECHO PROCESALES

JURISDICCIÓN: Tiene jurisdicción el órgano del orden civil al que dirijo, atendiendo al artículo 21.1º de la Ley Orgánica del Poder Judicial, complementado por el 85.1º de la misma Ley, por ventilarse en este procedimiento materia de relaciones patrimoniales entre cónyuges, contempladas en el artículo 22 quáter de la repetida Ley, letra c), a la que remite el artículo 36.1 de la Ley de Enjuiciamiento Civil.

COMPETENCIA:

a) Objetiva.-Tiene competencia objetiva el órgano al que me dirijo en virtud del artículo 45 de la Ley de Enjuiciamiento Civil.

b) Territorial.-Y la tiene territorial. Se la atribuye el artículo 52.1 de la Ley de Enjuiciamiento Civil, porque se reivindica la propiedad privativa sobre un bien inmueble, por lo que corresponde la competencia al tribunal del lugar en que esté sita la cosa litigiosa.

CAPACIDAD DE LAS PARTES: Tienen capacidad las dos partes, mayores de edad, a tenor de los artículos 6 y 7 de la Ley de Enjuiciamiento Civil.

LEGITIMACIÓN: Tienen legitimación las partes demandante y demandada, porque son los titulares de la relación jurídica defectuosamente establecida, que se pretende ajustar a Derecho.

POSTULACIÓN: Esta parte comparece representada por Procurador, en cumplimiento del artículo 23.1 de la Ley de Enjuiciamiento Civil, cuyo poder está autorizado por Notario y se aporta a este primer escrito, obedeciendo los mandatos de los artículos 24 y 25 de la misma Ley. Y es dirigida por abogado en ejercicio, cuyo nombre se hace constar en el encabezamiento de la demanda.

PROCEDIMIENTO, EN RAZÓN A CUANTÍA: Corresponde decidirse este asunto por los trámites del juicio ordinario, pues la cuantía principal sobre la que versa el conflicto es de [IMPORTE] €, precio del inmueble cuya titularidad se reivindica, superior a los 15.000 euros, y entra, por tanto, en la previsión del artículo 249.2 de la Ley de Enjuiciamiento Civil, redactado según Ley 13/2009, de 3 de noviembre.

CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD: La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

DEMANDA Y SU DOCUMENTACIÓN: La demanda cumple los requisitos del artículo 155 de la Ley procesal y los del artículo 399 LEC. Se aportan los documentos originales en los que esta parte funda su derecho, cumpliendo los artículos 264 y siguientes de la Ley de Enjuiciamiento Civil. Se acompañan también las copias exigidas por el artículo 273 de la misma Ley.

B) FUNDAMENTOS DE DERECHO DE FONDO

ACCIÓN EJERCITADA: Se ejerce, con apoyo en el segundo párrafo del apartado 5 del artículo 787, de la Ley de Enjuiciamiento Civil, al que hace remisión el artículo 810.5 de la misma Ley, ACCIÓN DECLARATIVA DE LA PROPIEDAD Y DE CONDENA, para el caso que se hubiere llevado a efecto la Sentencia aprobatoria de las operaciones divisorias. Ambas comprendidas en el artículo 348 del Código Civil.

COSTAS: Deben ser impuestas a la parte demandada atendiendo al artículo 394 de la Ley de Enjuiciamiento Civil.

Por cuanto antecede,

SUPLICO AL TRIBUNAL: Que, teniendo por presentado este escrito, con los documentos acompañados y copia de todo ello para traslado, se sirva admitirlo, tenga por comparecido al Procurador que suscribe en representación de Doña [NOMBRE Y APELLIDOS], y por deducida DEMANDA DE JUICIO ORDINARIO contra don [NOMBRE Y APELLIDOS], y, previos los trámites legales oportunos, dicte finalmente sentencia por la que, estimando la demanda,

A) DECLARE que la vivienda en la localidad de [LOCALIDAD], núm. [Nº] de la calle de [CALLE], con una superficie construida de [Nº] metros cuadrados, es de propiedad privativa de la demandante, por lo que no puede ser incluida dentro de la sociedad de gananciales que tuvo constituida con don [NOMBRE Y APELLIDOS], y que se ha liquidado.

B) CONDENE al demandado, don [NOMBRE Y APELLIDOS], a estar y pasar por esta declaración.

C) CONDENE al demandado al pago de las costas de este procedimiento.

OTROSÍ DIGO: Que para el momento procesal oportuno se interesa el recibimiento a prueba de este juicio.

SUPLICO AL TRIBUNAL: Tenga por hecha tal manifestación a los efectos oportunos.

SEGUNDO OTROSÍ DIGO: Que siendo general el poder para pleitos que se acompaña,

SUPLICO AL TRIBUNAL: Acuerde su devolución a esta parte, previo desglose y una vez tomada nota bastante en los presentes autos.

Es Justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo. Colegiado/a núm. Fdo.: Colegiado/a núm. [Nº DE COLEGIADO]

========================================================================
