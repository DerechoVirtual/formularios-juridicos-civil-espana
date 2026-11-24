---
name: demanda-ordinaria-rescision-lesion-segun-codigo-civil-civ-0818
description: "Demanda ordinaria de rescisión por lesión según el Código civil catalán, con dictamen pericial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ordinaria de rescisión por lesión según el Código civil catalán, con dictamen pericial

> Formulario **CIV-0818** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en ejercicio de la pretensión de rescisión por lesión prevista en el artículo 621-46 del Código civil de Catalunya.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ordinaria de rescisión por lesión según el Código civil catalán, con dictamen pericial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ordinaria de rescisión por lesión según el Código civil catalán, con dictamen pericial” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-ordinaria-rescision-lesion-segun-codigo-civil-civ-0818`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (27 veces)
- [ ] NÚMERO (17 veces)
- [ ] LOCALIDAD (12 veces)
- [ ] Nº DE DOCUMENTO (12 veces)
- [ ] IMPORTE (10 veces)
- [ ] FECHA (8 veces)
- [ ] Nº (4 veces)
- [ ] AÑO (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHAS (2 veces)
- [ ] FINCA (2 veces)
- [ ] MUNICIPIO (2 veces)
- [ ] NOMBRE DE LA FINCA (2 veces)
- [ ] NOMBRE DEL PROYECTO DE URBANIZACIÓN (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] PARTE DEMANDADA (2 veces)
- [ ] TITULAR REGISTRAL (2 veces)
- [ ] BENEFICIARIO
- [ ] CORREO ELECTRÓNICO
- [ ] FECHA DE NACIMIENTO
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] NOMBRE DE LA EMPRESA TASADORA
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE DEL PROYECTO URBANÍSTICO
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE POLÍGONO
- [ ] Nº DE PROTOCOLO
- [ ] SEDE
- [ ] TELÉFONO
- [ ] TOMO
- [ ] UNIDAD FISCAL

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 51.1 LEC
- art. 53.2 LEC
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 10 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 399 LEC
- art. 5 Ley Orgánica 1/2025
- art. 621 CC
- art. 1.156 CC
- art. 1.204 CC
- art. 1.203 CC
- art. 1.295 Código Civil
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

- Junto a «…N CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO DE REPARTO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta (de dicho Registro) automatizada orientada al dato. Algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC, configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada; se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

(2) El art. 155.3 LEC permite fijar expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes, o apoderados; o, si es asociación que consta en registro oficial; el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, nº [Nº] de teléfono o de fax, dirección de correo electrónico, o similares.

========================================================================


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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO DE REPARTO CORRESPONDA

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito, y en ejercicio de la pretensión de RESCISIÓN POR LESIÓN, prevista en el artículo 621-46 del Código civil de Catalunya (CCC) vengo a formular DEMANDA DE JUICIO DECLARATIVO OREDINARIO, contra [PARTE DEMANDADA], C.I.F. n.º [NÚMERO], con domicilio en [LOCALIDAD], y D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

HECHOS

PRIMERO.- D./Dña. [NOMBRE Y APELLIDOS] era propietario de una finca conocida como [NOMBRE DE LA FINCA] ‘, en el término municipal de [MUNICIPIO], en la cual tenía construida una pequeña vivienda unifamiliar con garaje, almacén y recinto para aperos rústicos, de una superficie de unos trescientas cincuenta metros cuadrados, sobre un terreno de superficie total de aproximadamente siete mil metros cuadrados.

Se trataba de finca n.º [NÚMERO], al folio [FOLIO] de [LOCALIDAD], tomo [TOMO], libro [LIBRO], del Registro de la Propiedad n.º [NÚMERO] de [LOCALIDAD]. Se acompaña certificación registral como documento n.º [NÚMERO].

La parcela del Catastro de Rústica de [MUNICIPIO] (Unidad Fiscal [UNIDAD FISCAL]) era número [NÚMERO], del polígono [Nº DE POLÍGONO]. Se acompaña cédula catastral como documento n.º [NÚMERO].

SEGUNDO.- Con fecha [FECHA], se otorgaron dos escrituras públicas ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], números [Nº] y [Nº] de su protocolo general corriente.

En la primera de ellas, D./Dña. [NOMBRE Y APELLIDOS] vendía a [NOMBRE Y APELLIDOS]. la descrita finca registral por el precio de [IMPORTE] euros, previéndose para el pago un término de doce meses. Se adjunta copia auténtica como documento n.º [NÚMERO].

TERCERO.- En la segunda escritura pública, comparecieron por una parte D./Dña. [NOMBRE Y APELLIDOS], y por la otra D./Dña. [NOMBRE Y APELLIDOS], en su propio nombre y derecho, y también en nombre y representación de [NOMBRE DEL REPRESENTADO/A].

Es el anexo documento n.º 4 de la mentada escritura, en que los otorgantes se comprometen a:

a) Ejecutar las obras de urbanización de [NOMBRE DEL PROYECTO DE URBANIZACIÓN] ‘, en [LOCALIDAD], de conformidad a las determinaciones del proyecto de urbanización aprobado por el Ayuntamiento de [LOCALIDAD], tal como consta en el día de hoy.
b) Terminar la ejecución de dichas obras en el plazo máximo de los dieciocho meses siguientes a la formalización del acta de replanteo con el Ayuntamiento de la citada localidad.
c) Entregar, una vez finalizadas las obras referidas, a D./Dña. [NOMBRE Y APELLIDOS] o persona natural o jurídica que aquel designe, seis solares de los resultantes en el proceso compensatorio, siendo tales solares los que constan en el plano que los comparecientes me entregan por duplicado, firmándolos en mi presencia, y quedando uno de ellos incorporado a la presente, pactando expresamente que con la entrega de dichos solares quedará totalmente pagado y satisfecho el precio de [IMPORTE] euros, pactado en escritura de compraventa por mí autorizada en el día de hoy, en cuya virtud D./Dña. [NOMBRE Y APELLIDOS] ha vendido una finca a la mercantil [DENOMINACIÓN SOCIAL].

Se dejaba además constancia que de la finca registral matriz que se ha consignado más arriba, por virtud del proceso urbanístico, resultaban dos fincas nuevas, la número [NÚMERO] y la número [NÚMERO], como se aprecia en la certificación del documento n.º 1, siendo la primera atribuida al Ayuntamiento de [LOCALIDAD] por cesión obligatoria derivada de la Ley del Suelo, y la primera la que se inscribió como titularidad de [TITULAR REGISTRAL].

CUARTO.- Si para el [TITULAR REGISTRAL] como máximo, se habían de haber entregado por parte de la demandada los seis solares edificables resultantes después del proceso de urbanización de [NOMBRE DEL PROYECTO DE URBANIZACIÓN] ‘, no sucedió hasta diez meses más tarde, el [FECHA], cuando ante el Notario de [LOCALIDAD], mi patrocinado otorgó en favor de [BENEFICIARIO] carta de pago de la cantidad de [IMPORTE] euros, precio acordado en su día, cantidad que D./Dña. [NOMBRE Y APELLIDOS] declaraba que le había pagado la sociedad demandada.

Se acompaña copia del acta notarial, número [NÚMERO] del protocolo general corriente de dicho Notario, como documento n.º [NÚMERO].

QUINTO.- El mismo día [FECHA], otorgó D./Dña. [NOMBRE Y APELLIDOS] ante el mismo Notario autorizante de [NOMBRE DEL NOTARIO], escritura con número de protocolo general corriente [Nº DE PROTOCOLO], que eleva a público un contrato denominado atípico, a cuyo tenor se pactaba con la mercantil [DENOMINACIÓN SOCIAL] debidamente representada por D./Dña. [NOMBRE Y APELLIDOS], dejarse sin efecto las obligaciones derivadas de la segunda de las escrituras públicas mencionadas, que se reseña en el ordinal tercero, y en concreto, la obligación de entregar en favor de mi mandante los seis solares a los que se hacía referencia.

Se acompaña copia auténtica del contrato como documento n.º [NÚMERO].

SEXTO.- Mi representado nació el [FECHA DE NACIMIENTO], por lo que tenía [Nº] años cuando suscribió los indicados documentos públicos, y padecía un proceso ansioso-depresivo como reacción a la muerte de su esposa, como se acredita mediante certificados de nacimiento y matrimonio expedidos por el Registro Civil, y dictamen médico del Dr./a. D./Dña. [NOMBRE Y APELLIDOS], especialista en psiquiatría gerontológica, de fecha (respectivos documentos nos. [Nº DE DOCUMENTO], [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]).

SÉPTIMO.- El precio de mercado mínimo de los seis solares edificables del proyecto urbanístico ‘´ [NOMBRE DEL PROYECTO URBANÍSTICO] ‘ asciende a la fecha del precitado contrato atípico de extinción de compromisos antecedentes a 600.000 euros, con arreglo al informe emitido por Expertos Inmobiliarios de [NOMBRE DE LA EMPRESA TASADORA].

Se acompaña el informe, como dictamen pericial de parte, haciendo documento n.º [NÚMERO].

OCTAVO.- Los hechos relacionados no dejan lugar a duda sobre la inequívoca mala fe de D./Dña. [NOMBRE Y APELLIDOS] y la sociedad codemandada, en la elaboración de los negocios que han sorprendido la confianza de mi patrocinado, una persona provecta, enferma, y sumida en la depresión por la reciente viudez, y hasta el último momento, a través del despacho de abogados que respaldan la demanda, ha intentado negociar una solución extrajudicial que permitiera restablecer de alguna manera aceptable la lesión patrimonial causada, sin tener que incurrir en un largo y costoso acudimiento a los tribunales, que la sociedad demandada está en mucha mejor condición económica para soportar, por ser profesional de la construcción, pero que se ha negado a cualquier solución.

NOVENO.- Previamente a la presentación de la presente demanda, se llevaron a cabo diversos esfuerzos de negociación con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria.

Entre las acciones realizadas, se incluyen el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución; así como la participación en reuniones llevadas a cabo los días [FECHAS], cuyos objetivos fueron buscar una conciliación respecto de las diferencias planteadas.

Se adjuntan como prueba copias de las comunicaciones enviadas y recibidas durante el proceso de negociación, incluidas cartas, correos electrónicos y/o actas de reuniones como documentos números [Nº DE DOCUMENTO].

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo, viéndonos en la necesidad de acudir a la presente vía judicial.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los presentes hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- PRESUPUESTOS SUBJETIVOS.

I.1. JURISDICCIÓN Y COMPETENCIA.

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en el art. 85.1 LOPJ y art. 45 LEC, y puesto que no está prevenido un fuero territorial preceptivo específico, con arreglo a lo previsto en el art. 51.1 LEC, resulta territorialmente competente el Tribunal a que me dirijo, puesto que es el del partido del lugar donde tiene su domicilio social la demandada, toda vez que, ante las pretensiones frente a varios demandados a los que corresponderían distintos Tribunales, la elección pertenece a la parte actora, con arreglo al art. 53.2 LEC.

I.2. CAPACIDAD Y LEGITIMACIÓN.

Tanto mi mandante como el demandado D./Dña. [NOMBRE Y APELLIDOS] son personas físicas, mayores de edad, en pleno ejercicio de sus derechos civiles, por lo que tienen capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC.

es una persona jurídica mercantil, sociedad de responsabilidad limitada, por su inscripción en el Registro Mercantil con capacidad para ser parte (art. 6.1.3.º LEC), y capacidad procesal (art. 7.4 LEC), compareciendo por medio de su representante orgánico o necesario.

Corresponde la legitimación activa directa a mi mandante, ya que según el art. 10 LEC, es titular de un derecho subjetivo, por cuanto que es la parte perjudicada en la contraprestación pecuniaria por los codemandados, dado el precio que se le pagó y el valor en cambio de la finca transmitida, quienes por dicha razón, al ser la otra parte contratante, D./Dña. [NOMBRE Y APELLIDOS], en su propio nombre y derecho, y la sociedad representada orgánicamente por el mismo, correlativamente beneficiada, es por lo que están legitimados pasivamente de forma directa.

I.3. POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23.1 y 31.1 LEC se formula esta demanda por medio de representación a Procurador/a de los Tribunales con poder notarial para pleitos, y bajo dirección y firma de Letrado habilitado ante el Tribunal.

II.- PRESUPUESTOS OBJETIVOS.

II.1. PROCEDIMIENTO

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en los arts. 248 y 249.2 LEC, toda vez que el criterio de atribución preferente de la materia objeto del proceso resulta inaplicable, al carecer de especialidad típica la de éste, y cumplir entonces el criterio de cuantía, que supera los 15.000 euros.

II.2. CUANTÍA.

Cumpliendo lo prevenido en el art. 253.1 LEC, hacemos constar que la cuantía de esta demanda es de 600.000 euros, con arreglo a la regla 2.ª del art. 251 LEC, puesto se trata de pleito relativo a la recuperación de un bien inmueble, en decir condena de dar la finca, sin perjuicio de que procede de una ineficacia contractual, siendo dicho el valor corriente a la fecha, de conformidad con el dictamen pericial que se presenta como documento n.º [NÚMERO].

II.3. REQUISITOS FORMALES.

No aparecen, aparte de los requisitos genéricos de la demanda en juicio ordinario del art. 399 LEC, otros de carácter formal cuya falta, por el tipo de acción, invalidarían el proceso para pronunciarse sobre el fondo del asunto.

La presente demanda cumple, asimismo, con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

III.- FONDO DE LA CUESTIÓN CONTROVERTIDA.

Se ejercita la acción de rescisión del art. 621-46 CCC, el cual dispone que el contrato de compraventa y los demás de carácter oneroso pueden rescindirse si la parte perjudicada prueba que, en el momento de la conclusión del contrato, el valor de mercado de la prestación que recibe es inferior a la mitad del valor de mercado de la prestación que realiza.

Del análisis del actual art. 621-46 CCC puede concluirse que, a diferencia de lo que acontecía en la Compilación de Derecho Civil de Cataluña (art. 321), el ámbito de aplicación de la rescisión por lesión no se limita a los contratos onerosos sobre bienes inmuebles, sino que se concede tanto para inmuebles como para muebles, y cabe en beneficio no solo del enajenante sino de cualquiera de las partes contractuales que sufra la lesión.

Pero en el vigente Derecho civil catalán sigue teniendo hoy esta institución una naturaleza jurídica objetiva, independiente, pues, de los vicios de consentimiento que hayan determinado la manifestación de voluntad. Así procede cuando "el valor de mercado de la prestación que se recibe es inferior a la mitad de valor de mercado de la prestación que se realiza", a diferencia de lo que ocurre en el Derecho Navarro (Ley 499 del Fuero Nuevo: ‘Quien haya sufrido lesión enorme, a causa de un contrato oneroso que hubiere aceptado por apremiante necesidad o inexperiencia, podrá pedir la rescisión del mismo’), y a diferencia de los que pudiera inducir a pensar su denominación tradicional de ‘engany a mitges’.

Por ello, no se incide aquí en la eventual concurrencia de dolo en la parte demandada, ni del error inducido, derivado de la edad y situación física y psíquica del demandante, como vicios invalidantes, sino que se parte de la base de que el precio es una estricta compensación del valor de la cosa recibida, causalizándose, en consecuencia, el sinalagma o equivalencia de prestaciones, lo que excluye cualquier elemento en aquél ajeno a dicha consideración, y por ello se excluyen los contratos conmutativos aleatorios o litigiosos, o teñidos ‘animus donandi’ (SSTSJ Catalunya de 2 de octubre y 7 de noviembre de 1998).

En el supuesto presente, los dos primeros negocios en documentos públicos entre mi mandante y los codemandados, en definitiva, articulan una operación de permuta, de una finca actual, llamada [NOMBRE DE LA FINCA] ‘ en el año [AÑO], por seis solares urbanizados en determinadas condiciones al de un determinado tiempo, con lo que se cubría un valor en cambio prefijado equivalente al precio fiduciario de [IMPORTE] euros, lo cual, desde la perspectiva de esas escrituras públicas (documentos [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]), nada tenía de lesivo para D./Dña. [NOMBRE Y APELLIDOS]

La lesión se produce con la segunda escritura de las de año y medio después, la cual se pretende rescindir para recuperar los derechos y obligaciones acordados previamente.

La novación contractual, por un lado, se regula como una forma de extinguir obligaciones (art. 1.156 CCiv), aunque por otro, es contemplada también como una fórmula de sustitución de una obligación por otra (art. 1.204 CCiv), y no se puede eludir que el art. 1.203 CCiv permite la modificación, sin extinción, de las obligaciones por variación, tanto de elementos subjetivos como objetivos (permite alterar el objeto y las condiciones principales de las obligaciones). De ello ha construido la jurisprudencia una doctrina tradicional de distinción entre las dos clases de novaciones, la propia o extintiva, y la impropia o modificativa [SSTS de 24 de febrero de 1984 ó 19 de noviembre de 1993, Rec. 925/1991], y para detectar la calificación apropiada se acude a la voluntad de las partes en relación con la significación económica de la modificación introducida en el vínculo jurídico [SSTS de 26 de mayo de 1981, 8 de octubre de 1986 ó 29 de noviembre de 1991], teniendo en cuenta todas las circunstancias concurrentes en cada caso [SSTS de 26 de octubre de 1985, 16 de diciembre de 1987 ó 27 de noviembre de 1990], aunque exigiendo siempre la acreditación, sin ningún género de duda, de la voluntad inequívoca de los contratantes (SSTS de 1 de diciembre de 1989, 21 de noviembre de 1991, 12 de mayo de 1993 ó 3 de febrero de 1994].

En el caso de autos, se evidencia en los actos documentados notarialmente y que se acompañan como documentos [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO] una novación propia o extintiva, por la voluntad incuestionable de las partes, de manera que D./Dña. [NOMBRE Y APELLIDOS] y los demandados, que actúan sociedad y administrador social de consuno, extinguieron la primigenia permuta e instauraron una verdadera compraventa. D./Dña. [NOMBRE Y APELLIDOS], entonces, concedió carta de pago por el total importe de la cantidad de [IMPORTE] euros a [NOMBRE DE LA PARTE], en un acto, y en el segundo, de la misma fecha, dejaron D./Dña. [NOMBRE Y APELLIDOS] y la indicada sociedad sin efecto ni valor el acuerdo antecedente, con referencia a escrituras realizadas en la misma Notaría, y expresión de sus fechas y números respectivos de protocolos, manifestando no tener los intervinientes nada que reclamarse entre sí por dicho concepto.

Resulta, pues, obvio que la acción de rescisión se dirige a privar de eficacia al contrato de compraventa perfeccionado con extinción de la primitiva convención de permuta, en que el objeto transmitido es la finca [FINCA] ‘, en la situación que entonces tenía, sin acabar su proceso de urbanización, y el precio único pactado fueron los [IMPORTE] euros.

Si conforme al art. 621-46 CCC para apreciar la existencia de la lesión se debe atender al valor de mercado de la prestación en el momento de la conclusión del contrato, sin perjuicio de que el contrato se consumara más tarde, se sigue que el valor de mercado de la finca [FINCA] ‘ debe determinarse en el punto temporal en que la cuarta escritura (documento [Nº DE DOCUMENTO]) extinguió por novación la segunda escritura del año [AÑO] (documento [Nº DE DOCUMENTO]). Es decir, hay que comparar si en ese nuevo momento, que es cuando los demandados consiguen dejar de tener la obligación de entregar seis solares urbanizados, en las condiciones pactadas (objeto al que mi representado, D./Dña. [NOMBRE Y APELLIDOS] tenía derecho, y lo pierde a cambio de una cantidad de dinero), valía más del doble de [IMPORTE] euros.

Puesto que el precio de los seis solares debidamente urbanizados que se tenían que entregar al actor el [FECHA] tenía un valor mínimo en el momento en que se deja de tener la obligación por la declaración de voluntad del actor de [IMPORTE] euros, conforme al dictamen pericial que se deduce, y en cambio no se habían recibido más que [IMPORTE] euros según la carta de pago del mismo día, debe considerarse probada la rescisión por lesión en más de la mitad del precio justo.

Cumpliéndose todos los requisitos de la acción rescisoria, debe pronunciarse su consecuencia jurídica, consistente en la restitución de la cosa objeto del contrato, volviéndose así a la situación existente antes de la celebración del contrato lesivo.

Disponía el art. 324 de la Compilación de Derecho Civil de Cataluña que "será aplicable a la rescisión lo dispuesto en el art. 1.295 del Código Civil", a saber, que "la rescisión obliga a la devolución de las cosas que fueron objeto del contrato con sus frutos, y del precio con sus intereses...". Pero el art. 324 de la Compilación añadía que "... no tendrán que ser restituidos los frutos o intereses anteriores a la reclamación judicial, y habrán de ser abonados los gastos extraordinarios de conservación o refacción y las mejoras útiles".

Aunque la actual regulación no contiene ninguna remisión a los efectos de la rescisión en el Código Civil no parece que haya obstáculo en acudir al Derecho supletorio para integrar la laguna, y si tenemos en cuenta que el contrato, aunque lesivo, es válido y perfecto, y mientras el contrato no se rescinda, el adquirente es verdadero propietario y poseedor de buena fe, mientras no se suscite el pleito, hará suyos los frutos, así como el vendedor hace suyos los intereses del precio. La rescisión del contrato opera ex nunc, por lo que sólo se deberán frutos e intereses desde el día de la interposición de la demanda, momento en el que cesa la buena fe.

Así:

1.º) Los demandados han de reintegrar la finca objeto de compraventa (la totalidad de la finca que inicialmente era la finca registral n.º [NÚMERO], parcela catastral n.º [NÚMERO]), para el caso de que todavía esté sin urbanizar.
2.º) De haber producido frutos la finca se habrán de restituir los posteriores a la reclamación judicial.
3.º) Los demandados han de satisfacer a mi poderdante los intereses legales del precio pagados desde esa reclamación.
4.º) Igualmente el demandante ha de satisfacer a los demandados, caso de producirse la devolución, las impensas extraordinarias de conservación o refacción de la finca, y las mejoras útiles.

-Acción de complemento del precio.

Subsidiariamente, para el caso de que la finca haya experimentado una transformación urbanística que suponga una alteración de ésta que imposibilite devolverla al actor, no es viable la rescisión del contrato mediante devolución de prestaciones, sino que comportará que los demandados deban completar el precio abonado hasta llegar al precio justo, por lo que habrán de pagar a D./Dña. [NOMBRE Y APELLIDOS] la cantidad de [IMPORTE] euros.

IV. COSTAS.

Conforme al principio del art. 394.1 LEC, del vencimiento objetivo, las costas irrogadas a esta parte en el juicio declarativo en la primera instancia se han pronunciar a cargo de los demandados.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito, con sus copias, documentos y pericias que se acompañan, se sirva admitir uno y otros; en su virtud tener por interpuesta en la representación que ostento, la presente demanda de Juicio declarativo Ordinario contra [PARTE DEMANDADA], y D./Dña. [NOMBRE Y APELLIDOS], quienes deberán ser emplazado en legal forma, y previos los oportunos trámites legales, en su día se sirva dictar sentencia por la que:

1.°.- Se declare la rescisión de los contratos de fecha [FECHA], entre demandante y demandados, que sustituyeron a los primigenios acuerdos de fecha [FECHA].
2.°.- Se condene a quedevuelva al demandante la finca‘, cuyas referencias registrales y catastrales constan en el cuerpo de este escrito, estando obligado el demandante, entonces, a devolver el precio recibido, más lo que importen los gastos extraordinarios de conservación de la finca, y los útiles.
3.º.- Se condene a que los demandados, conjunta y solidariamente, restituyan, en su caso, los frutos producidos por la finca indicada con posterioridad a la fecha de interposición de esta demanda, y le indemnicen en los intereses legales del precio desde dicha fecha.
4.º.- Para el caso de que la finca haya experimentado una transformación urbanística que suponga una alteración de ésta que imposibilite devolverla al actor, se condene a los demandados a que, conjunta y solidariamente, paguen al demandante la cantidad deeuros (euros).
5.°.- Se condene en costas a los demandados.

Es justicia de hacerse en [LUGAR], a [FECHA].

OTROSÍ PRIMERO DIGO: Se acompaña dictamen pericial, con arreglo a los arts. 335 y 336.1 LEC, que hace documento n.º [NÚMERO], emitido en debida forma, en nombre de [NOMBRE DEL REPRESENTADO/A], por D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle

OTROSÍ SEGUNDO DIGO: Que siendo general para pleitos el poder que presenta el Procurador/a suscrito, y precisándolo para otros usos.

Por lo expuesto,

AL TRIBUNAL SUPLICO que, teniendo por hechas las afirmaciones anteriores, y por presentadas pruebas periciales, se admitan y quede anunciada su proposición como prueba, así como que acuerde el desglose de la copia auténtica del poder para pleitos y la devolución a esta parte.

Firma del Abogado/a	Firma del Procurador/a
