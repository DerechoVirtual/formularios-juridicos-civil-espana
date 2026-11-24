---
name: demanda-acumulacion-acciones-civ-0992
description: "Demanda con acumulación de acciones. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda con acumulación de acciones

> Formulario **CIV-0992** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda con acumulación de acciones» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda con acumulación de acciones” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:demanda-acumulacion-acciones-civ-0992`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (9 veces)
- [ ] DESCRIPCIÓN DE LA REPARACIÓN (8 veces)
- [ ] DIRECCIÓN (5 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] AÑO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIBIR
- [ ] DESCRIPCIÓN DE LAS DEFICIENCIAS
- [ ] DOMICILIO
- [ ] DÍA
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE PROCEDIMIENTO
- [ ] PARTE DEMANDADA
- [ ] SEDE
- [ ] TIPO DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 71.2 LEC
- art. 73 LEC
- art. 1101 CC
- art. 1544 CC
- art. 1106 CC
- art. 1100 CC
- art. 394 LEC
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…TO]/[AÑO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Juicio [TIPO DE PROCEDIMIENTO] n.º [Nº DE PROCEDIMIENTO]/[AÑO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A] según se acredita mediante copia electrónica del poder notarial de representación informática (o digitalizada) que se acompaña y se solicita sea devuelta una vez testimoniada por medio de la presente formulo demanda de juicio ordinario frente a la mercantil [DENOMINACIÓN SOCIAL], domiciliada en [DOMICILIO] C [DIRECCIÓN] y la fundo en los siguientes:

HECHOS

PRIMERO.- Que en la vivienda titular de mi representado sita en [LOCALIDAD] C [DIRECCIÓN] se llevaron a cabo por parte de [NOMBRE DE LA PARTE] obras de rehabilitación consistentes en [DESCRIBIR] A tal efecto se suscribió el correspondiente documento de encargo adjunto como documento n.º 2 de esta demanda en el que se hace expresa remisión en cuanto a las concretas labores a efectuar al presupuesto aceptado por las partes y que se adjunta como documento n.º 3. El importe de tales obras [IMPORTE] Euros fue puntualmente abonado por mi representado por medio de transferencias bancarias a la cuenta de la mercantil demandada tal y como se acordó en el pacto 5.º del contrato aportado como documento n.º 1 antes mencionado y que se acreditan por los pertinentes resguardos bancarios que se adjuntan como documentos n.º 4 a 8.

SEGUNDO.- Una vez terminadas las obras se ha constatado la aparición de una serie de deficiencias que constan en el acta notarial al efecto levantada el pasado [FECHA] y que se adjunta como documento n.º 9 de esta demanda.

Tales deficiencias consisten en [DESCRIPCIÓN DE LAS DEFICIENCIAS] habiéndose verificado por parte del arquitecto técnico D. el pertinente examen de las mismas concluyendo que obedecen a defectos de ejecución material ascendiendo su coste de reparación a [IMPORTE] Euros (IVA incluido). Dicho dictamen se aporta a las presentes actuaciones como documento n.º 10 de esta demanda.

TERCERO.- Asimismo a la mercantil demandada le encargó mi mandante la realización de unas obras de acondicionamiento en el local comercial sito en [LOCALIDAD] C [DIRECCIÓN] del que D. es arrendatario en virtud de contrato de fecha [FECHA] que se aporta como documento n.º 11 y consistentes en colocación del mobiliario adecuado, pintura de las paredes e instalación de parquet en toda la superficie del local.

A tal efecto se suscribió el [FECHA] el correspondiente documento de encargo que se aporta como documento n.º 12 y en base al presupuesto aceptado por ambas partes y que se adjunta como documento n.º 13.

El precio de tales labores ( Euros) fue abonado por mi mandante por medio de transferencias bancarias cuya realidad se acredita por medio de los resguardos pertinentes que se adjuntan como documentos n.º 14 y 15.

CUARTO.- Una vez concluidas las reparaciones se han detectado las deficiencias siguientes:

La realidad de las mismas como sucedía con las referentes a la vivienda, deriva del acta notarial levantada el [FECHA] y que se adjunta como documento n.º 16 de esta demanda habiendo sido valorada su reparación por el arquitecto técnico D. [NOMBRE Y APELLIDOS] en [IMPORTE] Euros, concluyendo que su origen es un defecto de ejecución material y precisándose en tal dictamen que para la realización de las reparaciones pertinentes serán necesarios [Nº] días en los que el local deberá permanecer cerrado.

Dicho dictamen se adjunta como documento n.º 16 de la demanda.

QUINTO.- El objeto de esta demanda es el que se indemnice a mi mandante en la cantidad de [IMPORTE] Euros que es el coste de las reparaciones que es necesario efectuar tanto en la vivienda como en el local para dejarlo en condiciones idóneas y subsidiariamente la condena a la demandada a llevarlas a cabo. Asimismo se reclama la cantidad de [IMPORTE] Euros que es el importe de las ganancias que se dejarían de obtener durante el período en el que el local deberá permanecer cerrado mientras se llevan a cabo las reparaciones. La justificación de este importe se desprende de la media de ventas que se obtiene en un período de tiempo como el indicado, al constar que el promedio de venta diaria es de [IMPORTE] Euros tal y como resulta de las hojas de ingreso del IVA a la AEAT de los últimos 2 años que se adjuntan como documentos n.º 17 a 24 de esta demanda, sin que quepa verificar descuento alguno ya que los gastos propios derivados del funcionamiento del local se deberán continuar abonando durante el tiempo en el que se desarrollen las obras.

SEXTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

Competencia y procedimiento

Para conocer de esta demanda corresponde a los Tribunales de esta ciudad al tratarse de un juicio ordinario y tener la demandada su domicilio en la misma (arts. 249.2; 45 y 51 LEC).

Acumulación de acciones

Se estima procedente el ejercicio de las acciones derivadas de los dos encargos realizados al tratarse del mismo demandante y demandado aun cuando se fundan en diferentes títulos (art. 71.2 LEC) poseyendo para ambas competencia el tribunal ante el que me dirijo, siendo las acciones que se podrían tramitar por separado del mismo tipo (ambos juicios ordinarios) (art. 73 LEC).

Fondo de la cuestión

Se ejercita en ambos casos una acción por responsabilidad contractual (art. 1101 CC) derivada del incumplimiento por parte de la demandada de la obligación por ella asumida en los contratos de obra que vinculan a las partes (art. 1544 CC) solicitándose el importe de la reparación y subsidiariamente la condena a la demandada a la realización de tales trabajos, siendo el fundamento de la reclamación del lucro cesante por el tiempo de cierre del local el art. 1106 CC y la jurisprudencia según la que no basta con meras hipótesis o suposiciones, ni es suficiente con referir beneficios dudosos o contingentes, constatándose los mismos con una prueba basada en criterios de probabilidad objetiva que tengan el curso normal de los acontecimientos y las circunstancias (SSTS 31 mayo 1983; 7 junio 1988; 16 junio 1993; 30 junio 1993; 15 diciembre 1995; 8 julio 1996; 21 octubre 1996). En cuanto a los intereses el art. 1100 CC.

Costas

El art. 394 LEC sobre imposición de costas a los litigantes cuyas peticiones hayan sido totalmente rechazadas.

En base a lo anterior,

SUPLICO al Tribunal que tenga por interpuesta la presente demanda con el poder, documentos y copias, la admita decretando la unión de los mismos a las actuaciones, teniendo por comparecida a esta parte y por interpuesta demanda de juicio ordinario frente a [PARTE DEMANDADA] en la que tras los trámites oportunos se dicte sentencia por la que se condene a la demandada a abonar a mi principal la cantidad de [IMPORTE] Euros más los intereses de la misma desde la interpelación judicial. Subsidiariamente y para el caso de que no se estime procedente el abono del importe de reparación de las deficiencias apreciadas se solicita que se condene a la demandada a efectuar las siguientes reparaciones en un plazo que prudencialmente se fija en un mes: A) En la vivienda sita en [LOCALIDAD] C [DIRECCIÓN] las siguientes reparaciones: a) [DESCRIPCIÓN DE LA REPARACIÓN] b) [DESCRIPCIÓN DE LA REPARACIÓN] c) [DESCRIPCIÓN DE LA REPARACIÓN] d) [DESCRIPCIÓN DE LA REPARACIÓN]; B) En el local sito en [LOCALIDAD] C [DIRECCIÓN] las siguientes: a) [DESCRIPCIÓN DE LA REPARACIÓN] b) [DESCRIPCIÓN DE LA REPARACIÓN] c) [DESCRIPCIÓN DE LA REPARACIÓN] d) [DESCRIPCIÓN DE LA REPARACIÓN] A esta cantidad se añadirá la de [IMPORTE] Euros en concepto de lucro cesante y los intereses que genere desde la interpelación judicial. Asimismo se solicita que se condene a la demandada en el pago de las costas derivadas de las presentes actuaciones.

OTROSÍ DIGO: El importe de este procedimiento se fija en [IMPORTE] euros que es la cantidad objeto de reclamación derivada de ambas acciones que se ejercitan de forma acumulada, conforme a las reglas establecidas en el artículo 251 y ss. de la LEC.

OTROSÍ SEGUNDO DIGO.-Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 300 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hechas las anteriores manifestaciones a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

a [DÍA] de [MES] de [AÑO]

Firma Abogado	Firma Procurador

========================================================================
