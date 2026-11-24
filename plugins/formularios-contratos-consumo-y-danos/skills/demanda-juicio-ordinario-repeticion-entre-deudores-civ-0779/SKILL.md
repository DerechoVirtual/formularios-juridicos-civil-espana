---
name: demanda-juicio-ordinario-repeticion-entre-deudores-civ-0779
description: "Demanda de juicio ordinario de repetición entre deudores solidarios condenados. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario de repetición entre deudores solidarios condenados

> Formulario **CIV-0779** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en que un deudor solidario al que le han reclamado la deuda íntegra, reclama, en la vía de regreso, contra el otro deudor solidario condenado por la cuota que le corresponde.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario de repetición entre deudores solidarios condenados» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario de repetición entre deudores solidarios condenados” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-repeticion-entre-deudores-civ-0779`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] FECHA (9 veces)
- [ ] IMPORTE (9 veces)
- [ ] NÚMERO (7 veces)
- [ ] SEDE (5 veces)
- [ ] AÑO (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] CONDICIÓN DE LA PARTE (PROMOTOR/PROPIETARIO) (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] MES (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES Y AÑO
- [ ] NOMBRE DE LA PARTE
- [ ] Nº DE COLEGIADO/A
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 9.2 LOPJ
- art. 5 LEC
- art. 45 LEC
- art. 50 LEC
- art. 249.2 LEC
- art. 10 LEC
- art. 253.1 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.145.I CC
- art. 1.145 CC
- art. 222.4 LEC
- art. 1145.2 Código Civil
- art. 576 LEC
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…ramitó ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta (de dicho Registro) automatizada orientada al dato. Algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC, configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada; se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

(2) El art. 155.3 LEC permite fijar expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes, o apoderados; o, si es asociación que consta en registro oficial; el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, nº [Nº] de teléfono o de fax, dirección de correo electrónico, o similares.

========================================================================

[NOTA DE REVISIÓN: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).]


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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO ORDINARIO EN RECLAMACIÓN DE CANTIDAD euros de principal, más los intereses que legalmente correspondan, contra el arquitecto D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

HECHOS

PRIMERO.- Mi mandante intervino, como promotora y constructora, en la obra de edificación de la vivienda unifamiliar situada en el n.º [NÚMERO] de la calle [CALLE] de [LOCALIDAD], desarrollada entre los meses de [MES] de [AÑO] y [MES] de [AÑO], con licencia de obra otorgada el [FECHA]. Al efecto, se contrató:

— El [CONDICIÓN DE LA PARTE (PROMOTOR/PROPIETARIO)] al arquitecto D./Dña. [NOMBRE Y APELLIDOS], quien se encargó de redactar el proyecto constructivo con fecha de visado [FECHA], y quien se ocupó también de la dirección facultativa de la obra desde su inicio hasta la finalización de la obra. Se acompañan, como documentos n.º [NÚMERO] y [Nº DE DOCUMENTO] de la demanda, copias del contrato y del proyecto constructivo.
— El [CONDICIÓN DE LA PARTE (PROMOTOR/PROPIETARIO)] al aparejador D./Dña. [NOMBRE Y APELLIDOS], quien se encargó de la dirección de ejecución de obra desde la finalización de la obra. Se aporta el contrato indicado como documento n.º [NÚMERO] de la demanda. Dicho profesional no es demandado en el presente procedimiento.

SEGUNDO.- El [CONDICIÓN DE LA PARTE (PROMOTOR/PROPIETARIO)] D./Dña. [NOMBRE Y APELLIDOS], propietario de la citada vivienda unifamiliar interpuso una demanda de juicio ordinario exclusivamente contra mi mandante, y contra los citados arquitecto y aparejador por sus intervenciones en la construcción de aquella. El citado procedimiento se tramitó ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] , como juicio ordinario n.º [Nº DE PROCEDIMIENTO]/[AÑO].

La sentencia dictada en primera instancia en fecha [FECHA], estimó parcialmente la demanda y condenó a mi representada y al arquitecto D./Dña. [NOMBRE Y APELLIDOS], a abonar de forma conjunta y solidaria al actor la cantidad de [IMPORTE] euros, más el interés legal incrementado en dos puntos desde la fecha de dicha resolución y hasta su completo pago, con imposición de costas. Dicha resolución fue recurrida en apelación por mi mandante y el arquitecto D./Dña. [NOMBRE Y APELLIDOS], y confirmada, con imposición de las costas de la segunda instancia, por la sentencia de la Audiencia Provincial de Madrid de fecha 25 de octubre de 2.010. Se adjuntan como documentos n.ºy copia de ambas sentencias.

TERCERO.- En cumplimiento de lo acordado, con fecha [FECHA] mi mandante consignó la cantidad de [IMPORTE] euros, correspondiente al % del importe total de la condena. Se acompaña resguardo de la consignación efectuada en el Tribunal de Instancia como documento n.º [Nº DE DOCUMENTO].

Ante la falta de pago por parte del arquitecto D./Dña. [NOMBRE Y APELLIDOS] del otro 50 de la condena solidaria que le había sido impuesta; D./Dña. [NOMBRE Y APELLIDOS] reclamó el [FECHA] mediante burofax a mi mandante el pago del resto de la condena, en atención a su carácter solidario, advirtiendo de la presentación de una demanda de ejecución con embargo de bienes, en caso negativo. Por ello, [NOMBRE DE LA PARTE] se vio obligada a consignar en la cuenta del Tribunal los otros [IMPORTE] euros el [FECHA], interesando del Tribunal la entrega de esa cantidad a la parte actora. Se aportan copia del burofax y resguardo de la segunda consignación como documentos n.ºy.

CUARTO.- Además de mediante varias conversaciones personales y telefónicas, el [FECHA] mi representada reclamó extrajudicialmente mediante burofax al arquitecto D./Dña. [NOMBRE Y APELLIDOS] el pago de los [IMPORTE] euros, con objeto de repartir por iguales y mitades partes entre las intervinientes condenados, el importe global de la condena. Se acompaña, como documento n.º copia de la citada comunicación.

En consecuencia, dado que todas las gestiones realizadas hasta el momento han sido infructuosas, mi mandante se ve obligado a solicitar el auxilio judicial para intentar recuperar la cantidad abonada correspondiente al aquí demandado. Todo ello, mediante la interposición de la presente demanda, que tiene su base en los siguientes:

FUNDAMENTOS DE DERECHO

I.- Jurisdicción y Competencia

De acuerdo de lo dispuesto en los arts. 9.2 y 21 LOPJ y el art. 5 LEC, el conocimiento del presente litigio corresponde al orden jurisdiccional civil y, en concreto, a las secciones civiles de los tribunales de instancia, en virtud de lo previsto en el art. 45 LEC.

Es competente territorialmente el Tribunal al que tenemos el honor de dirigirnos al tratarse del municipio en el que tiene fijado su domicilio el demandado, tal y como se expone en el encabezamiento, y de desprende de del contrato que, en su momento, ligó a las partes aquí en conflicto (art. 50 LEC).

II.- Procedimiento

De conformidad con lo dispuesto en el art. 249.2 LEC, el presente procedimiento deberá seguirse por los trámites correspondientes al juicio ordinario, al tratarse de una reclamación dineraria de importe superior a 15.000 euros.

III.- Legitimación

A partir de lo dispuesto en el art. 10 LEC, mi mandante ostenta legitimación activa como consecuencia de haber abonado el precio íntegro de la condena solidaria a los dos codemandados en el procedimiento tramitado ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO], como juicio ordinario n.º [Nº DE PROCEDIMIENTO]/[AÑO], como se puede comprobar con los referidos resguardos de consignación, documentos n.º [NÚMERO] y [Nº DE DOCUMENTO] de la demanda.

Y en esta misma línea, la legitimación pasiva del demandado deriva de la misma condena solidaria; sin que exista ningún elemento concreto que permita alterar el porcentaje del 50% que corresponde abonar a cada una de las partes de este procedimiento.

IV.- Cuantía

Cumplimentando la exigencia legal del art. 253.1 LEC, se concreta la cuantía del presente procedimiento en la cantidad de [IMPORTE] euros, como principal reclamado en la vía de regreso frente al deudor solidario.

V.- Postulación

Conforme disponen respectivamente los arts. 23 y 31 LEC, atendiendo a la cuantía y al procedimiento seguido, comparece esta parte asistida de Procurador/a que le representa y Letrado que le defiende, ambos debidamente colegiados y capacitados para actuar ante el Tribunal al cual tengo el honor de dirigirme.

VI.- Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- Fondo del asunto

1.- Acción de regreso:

Tal y como se ha explicado en los hechos del presente escrito rector, tanto mi mandante, como el aquí demandado D./Dña. [NOMBRE Y APELLIDOS], fueron condenados mediante sentencia firme al pago solidario de la cantidad de [IMPORTE] euros. Respecto a dicho importe, mi representada ha abonado la cantidad íntegra, en un primer momento la parte que le correspondía, [IMPORTE] euros, y, tras requerimiento extrajudicial del acreedor, la parte correspondiente al arquitecto, por importe de otros [IMPORTE] euros, cumpliendo con lo dispuesto en el art. 1.145.III CCiv, "La falta de cumplimiento de la obligación por insolvencia del deudor solidario será suplida por sus codeudores, a prorrata de la deuda de cada uno." En este sentido, ninguna excepción podía oponer mi mandante al propietario de la vivienda que obtuvo la sentencia condenatoria y que le reclamaba el pago íntegro, al ser un deudor solidario, según se dispone en la sentencia indicada, documento n.º [NÚMERO] de la demanda.

Hasta la fecha, a pesar del requerimiento realizado al otro deudor solidario, mi mandante no ha visto reembolsada cantidad alguna, por lo que procede ejercitar la acción de regreso del art. 1.145 CCiv "El que hizo el pago sólo puede reclamar de sus codeudores la parte que a cada uno corresponda, con los intereses del anticipo." Y así, no habiendo diferenciado la sentencia condenatoria cuota alguna de responsabilidad de las partes condenadas; y no existiendo elementos de hecho para ello, cada uno debía abonar la mitad de la condena, por lo que se reclama la cantidad de 70.000 euros, que se corresponde con el segundo pago realizado. En este sentido, el Tribunal Supremo ha acogido la posibilidad de ejercitar esta acción de repetición en supuestos como el presente en numerosas sentencias, entre las que podemos citar las de 25 de octubre de 1.988, de 8 de mayo de 1.991, de 11 de julio de 1.992, de 10 de octubre de 1.992, de 29 de septiembre de 1.993 o de 22 de septiembre de 1.994.

2.- Responsabilidad del demandado, cosa juzgada:

El demandado no puede oponer ninguna suerte de alegación en relación a su responsabilidad, ya que la misma fue declarada mediante sentencia dictada por el Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO] el [FECHA]; en la que, tras haber podido contestar a la demanda y desplegar su defensa sin causa de indefensión alguna, fueron desestimados los argumentos exculpatorios, sin que pueda sostener aquí otras alegaciones distintas en su defensa, que debieron ser articuladas en el anterior proceso.

Revistiendo dicha resolución judicial el carácter de firme, opera el efecto de cosa juzgada positiva previsto en el art. 222.4 LEC, según el cual "lo resuelto con fuerza de cosa juzgada en la sentencia firme que haya puesto fin a un proceso, vinculará al tribunal de un proceso posterior, cuando en éste aparezca como antecedente lógico de lo que sea su objeto, siempre que los litigantes de ambos procesos sean los mismos....". Sobre dicha base legal, señala el Tribunal Supremo en la sentencia de su Sala 1.ª con fecha 27 de Febrero de 2004, rec. 909/1998, que "la eventual repetición habrá de respetar lo así resuelto o declarado, en una suerte de efecto prejudicial evitatorio de la posible contradicción en las resoluciones o hasta vulneración del "non bis in idem". Quiere subrayarse, pues, que lo que está enjuiciado o valorado en anterior proceso, ha de vincular, en concreto en el siguiente contenido en la pretensión de repetición."

En esta misma línea, una consolidada línea de jurisprudencia menor, como la sentencia de la Audiencia Provincial de Vizcaya de 1 de febrero de 2.010, rec. 374/2009 o la sentencia de la Audiencia Provincial de Valencia, Sección 2.ª, de 15 de Julio de 1998, rec. 116/1998, la cual dispone que "en modo alguno puede tolerarse la reproducción o revisión de una decisión judicial firme anterior, en la que pudieron y debieron utilizarse todos los argumentos en favor de las respectivas tesis defensivas de las posiciones de las partes, como tan acertada y categóricamente recoge la sentencia impugnada, sin que se haya aportado ni un solo argumento jurídico o fáctico contrario a la procedencia de la acción o derecho de regreso que se ejercita por el actor y se concede por la juzgadora de primera instancia. Esta pretensión, tipificada en el artículo 1145.2 del Código Civil, está fundamentada en la interdicción del enriquecimiento sin causa y cuyo único presupuesto es la validez y eficacia del pago liberador efectuado por el regresante, cuyo importe se acredita con el resguardo de ingreso, obrante al folio 16, de fecha 11 de julio de 1997, y por el importe cuya mitad se reclama".

En consecuencia, al encontrarse determinada y cuantificada judicialmente la responsabilidad del demandado, y dado que mi mandante ha abonado la cantidad que le correspondía pagar, procede estimar la demanda y condenarle al pago del principal.

VIII.- De los intereses

El citado art. 1.145 CCiv establece que el deudor solidario que abonó el importe de la deuda puede reclamar al resto de deudores "la parte que a cada uno corresponda, con los intereses del anticipo". En consecuencia, la cantidad reclamada devengará intereses desde la fecha del abono de la cantidad, 25 de noviembre de 2.010. Asimismo, a partir de la fecha de la sentencia y den virtud de lo dispuesto en el art. 576 LEC, los intereses serán los correspondientes al interés legal incrementado en dos puntos.

IX.- Costas

Las costas deberán ser impuestas al demandado, en virtud del criterio del vencimiento recogido en el art. 394 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito con la documentación que se acompaña, se sirva admitirlos y, en su virtud, tenga por formulada demanda de juicio ordinario contra el Arquitecto D./Dña. [NOMBRE Y APELLIDOS], previos los trámites pertinentes, dicte en su día sentencia por la que, estimándola, se condene al demandado a rembolsar a mi mandante la cantidad de [IMPORTE] euros, más los intereses legales desde el [FECHA], con expresa imposición de las costas del procedimiento. Por ser así de justicia, que pido en [LUGAR], a [DÍA] de [MES Y AÑO].

OTROSI DIGO que, para el improbable supuesto de que alguno de los hechos descritos en la presente demanda fuera negado por el demandado, o que la autenticidad de alguno de los documentos aportados fuera impugnada de adverso, o que los documentos aportados se consideren insuficientes para acreditar los hechos de los que trae causa la presente reclamación, designamos, a efectos probatorios, los archivos del Tribunal de Instancia de [SEDE], plaza n.º Madrid, como juicio ordinario n.º 29/09. Por ser igualmente de justicia, que pido en el mismo lugar y fecha.

Firma del Abogado/a	Firma del Procurador/a
