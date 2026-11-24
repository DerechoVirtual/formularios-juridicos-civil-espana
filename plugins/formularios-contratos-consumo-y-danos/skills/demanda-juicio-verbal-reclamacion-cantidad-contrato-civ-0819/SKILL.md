---
name: demanda-juicio-verbal-reclamacion-cantidad-contrato-civ-0819
description: "Demanda de juicio verbal de reclamación de cantidad por contrato de obra entre 2.000 y 15.000 euros. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal de reclamación de cantidad por contrato de obra entre 2.000 y 15.000 euros

> Formulario **CIV-0819** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio verbal sobre reclamación de cantidad, superior a 2.000 euros e inferior a 15.000 euros, por arrendamiento de obra.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal de reclamación de cantidad por contrato de obra entre 2.000 y 15.000 euros» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal de reclamación de cantidad por contrato de obra entre 2.000 y 15.000 euros” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-verbal-reclamacion-cantidad-contrato-civ-0819`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] FECHAS
- [ ] IMPORTE EN CIFRA
- [ ] LUGAR
- [ ] MARCA/MODELO
- [ ] MATRÍCULA
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 437.1 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 50.1 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.544 CC
- art. 1.100 CC
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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO VERBAL SOBRE RECLAMACIÓN DE CANTIDAD, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II con relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Todo ello de conformidad con los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO

Mi mandante se dedica a la reparación de vehículos de motor, ejerciendo su profesión en esta localidad, calle [CALLE], donde radican sus talleres mecánicos y de chapa, y satisfaciendo por ello la correspondiente contribución y estando en posesión de la preceptiva licencia fiscal que ampara su actividad.

SEGUNDO

El demandado D./Dña. [NOMBRE Y APELLIDOS] se personó en el taller de reparaciones de mi representado, trayendo el vehículo de su propiedad marca [MARCA/MODELO] y matrícula [MATRÍCULA], encargándole a mi mandante su reparación en la parte mecánica, por los problemas de funcionamiento que había observado, así como en los de chapa y pintura a causa de varios golpes y arañazos que presentaba la carrocería en su parte delantera, aceptando mi mandante el encargo bajo la fórmula de presupuesto previo.

TERCERO

En cumplimiento del encargo, por mi mandante se examinó el vehículo y se comprobaron las partes de su mecánica en mal estado, así como el estado de la carrocería en su parte dañada, elaborando el correspondiente presupuesto de reparación, que alcanzaba la cantidad de [IMPORTE] euros, que le fue comunicado al demandado, que mostró su conformidad y dio orden de reparación.

CUARTO

Verificada la reparación del vehículo, se puso a disposición del demandado, junto con la factura correspondiente, que estaba en consonancia con el presupuesto previo aceptado, personándose el demandado en el taller y retirando de su propia mano el susodicho vehículo, ofreciendo pagar el importe de la reparación en el día siguiente o en los más próximos, lo que aceptó mi mandante guiado por su buena fe, pero que no encontró la justa correspondencia en el comportamiento posterior del demandado, que ha hecho caso omiso a los diversos requerimientos de pago que se le han hecho, dando largas al asunto y sin dar ninguna satisfacción a mi cliente.

QUINTO

La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo posteriores negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en el art. 85.1 LOPJ y art. 45 LEC, y puesto que no está prevenido un fuero preceptivo específico, resulta territorialmente competente el Tribunal a que me dirijo, puesto que es el del partido del lugar donde tiene su domicilio el demandado, que es el fuero general de las personas físicas (art. 50.1 LEC).

II.- PROCEDIMIENTO

El juicio verbal a que se refieren los arts. 248, 250.2 y 437 y ss. LEC.

III.- LEGITIMACIÓN ACTIVA Y PASIVA

Corresponde al demandante la activa por ser la parte que ha cumplido sus obligaciones y no percibido la prestación debida; la pasiva la tiene el demandado en cuanto obligado a satisfacer el precio debido por los servicios que se le han prestado.

IV.- CUANTÍA DE LA DEMANDA

La cuantía de la demanda a los efectos de lo dispuesto en el art. 253.1 LEC es la de [IMPORTE] euros ([IMPORTE EN CIFRA] €), en aplicación de la regla 1.ª del art. 251 LEC, según el cual si se reclama una cantidad de dinero determinada, la cuantía de la demanda estará representada por dicha cantidad.

De ahí procede la preceptividad de la representación por procurador y la defensa por abogado, conforme a los arts. 23.2.1.º y 31.2.1.º LEC.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.- FUNDAMENTOS DE DERECHO MATERIALES O SOBRE EL FONDO DEL ASUNTO

La relación contractual entre partes constituye un arrendamiento de obra, ya que en virtud del mismo una de las partes se obliga a ejecutar una obra (reparar un vehículo), y la otra se compromete a pagar por ello un precio cierto (art. 1.544 CCiv).

Artículo 1.089 CCiv en cuanto establece que las obligaciones nacen de la Ley, de los contratos y otros supuestos; estas obligaciones nacidas de los contratos son recogidas en el art. 1.091 del mismo Texto previniendo que las mismas tienen fuerza de Ley entre las partes y habrán de ser cumplidas a tenor de los mismos.

Articulo 1.599 CCiv que previene que si no hubiere pacto o costumbre en contrario el precio de la obra deberá pagarse al hacerse la entrega.

Citamos asimismo el art. 1.100 CCiv en cuanto a la aplicación de la mora y el 1.108 del mismo Texto que previene que si el deudor incurre en mora, y no habiendo pacto en contrario, la indemnización de daños y perjuicios consistirá en el interés legal.

VII.- COSTAS

Conforme al art. 394.1 LEC, las costas procesales han de imponerse a la parte demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que tenga por presentado este escrito con sus documentos y copias de todo ello, teniéndome por comparecido y parte en la representación que ostento, y ordenando se entiendan conmigo las sucesivas actuaciones; se sirva admitir a trámite la demanda de juicio verbal que se interpone, acuerde dar traslado al demandado para que comparezca y la conteste, y seguido el juicio por sus trámites, se venga a dictar sentencia que condene al demandado al pago de la cantidad de [IMPORTE] euros que se reclama como principal, más los intereses moratorios correspondientes devengados desde la fecha de interposición de la demanda, con costas procesales.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
