---
name: demanda-desahucio-precario-local-trastero-civ-0556
description: "Demanda de desahucio por precario de local trastero. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de desahucio por precario de local trastero

> Formulario **CIV-0556** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de desahucio por precario de local trastero» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de desahucio por precario de local trastero” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-desahucio-precario-local-trastero-civ-0556`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] CALLE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] FOLIO
- [ ] IMPORTE
- [ ] LINDEROS
- [ ] LUGAR Y FECHA
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] Nº
- [ ] Nº DE LOCAL

## Normas que cita el formulario

- art. 250.1.2 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 394 LEC
- art. 251 LEC
- art. 7.2 Ley 10/2012

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de la Comunidad de propietarios del edificio sito en esta ciudad, calle [CALLE], representada por su presidente Don [NOMBRE Y APELLIDOS] con domicilio en [LOCALIDAD], según acredito con la copia electrónica del poder notarial de representación informática (o digitalizada) general para pleitos que acompaño y cuya devolución solicito previa unión a los autos de testimonio suficiente, por ser necesaria para otros asuntos, ante el Tribunal comparezco y DIGO:

Que demando en juicio verbal de desahucio por precario a Don [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], a fin de que tras la tramitación del juicio verbal se dicte sentencia condenando al demandado a dejar libre, vacuo y expedito el local-trastero sito en la parte interior de la finca de esta ciudad, calle [CALLE], nº [NÚMERO], propiedad de mi mandante y cuya posesión ostenta el demandado sin título alguno que la justifique y sin pagar renta, merced o contraprestación alguna, tal como quedará expuesto más abajo al basar mi petición en los siguientes:

HECHOS

Primero.- La Comunidad de Propietarios, de quien ostento la representación, es dueña en pleno dominio del local-trastero sito en la planta baja del edificio sito en esta ciudad [LOCALIDAD], calle [CALLE], nº [NÚMERO] el cual consta identificado y descrito en la escritura de constitución de propiedad horizontal como «Local-Trastero [Nº DE LOCAL], de [Nº] m2, que linda con [LINDEROS] y al cual se accede mediante una puerta interior desde el vestíbulo».

Este local-trastero se encuentra libre de cargas y gravámenes y según se desprende del apartado transcrito en la citada escritura pública, constituye un recinto interior comunitario susceptible de ser utilizado de forma independiente a los demás elementos comunes, por estar debidamente individualizado y separado pues no sólo cuenta con dos ventanas que le proporcionan luz natural, ambas abiertas al patio de manzana, sino también con suministro comunitario de agua y electricidad y, se accede a su interior mediante una puerta a través del vestíbulo, de la cual sólo tiene llave el demandado. Acompaño a esta demanda la copia de la escritura de constitución de propiedad horizontal, otorgada ante Notario de [LOCALIDAD], en fecha [FECHA] la cual consta debidamente inscrita en el Registro de la Propiedad (Doc. nº 2).

Segundo.- El local-trastero, ha venido siendo ocupado en exclusiva por el demandado desde [FECHA] y por mera tolerancia de la comunidad de propietarios, sin que se haya constituido título alguno que justifique la posesión ni se haya pactado el pago de renta ni derecho alguno asimilable al pago de una renta o en contraprestación de la posesión.

Tercero.- Que el Presidente de la Comunidad en ejecución del acuerdo adoptado en la reunión de [FECHA], según consta en el folio [FOLIO] del Libro de Actas que como documento nº 3 acompaño, ha requerido en múltiples ocasiones y de forma amistosa al demandado para que desalojara el local-trastero y lo pusiera a disposición de la comunidad libre, vacuo y expedito, gestiones que resultaron infructuosas por lo que el pasado [FECHA] formuló un requerimiento con intervención del Notario de esta ciudad Don [NOMBRE Y APELLIDOS].

No obstante el demandado, tal como ha venido haciendo reiteradamente, contestó al requerimiento alegando la existencia de un contrato verbal de arrendamiento el cual, por supuesto, no es aceptado por esta parte. Y tal como había hecho en otras ocasiones alegó el pago de una cantidad superior a la que le corresponde abonar por gastos de comunidad atribuyendo a la diferencia el carácter de renta por la utilización del local. (Acompaño como documento nº 4 el acta original de requerimiento y su contestación o certificación del acta de conciliación).

Cuatro.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A estos hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

Primero.- La pretensión que se ejercita queda amparada en el art. 250.1.2º de la LEC que tutela la recuperación de la plena posesión de una finca, cedida en precario, por el dueño, usufructuario o cualquier otra persona con derecho a poseer dicha finca y que, conforme al mismo precepto, se seguirá por los trámites del juicio verbal.

Segundo.- Corresponde la competencia para conocer de esta clase de procesos al Tribunal de Instancia del lugar en que se halle la finca a tenor de lo establecido en el artículo 45, 47 y 52.1.7º de la LEC.

Tercero.- Mi mandante ostenta la legitimación para interponer esta demanda puesto que fue designado Presidente de la Comunidad en Junta de fecha [FECHA] Por otra parte, la interposición de esta demanda fue acordada en Junta de propietarios, convocada al efecto, que tuvo lugar en fecha [FECHA] Acompaño copias de las actas levantadas, como docs. nos 5 y 6.

La Comunidad de propietarios demandante está legitimada para el ejercicio de la acción al tener la propiedad plena del local-trastero cuya posesión pretende recuperar, tal como ha quedado acreditado con el documento nº 2 de escritura de constitución de la propiedad horizontal, en cuyo apartado, consta la descripción del local-trastero como dependencia que constituye finca independiente y separada la cual fue inscrita en el Registro de la Propiedad y cuya titularidad corresponde a la Comunidad de propietarios por tratarse de un elemento común (doc. nº 2).

Cuarto.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Quinto.- A falta de una definición legal del precario ha sido la Jurisprudencia del Tribunal Supremo la que ha determinado su concepto y sus requisitos. Conforme a ella «se encuentran en precario los que sin pagar merced poseen una finca sin título o con título ineficaz para destruir el del dueño, y sin otra razón que la simple tolerancia o liberalidad del propietario» [SSTS de 22 de junio de 1945, 5 de julio de 1955, 12 de noviembre de 1962 (RJ/1962/5003) 24 de septiembre de 1963 y 16 de febrero de 1965, entre otras].

Sexto.- Hay que tener en cuenta que el exceso de la cantidad que trimestralmente abona el demandado, la mayor parte de la cual corresponde a su cuota de participación en los gastos comunitarios, sólo viene a reembolsar las cantidades estimadas por consumo de agua y luz con los que cuenta el trastero ya que al no disponer el local de contadores independientes son satisfechas por la Comunidad en los recibos que oportunamente pasan al cobro las Compañías suministradoras.

Por lo demás, anticipándonos a una eventual oposición del demandado, es preciso manifestar que el exceso de la cantidad por él ingresada, sin duda superior a la que le correspondería por cuotas de la comunidad, no ha sido aceptado por la comunidad en concepto de renta o contraprestación sino, como ya se ha dicho más arriba, en compensación de los gastos por los servicios y suministros que satisface la comunidad pues como afirma la SAP de Barcelona, de 27 de febrero de 2002 (PROV 2002, 149687) «no cabe olvidar que la jurisprudencia es constante al declarar que el hecho de pagar merced o renta, lo cual excluiría la condición de precarista, no está constituido por la mera entrega de una cantidad en dinero sino que tal entrega ha de ser por cuenta propia y a título de renta, y aceptada expresa o tácitamente en este concepto, sin que los gastos o pagos que fueren realizados por el ocupante para su propia utilidad, como pueden ser los suministros de agua, luz, calefacción, etc., constituyan renta si no consta que fueron aceptados como contraprestación por el arrendamiento, lo cual no ocurre en este caso».

En el mismo sentido podemos citar la SAP de Orense, de 30 de mayo de 2002 (PROV 2002, 179074); la SAP de Segovia, de 30 de diciembre de 2000 (PROV 2001, 96551); o las más recientes, la SAP de Barcelona, de 14 de junio de 2007 (PROV 2007, 293291) y la SAP de Murcia, de 26 junio de 2007 (PROV 2007, 357738).

Séptimo.- Con arreglo a lo establecido en el art. 394 de la LEC procede imponer las costas de este proceso a la parte demandada, ya que, como nos dice la SAP de Barcelona que seguidamente se cita, al haberse formulado el requerimiento previo se hizo saber al demandado el cese de la tolerancia posesoria y al haber hecho caso omiso y mantener su ilegal ocupación, ha obligado a la Comunidad de Propietarios a la que represento a interponer esta demanda (SAP de Barcelona, de 12 de julio de 2007, rec. 739/2006), y por cuanto antecede:

SUPLICO AL TRIBUNAL: Que tenga por presentada esta demanda, con su copia y documentos que la acompañan, que la admita y que me tenga por personado y parte en la representación que ostento de la Comunidad de Propietarios del edificio sito en la calle [CALLE], de esta ciudad, en virtud de la copia electrónica del poder notarial de representación informática (o digitalizada) general para pleitos cuya devolución intereso previa unión a los autos de copia testimoniada (o designa apud acta efectuada por el Presidente de la Comunidad), que se entiendan conmigo las sucesivas diligencias y que se tenga por formulada demanda de juicio verbal de desahucio por precario contra Don [NOMBRE Y APELLIDOS], así como que, previos los trámites que procedan, señale día y hora para la celebración de la vista con citación al demandado en legal forma y con los apercibimientos establecidos en la Ley, y, en su día, se dicte sentencia por la que se estime la demanda condenando al demandado a dejar libre y expedito y a disposición de mi mandante el local-trastero objeto de este proceso, con apercibimiento de lanzamiento si no lo llevara a cabo y con expresa imposición de costas.

OTROSÍ DIGO: Que fijo la cuantía del pleito en [IMPORTE] euros, que corresponde al valor del bien inmueble cuya posesión se reclama conforme a los precios corrientes de mercado, al amparo del apartado 3º de la regla 3ª en relación con la regla 2ª del art. 251 de la LEC.

OTROSÍ DIGO.-Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por Real Decreto Ley 3/2013, de 22 de febrero, y Ley 25/2015, de 28 julio, y por Orden HAP/861/2015, de 7 de mayo, siendo mi representada persona jurídica no exenta, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 150 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR Y FECHA].

========================================================================
