---
name: demanda-juicio-verbal-danos-cosas-trafico-contra-civ-0823
description: "Demanda de juicio verbal por daños en cosas de tráfico contra el Consorcio de Seguros. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal por daños en cosas de tráfico contra el Consorcio de Seguros

> Formulario **CIV-0823** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio verbal sobre reclamación de indemnización de daños en las cosas derivados de accidente de circulación, interpuesta contra el Consorcio de Compensación de Seguros.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal por daños en cosas de tráfico contra el Consorcio de Seguros» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal por daños en cosas de tráfico contra el Consorcio de Seguros” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-verbal-danos-cosas-trafico-contra-civ-0823`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (15 veces)
- [ ] Nº DE DOCUMENTO (9 veces)
- [ ] CALLE (5 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] ASEGURADORA (4 veces)
- [ ] FECHA (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] NOMBRE DEL TALLER (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] MARCA/MODELO (2 veces)
- [ ] MATRÍCULA (2 veces)
- [ ] Nº (2 veces)
- [ ] APELLIDOS
- [ ] AÑO
- [ ] DATOS DEL VEHÍCULO
- [ ] FECHAS
- [ ] LUGAR
- [ ] LUGAR DE DESTINO
- [ ] LUGAR DE PROCEDENCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 437.1 LEC
- art. 15 Ley 52/1997
- art. 84.1.a Ley 40/2015
- art. 52.1.9.º LEC
- art. 7.1 LEC
- art. 551 LOPJ
- art. 253.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.902 CC
- art. 394.1 LEC
- art. 304 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], conforme acredito con escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro como documento nº [Nº DE DOCUMENTO], y con la asistencia del Letrado D./Dña. [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogado de [LOCALIDAD], cuyo despacho está abierto en esta población, calle [CALLE], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que siguiendo expresas instrucciones de quienes ostento representación, por medio del presente escrito formulo demanda deJUICIO VERBAL, que dirijo contra:

-D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, vecino de [LOCALIDAD], domiciliado en la calle [CALLE], cuyas demás circunstancias personales nos son desconocidas.
-EL CONSORCIO DE COMPENSACIÓN DE SEGUROS, para ser citado en su domicilio en [LOCALIDAD], calle [CALLE], número [NÚMERO]

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II en relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Baso mi pretensión en los siguientes datos y razonamientos jurídicos:

HECHOS

PRIMERO

Mi representado era el [FECHA] titular de un vehículo marca [MARCA/MODELO] matrícula [MATRÍCULA], conforme acredito mediante copia del permiso de circulación que se acompaña (documento número [Nº DE DOCUMENTO]), designando, para caso de impugnación contraria, los archivos y registro de la Jefatura Provincial de Tráfico de

SEGUNDO

El indicado día [FECHA], mi representado conducía el vehículo antes reseñado por la calle [CALLE] de esta población, procedente de [LUGAR DE PROCEDENCIA] y en dirección a [LUGAR DE DESTINO], cuando al efectuar una maniobra de giro hacia su izquierda, para seguir sentido a la calle [CALLE], y ya introducido en el carril destinado al efecto, fue colisionado por el vehículo marca [MARCA/MODELO], matrícula [MATRÍCULA], que conducía el codemandado D./Dña. [NOMBRE Y APELLIDOS]

De la ocurrencia del siniestro elaboró informe la Policía Local de [LOCALIDAD], registrado como diligencias n.º [NÚMERO]/[AÑO], cuya copia se aporta como documento número [Nº DE DOCUMENTO], designando los archivos municipales por si se impugnara de adverso.

TERCERO

D./Dña. [NOMBRE Y APELLIDOS] era el propietario del automóvil consignado [DATOS DEL VEHÍCULO], el cual se encontraba asegurado en la fecha del siniestro en la aseguradora [ASEGURADORA], con póliza número [NÚMERO], según declaración amistosa firmada por ambos conductores, la cual se acompaña como documento número [Nº DE DOCUMENTO].

CUARTO

Formulada reclamación a [ASEGURADORA] por el Letrado suscrito, dicha entidad dirigió carta a esta dirección letrada rehusando el siniestro por inexistencia de aseguramiento en vigor a la fecha del accidente (documento número [Nº DE DOCUMENTO]).

QUINTO

En razón a lo anterior, con arreglo al art. 11.1.b) de la Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor -Texto Refundido aprobado por Real Decreto Legislativo 8/2004, de 29 de octubre-, se dirigió por el Letrado suscrito, en nombre del actor, reclamación al Consorcio de Compensación de Seguros, dentro del límite cuantitativo del aseguramiento obligatorio, al actuar como fondo de garantía de vehículo no asegurado, en fecha [FECHA] (documento número [Nº DE DOCUMENTO]).

SEXTO

El vehículo de D./Dña. [NOMBRE Y APELLIDOS] experimentó importantes daños, que hubieron de ser reparados en [NOMBRE DEL TALLER], por precio de [IMPORTE], como se acredita con la factura de [NOMBRE DEL TALLER], que se adjunta como documento número [Nº DE DOCUMENTO].

SÉPTIMO

La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Para mi mandante es forzoso acudir a la presente vía judicial civil, dado que habiéndose dirigido solicitud de reparación a los codemandados, con expresión de las partidas por las que se solicita indemnización y su cuantía, en momento alguno han atendido al pago, habiendo transcurrido en exceso el plazo de tres meses desde dicha reclamación sin que se haya satisfecho o consignado cantidad alguna.

A efectos probatorios se acompañan sendas cartas certificadas con acuse de recibo a los codemandados (documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]) sin respuesta cabal.

FUNDAMENTOS DE DERECHO

I. COMPETENCIA

El art. 15 de la Ley 52/1997, de 27 de noviembre, de Asistencia Jurídica al Estado e Instituciones Públicas, que se declara en vigor expresamente por el párrafo 2.º del apartado 3 de la Disposición Derogatoria Única de la Ley de Enjuiciamiento Civil, confiere la competencia territorial para conocer de los procesos civiles en que sea parte el Estado y las Entidades estatales de Derecho Público a los Tribunales que tengan su sede en las Capitales de Provincia, en Ceuta o Melilla. Demandado el Consorcio de Compensación de Seguros, cuya naturaleza jurídica, según el art. 1 de su Estatuto Legal es de entidad pública empresarial de las previstas en el art. 84.1.a) de la Ley 40/2015, de 1 de octubre, de Régimen Jurídico del Sector Público, con personalidad jurídica propia y plena capacidad de obrar, resulta territorialmente competente el Tribunal al que nos dirigimos, por ser el de la capital de la provincia en cuyo territorio ocurrió el accidente.

El mandato del art. 15 de la Ley 52/1997 excepciona como ley especial el "forum delicti comissi" del art. 52.1.9.º LEC, sin que, por otra parte, se puede encontrar ninguna diferencia sustancial en el hecho de que junto al Consorcio de Compensación de Seguros concurran otra u otras partes codemandadas, siendo mayoritaria en la doctrina de apelación la tesis de aceptar sin reservas el fuero territorial del Estado y de los entes públicos, incluso en situaciones litisconsorciales.

II. PARTES

Demandante y demandados tienen capacidad para ser parte, como personas físicas, o persona jurídica pública institucional el Consorcio de Compensación de Seguros (art. 6.1.1.º y 3.º LEC), con capacidad de obrar procesal, esta mencionada entidad defendida y representada por la Abogacía del Estado (arts. 7.1 y 4 LEC y art. 551 LOPJ).

El actor ostenta legitimación activa ordinaria por derecho propio a la indemnización que reclama (art. 10, párrafo 1.º LEC), así como D./Dña. [NOMBRE Y APELLIDOS] tiene la obligación correlativa, y así, la legitimación pasiva ordinaria, fijándose la del Consorcio codemandado en la acción directa legal expresa del art. 11.3 TRLRCSCVM, como fondo de garantía de aseguradoras.

En aplicación de los arts. 23.1 y 31.1 LEC, dado que la cuantía reclamada supera los 2.000 euros, las partes comparecerán representadas por Procurador de los Tribunales y asistidas por Letrado en ejercicio, ambos habilitados ante el Tribunal.

III. PROCEDIMIENTO

En aplicación de los arts. 248.3 y 250.2 LEC, y en atención a la cuantía del objeto litigioso, de [IMPORTE] euros, suma que como cuantía ex art. 253.1 LEC se expresa, al no superar los 15.000 euros, deriva tramitar el proceso por las normas de proceso de declaración plenario común denominado juicio verbal.

IV. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V. FONDO DEL ASUNTO

La acción se dirige contra el conductor imprudente, D./Dña. [NOMBRE Y APELLIDOS], así como el Consorcio de Compensación de Seguros, en ejercicio de la acción de indemnización de daños y perjuicios materiales derivados de la circulación de vehículos de motor, especie de la responsabilidad civil extracontractual.

En el plano de los daños en las cosas, la normativa del seguro de responsabilidad civil del automóvil, modificada y rebautizada como Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor, por la Ley 30/1995 de 8 de noviembre, y actualmente recogida en el Texto Refundido aprobado por Real Decreto Legislativo 8/2004 de 29 de octubre (TRLRCSCVM), aísla un campo de relaciones sociales, la circulación de vehículos de motor, en que la responsabilidad civil sigue en un régimen subjetivo, sin suplantarse la culpabilidad por causalidad -art. 1.1, párrafo 3.º TRLRCSCVM-, y en el que la Ley no predetermina la tasa adecuada o fijación de un "quantum" máximo para la reparación, sino que mantiene la ‘restitutio in integrum’ del art. 1.902 CCiv.

No cabe discutir la acción indiligente de D./Dña. [NOMBRE Y APELLIDOS] RAMÓN [APELLIDOS] y tampoco el nexo causal adecuado entre la colisión y los daños sufridos por el vehículo de mi mandante, y esa restitución íntegra derivará de la valoración de la prueba, como quedan razonados los hechos, destacando que, en este campo de los daños materiales, no deja de arar el surco de la nueva orientación legislativa para el campo de las lesiones personales, cuya indemnidad no es monetizable en rigor, la consagración de expedientes objetivadores, como son las tarifas y facturas de los profesionales, como [NOMBRE DEL TALLER], que realizó la reparación del vehículo, invirtiendo [Nº] días, y por precio de [IMPORTE] euros, especificándose las partidas y el precio de la mano de obra, común del sector, puesto que controlan el efecto multiplicador de la litigiosidad con referentes que todas las compañías de seguros pueden conocer, como todo lo contrario ocurriría con exigencias de pruebas costosas e irreales.

Se demanda al Consorcio de Compensación de Seguros, de conformidad con lo dispuesto en el art. 11.1 b) y 3 TRLRCSCVM, en relación con los arts. 2 TRLRCSCVM (deber de suscripción del seguro obligatorio), 3 TRLRCSCVM (incumplimiento del deber) y 4 TRLRCSCVM (límite cuantitativo de la cobertura del seguro obligatorio), y con el art. 20.1 Reglamento del seguro obligatorio de responsabilidad civil en la circulación de vehículos a motor, aprobado por Real Decreto 1507/2008 de 12 de septiembre, acreditando haberle formulado reclamación previa justificando la existencia de controversia.

Según el Fichero Informativo de Vehículos Asegurados (FIVA), el vehículo del demandado se encontraba asegurado en la aseguradora [ASEGURADORA], y así se hizo constar en el parte amistoso del siniestro, pero reclamándose formalmente a la misma, resultó que no estaba la póliza en vigor.

Teniendo en cuenta lo anterior, procede no sólo exigir al Consorcio de Compensación de Seguros demandado la indemnización determinada, dentro del límite máximo por siniestro y vehículo del seguro obligatorio, sino también el interés moratorio establecido, interés consistente en el legal en vigor a la fecha del siniestro incrementado en un 50%, con devengo diario, y no inferior al 20% si transcurrieran dos años desde la producción del siniestro, sin perjuicio de sus facultades de repetición del Consorcio respecto de la aseguradora [ASEGURADORA], con exigencia del interés del 25 %.

VI. COSTAS

El empleo del principio cuasiobjetivo del vencimiento del art. 394.1 LEC, conlleva el deber de reintegro de las costas procesales por la parte demandada, sin que existan dudas de hecho o derecho, ni vacilaciones jurisprudenciales sobre el objeto del proceso.

En virtud de lo expuesto,

AL TRIBUNAL SUPLICO

que, habiendo por presentado este escrito con sus copias y los documentos que se acompañan, se sirva admitir unos y otros, teniendo por formulada demanda de juicio verbal civil en nombre de quien comparezco, contra D./Dña. [NOMBRE Y APELLIDOS], así como contra el Consorcio de Compensación de Seguros y, previo traslado a los demandados para que comparezcan y la contesten, y demás trámites legales, se sirva dictar sentencia por la que estimando íntegramente esta demanda se les condene a que paguen al actor conjunta y solidariamente la suma deeuros, siendo la condena del Consorcio dentro de los límites cuantitativos del aseguramiento obligatorio al actuar como fondo de garantía respecto de un vehículo carente de aseguramiento, más los intereses legales respecto del codemandado D./Dña. [NOMBRE Y APELLIDOS] desde la interpelación judicial y los especiales de mora del asegurador, legal vigente en la fecha de ocurrencia del siniestro incrementado en un cincuenta por ciento desde aquella fecha, o en su caso, del veinte por ciento a partir del segundo año, respecto del Consorcio de Compensación de Seguros, más las costas de este juicio.

Es Justicia de hacerse en [LUGAR], a [FECHA].

OTROSÍ DIGO: Que interesa al derecho de esta parte, desde ahora y para la proposición de prueba en su momento procesal oportuno:

-Citación del codemandado D./Dña. [NOMBRE Y APELLIDOS] con la admonición legal de ser tenido por conforme con los hechos en que hubiera tenido intervención personal y le sean perjudiciales, en caso de incomparecencia o negativa a declarar, conforme al art. 304 LEC.
-Citación de los testigos siguientes, con sus respectivos domicilios, interesando se libre exhorto al Tribunal de Instancia Decano de los de [LOCALIDAD], con entrega a la Procuradora que suscribe para cuidar de su cumplimiento:

D./Dña. [NOMBRE Y APELLIDOS]

Domicilio:

D./Dña. [NOMBRE Y APELLIDOS]

Domicilio:

AL TRIBUNAL SUPLICO se sirva tener por causadas las anteriores manifestaciones a los efectos pertinentes, y por formulada la solicitud de precaución de prueba, como es de hacer en justicia que reitero ‘ut supra’.

Firma del Abogado/a	Firma del Procurador/a

========================================================================
