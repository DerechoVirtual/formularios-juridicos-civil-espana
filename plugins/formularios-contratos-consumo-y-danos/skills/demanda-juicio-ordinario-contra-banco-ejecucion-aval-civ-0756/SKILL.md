---
name: demanda-juicio-ordinario-contra-banco-ejecucion-aval-civ-0756
description: "Demanda de juicio ordinario contra el banco por la ejecución de un aval a primer requerimiento. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario contra el banco por la ejecución de un aval a primer requerimiento

> Formulario **CIV-0756** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en reclamación de cantidad a entidad bancaria por la ejecución de aval a primer requerimiento.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario contra el banco por la ejecución de un aval a primer requerimiento» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario contra el banco por la ejecución de un aval a primer requerimiento” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-contra-banco-ejecucion-aval-civ-0756`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] NÚMERO (6 veces)
- [ ] FECHA (5 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] CALLE (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] FECHAS (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] IMPORTE
- [ ] LUGAR
- [ ] Nº
- [ ] PUERTA
- [ ] SEDE

## Normas que cita el formulario

- art. 399.1 LEC
- art. 85.1 LOPJ
- art. 51.1 LEC
- art. 10 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 23 LEC
- art. 399 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1255 CC
- art. 394.1 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], como acredito en virtud de escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado ejerciente, n.º [NÚMERO] del Iltre. Colegio de [LOCALIDAD], con despacho abierto en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito paso a interponer demanda de juicio ordinario en reclamación de cantidad contra la entidad [DENOMINACIÓN SOCIAL], con sucursal abierta en la calle [CALLE] de [LOCALIDAD].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Todo ello de acuerdo con los siguientes hechos y consideraciones de derecho:

HECHOS

PRIMERO.- Mi mandante, D./Dña. [NOMBRE Y APELLIDOS], es dueño en pleno dominio de una finca destinada a uso distinto del de vivienda.

La descripción de dicha finca es la siguiente: Local bajo sito en [LOCALIDAD], calle [CALLE], número [NÚMERO], puerta [PUERTA]

Se acompaña el título de propiedad -escritura de compraventa- como documento n.º [NÚMERO]

SEGUNDO.- Con fecha [FECHA], se celebró contrato de arrendamiento de dicho local entre mi mandante, como arrendador, y D./Dña. [NOMBRE Y APELLIDOS], como arrendatario.

Se acompaña dicho contrato como documento n.º [NÚMERO].

TERCERO.- La entidad bancaria demandada, con fecha [FECHA], se constituyó en fiador solidario de D./Dña. [NOMBRE Y APELLIDOS], arrendatario de la actora, por la cantidad máxima por todos los conceptos y a contar desde esa fecha de [IMPORTE] euros en concepto de garantía para responder de la obligación del primero del pago de la renta, gastos y responsabilidades pecuniarias que derivasen del contrato de arrendamiento del citado local.

Por virtud de la citada garantía, la entidad avalista quedaba obligada de forma incondicional a pagar a mi representado hasta el límite de la referida cantidad, comprometiéndose el garante al efecto a tal pago a su simple requerimiento en el plazo de tres días de la recepción del requerimiento notarial al efecto, recabando la puesta a disposición del importe requerido que la misma le formule en cualquier momento antes de su fecha de caducidad el día [FECHA], sin otro requisito que la expresa manifestación de los requirentes en el referido instrumento, de que se han incumplido las obligaciones asumidas por los indicados arrendatario y contrato.

Se adjunta como documento n.º [NÚMERO] el referido contrato de aval.

CUARTO.- En fecha [FECHA] la actora efectuó el requerimiento en la forma pactada, es decir mediante acta notarial autorizada por el Notario de [LOCALIDAD] que se remitió a la demandada el día 26 siguiente por correo con acuse de recibo, siendo recibida por la última el día 30 sucesivo.

Se adjunta copia del acta notarial de referencia como documento n.º [NÚMERO]

QUINTO.- El dicho requerimiento notarial no ha sido atendido por la entidad demandada, no dejando más alternativa a esta parte que la vía judicial.

A los anteriores hechos son de aplicación los siguientes:

SEXTO.- Previamente a la presentación de la presente demanda, se llevaron a cabo diversos esfuerzos de negociación con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria.

Entre las acciones realizadas, se incluyen el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución; así como la participación en reuniones llevadas a cabo los días [FECHAS], cuyos objetivos fueron buscar una conciliación respecto de las diferencias planteadas.

Se adjuntan como prueba copias de las comunicaciones enviadas y recibidas durante el proceso de negociación, incluidas cartas, correos electrónicos y/o actas de reuniones como documentos números [Nº DE DOCUMENTO].

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en los arts. 85.1 LOPJ y 45 LEC, y puesto que no está prevenido un fuero territorial preceptivo específico, con arreglo a lo previsto en el art. 51.1 LEC, resulta territorialmente competente el Tribunal a que me dirijo, puesto que es el del partido del lugar donde tiene su domicilio la entidad demandada, así como la sucursal, o establecimiento abierto al público indicado.

II.- CAPACIDAD Y LEGITIMACIÓN.

Mi mandante es una persona física, mayor de edad, en pleno ejercicio de sus derechos civiles, por lo que tiene capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC. Lo mismo ocurre con la entidad demandada, como persona jurídica, en virtud de lo dispuesto en los arts. 6.1.3.º y 7.4 LEC.

Corresponde la legitimación activa a mi mandante por ser la persona beneficiaria de la garantía constituida, y la legitimación pasiva corresponde a la entidad demandada, en cuanto que garante que asumió la obligación de pago al beneficiario (art. 10 LEC).

III.- PROCEDIMIENTO.

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en los arts. 248 y 249.2 LEC, toda vez que el criterio de atribución preferente de la materia objeto del proceso resulta inaplicable, al carecer de especialidad típica la de éste, y cumplir entonces el criterio de cuantía, que supera los 15.000 euros.

IV.- CUANTÍA.

Cumpliendo lo prevenido en el art. 253.1 LEC, hacemos constar que la cuantía de esta demanda es de quince mil euros (15.000 €), con arreglo a la regla 1.ª del art. 251 LEC, que es el importe de la cantidad que se reclama.

V.- POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23 y 31 LEC se formula esta demanda a través de Procurador/a de los Tribunales con poder notarial para pleitos, y con dirección y firma de Letrado habilitado ante el Tribunal. Asimismo se cumplen los requisitos formales del art. 399 LEC.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FONDO DEL ASUNTO

En lo que afecta a la naturaleza y requisitos del del denominado aval «a primer requerimiento», también denominado aval «a primera solicitud» o garantía «a primera demanda» o simplemente demandada o garantía independiente, el Tribunal Supremo, especialmente desde la sentencia de 27 de octubre de 1992 (rec. 925/1990), seguida por las sentencias de 12 de julio de 2001 (rec. 1631/1996),29 de abril de 2002 (rec. 3490/1996),5 de julio de 2002 (rec. 294/1997) y 12 de noviembre de 2003 (rec. 30/1998), tiene señalado que:

1 ) Entre las nuevas modalidades de garantías personales nacidas para satisfacer las necesidades del tráfico mercantil - ante la insuficiencia de la regulación de la fianza- se encuentra la garantías llamadas «a primera solicitud», «a primer requerimiento» o «a primera demanda», contrato atípico producto de la autonomía de la voluntad sancionada en el art. 1255 CCiv;
2 ) En este tipo de contrato el garante viene obligado a realizar el pago al beneficiario cuando éste lo reclame, ya que la obligación de pago asumida se constituye como una obligación distinta, autónoma e independiente, con respecto a las que nacen del contrato cuyo cumplimiento se garantiza, que es la relación subyacente;
3 ) Por tanto, el garante no puede oponer al beneficiario que reclama el pago otras excepciones que las que se deriven de la propia relación de garantía, siendo suficiente la reclamación del beneficiario frente al garante para entender que el obligado principal no ha cumplido;
4 ) La imposibilidad del garante de oponer excepciones derivadas del contrato subyacente determina que su obligación se reduzca al pago de una suma de dinero que, al haber sido determinada expresamente en el contrato y resultar pagadera a su mera reclamación, ha de ser considerada líquida con las consecuencias pertinentes en cuanto a la producción del interés;
5 ) No obstante lo cual, en virtud del principio de la buena fe contractual, permite al garante, en caso de contienda judicial, probar que el deudor ha cumplido su obligación, produciéndose la inversión de la carga de la prueba, ya que no puede exigirse al beneficiario que acredite el incumplimiento del obligado principal de pago del garante;
6 ) Todo ello sin perjuicio de las acciones que puedan surgir como consecuencia del pago de la garantía: la de regreso del garante frente al ordenante y la causal entre los interesados en la relación subyacente.

Bajo el anterior prisma doctrinal, no cabe duda que como tal debe calificarse el aval constituido a favor de mi representado, en el sentido de que realizado el requerimiento de pago del aval por el acta notarial acordada sin que se pactara la forma de remisión de ésta y antes de su caducidad, la obligación de tal pago se produce desde aquel requerimiento sin perjuicio de que dentro de los 3 días de su recepción nazca esa obligación de pago.

En efecto, realizado este requerimiento antes de su plazo de vencimiento y, a mayor abundamiento recibido dentro de él, esta garantía está plenamente vigente y despliega todos sus efectos, máxime cuando la recepción en su caso afectaría sólo al plazo de tres días a partir del cual su garante ha de abonarlo obligación ya nacida con la realización del repetido requerimiento.

VIII.- COSTAS.

La parte demandada soportará el reintegro de todas las costas del juicio por el principio cuasiobjetivo de vencimiento del art. 394.1 LEC, para declarativos en primera instancia.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL:

Que teniendo por presentado este escrito de demanda junto con los documentos que se acompañan y copias simples de todo ello, se sirva admitirlo a trámite, se me tenga por comparecido y parte demandante en el proceso y en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, por promovido el correspondiente juicio ordinario en reclamación de cantidad contra la entidad [DENOMINACIÓN SOCIAL] SA, acordando conferirle traslado de la demanda y documentos con ella presentados, emplazándosele en legal forma y, previos los trámites oportunos, en su día, se dicte sentencia por la que se condene a la demandada a abonar a la actora la cantidad de 15.000 euros de principal, más los intereses devengados desde el día 25 de marzo de 2013, y todas las costas procesales.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
