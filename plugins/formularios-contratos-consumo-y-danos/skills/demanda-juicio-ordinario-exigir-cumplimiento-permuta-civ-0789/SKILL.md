---
name: demanda-juicio-ordinario-exigir-cumplimiento-permuta-civ-0789
description: "Demanda de juicio ordinario para exigir el cumplimiento de una permuta inmobiliaria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para exigir el cumplimiento de una permuta inmobiliaria

> Formulario **CIV-0789** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en ejercicio de acción de cumplimiento de contrato de permuta inmobiliaria.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para exigir el cumplimiento de una permuta inmobiliaria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para exigir el cumplimiento de una permuta inmobiliaria” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-exigir-cumplimiento-permuta-civ-0789`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (8 veces)
- [ ] NÚMERO (8 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] IMPORTE (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] ENTIDAD BANCARIA
- [ ] FECHAS
- [ ] FINCA
- [ ] LUGAR
- [ ] Nº
- [ ] SEDE
- [ ] SUCURSAL
- [ ] TOMO

## Normas que cita el formulario

- art. 21 LOPJ
- art. 36 LEC
- art. 85 LOPJ
- art. 45 LEC
- art. 51 LEC
- art. 10 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.089 Código Civil
- art. 1.124 Código Civil
- art. 1.157 Código Civil
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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], conforme acredito con escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales con el nº [NÚMERO], y con la asistencia del Letrado D./Dña. [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], cuyo despacho está abierto en esta población, calle [CALLE], ante la Sección Civil del Tribunal de Instancia que por turno de reparto corresponda, comparezco y, como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito, y en la representación acreditada, promuevo demanda de Juicio Ordinario, ejercitando acción sobre cumplimiento de contrato de permuta, contra la entidad [DENOMINACIÓN SOCIAL], para ser citada en su oficina de [SUCURSAL], calle

Se basa en los siguientes:

HECHOS

PRIMERO.- En [FECHA] D./Dña. [NOMBRE Y APELLIDOS], administrador único de la mercantil [DENOMINACIÓN SOCIAL]., se puso en contacto con mi representado, como propietario de un solar en la localidad de [LOCALIDAD], de [Nº] metros cuadrados, inscrito en el Registro de la Propiedad de [LOCALIDAD], al Tomo [TOMO], finca registral [FINCA], proponiendo la permuta de dicho solar a cambio de un porcentaje del 30% de la obra total del edificio de viviendas que se comprometía a construir la citada entidad

SEGUNDO.- El [FECHA], mi representado, como propietario del solar, otorgó junto a D./Dña. [NOMBRE Y APELLIDOS] en calidad de administrador único de [DENOMINACIÓN SOCIAL], como adquirente, la correspondiente escritura pública de permuta - cesión de solar a cambio de fincas de obra futura, que debía entregar ésta a aquéllos, constituyendo la citada mercantil una hipoteca sobre el solar para garantizar el préstamo hipotecario por importe [IMPORTE] euros que, en el mismo acto, le concedió CAJA DE AHORROS DEL [ENTIDAD BANCARIA] para ejecutar el edificio.

Adjuntamos, como DOCUMENTO N.º [NÚMERO], copia de la citada escritura de permuta, autorizada por el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA], con el número [NÚMERO] de su protocolo, que fue debidamente inscrita en el Registro de la Propiedad de

Mediante la referida escritura pública de permuta mi mandante transmitió la propiedad de su parcela a [DENOMINACIÓN SOCIAL], a cambio de que esta sociedad le entregara un 30% de la construcción total, según unos coeficientes acordados por las partes, cuyo documento en el que se estipulaban los mismos, y se valora en el 30% de la construcción total, denominado "coeficientes de ponderación acordados por planta y finca", se hallaba incorporado como anexo firmado por ambas partes a la propia escritura de permuta por el Notario autorizante de la misma.

TERCERO.- [DENOMINACIÓN SOCIAL], tras obtener la oportuna licencia del Ayuntamiento de [LOCALIDAD] inició las obras de edificación en el plazo previsto, si bien por causas que se desconocen por mi mandante, las obras se paralizaron el [FECHA], abandonando los empleados de dicha sociedad las mismas sin ofrecer mayor explicación. La construcción se encuentra inacabada, encontrándose en pie la estructura general del edificio, y varios de los pilares maestros de cada planta.

Se aporta como DOCUMENTO N.º [NÚMERO] un reportaje fotográfico de la situación actual de la obra, que coincide con el estado en que se abandonó la obra, hace ahora seis meses. Se acompaña también como DOCUMENTO N.º [NÚMERO], el plano del proyecto de edificación, elaborado por el arquitecto D./Dña. [NOMBRE Y APELLIDOS], en el que se puede apreciar como debía culminarse la misma, y el presupuesto de la obra, como DOCUMENTO N.º [NÚMERO].

CUARTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, se ha requerido extrajudicialmente a la demandada para que cumpliera con lo pactado y continuara la edificación hasta terminarla, entregando la edificación pactada a mi mandante, mediante Burofax de fecha [FECHA] (DOCUMENTO N.º [NÚMERO]), primero, y después, mediante requerimiento notarial efectuado el [FECHA] (DOCUMENTO N.º [NÚMERO]), fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, sin que hasta la fecha se haya ofrecido contestación alguna.

Esta conducta fuerza la presentación de la demanda.

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Los arts 21 y 22 LOPJ y art. 36 LEC atribuyen con carácter general a la jurisdicción de nuestro Estado y al orden civil, el conocimiento de una materia como la presente.

El art. 85 LOPJ y art. 45 LEC, designan a los Tribunales de Instancia, concretamente a la Sección Civil, como los órganos con la competencia específica objetiva y funcional para resolver estos pleitos.

Finalmente, el art. 51 LEC fija que la competencia territorial general, en el caso de personas jurídicas o entidades sin personalidad, será del órgano del lugar de su domicilio.

II.- TRAMITACIÓN.

En aplicación de los arts. 248.3, 249.2 y 251.2.ª LEC, y en atención al valor de la construcción a recibir, aplicando el porcentaje del 30% sobre el presupuesto de la obra antes mencionado, se fija la cuantía en [IMPORTE] euros ( €), debiéndose tramitarse este pleito por las normas de proceso declarativo llamado Juicio Ordinario.

III.- LEGITIMACIÓN Y POSTULACIÓN.

El art. 10 LEC legitima para comparecer y actuar en juicio a los titulares de la relación jurídica o del objeto litigioso. En el caso de autos, el demandante y la mercantil demandada son los sujetos titulares del contrato cuyo íntegro cumplimiento se exige, existiendo, pues, legitimación directa ordinaria. El demandante es titular del crédito derivado de la permuta concertada, habiendo cumplido su prestación, y no habiendo recibido la construcción convenida. Está legitimada pasivamente la demandada por ser la permutante en el siempre citado contrato de permuta, consecuente obligada a la entrega de la construcción terminada.

En aplicación de los arts. 23 y 31 LEC, las partes comparecerán representadas por Procurador/a de los Tribunales y asistidas por Letrado en ejercicio, ambos habilitados ante el Tribunal.

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- FONDO DEL ASUNTO.

Según declara el art. 1.089 del Código Civil, que abre el Libro de obligaciones y contratos, "las obligaciones nacen de los contratos " y añade el 1.091 "las obligaciones que nacen de los contratos tienen fuerza de ley entre las partes contratantes y deben cumplirse al tenor de los mismos".

El Título II del dicho libro del Código comienza con el art. 1.254, que nos define el contrato: "existe desde que una o varias personas consienten en obligarse, respecto de otra u otras, a dar alguna cosa o prestar algún servicio".

En el art. 1.538, describe el contrato de permuta: "La permuta es un contrato por el cual cada uno de los contratantes se obliga a dar una cosa para recibir otra".

De la regulación legal contenida en los arts. 1.538 a 1.541 del propio Código civil, se desprende la catalogación como de un contrato consensual, que se perfecciona por el mero consentimiento, bilateral por ser productor de obligaciones recíprocas, a título oneroso, y conmutativo.

En el caso de Autos el contrato de permuta que unía a mi mandante y a la demandada se plasmó por escrito en documento público, autorizado por Notario.

El artículo 1.124 del Código Civil señala que "La facultad de resolver las obligaciones se entiende implícita en las recíprocas, para el caso de que uno de los obligados no cumpliere lo que le incumbe. El perjudicado podrá escoger entre exigir el cumplimiento o la resolución de la obligación, con el resarcimiento de daños y abono de intereses en ambos casos. También podrá pedir la resolución, aun después de haber optado por el cumplimiento, cuando éste resultare imposible".

En el presente caso, mi mandante, atendiendo al estado actual de las obras, y a su firme propósito de poder disfrutar de una edificación prometida en el solar que fue de su propiedad, opta por reclamar el cumplimiento del contrato de permuta. Y ello, sin que se promueva, por ahora, una reclamación de condena a la indemnización de los daños y perjuicios originados con el retraso en la entrega de la obra, a los efectos de poder facilitar el cumplimiento del contrato a la demandada, ante los problemas económicos que, se supone, está atravesando la misma, y que hayan podido influir en la paralización de la construcción.

Debe invocarse el art. 1.157 del Código Civil, sobre el pago al indicar que no se entenderá pagada una deuda sino cuando completamente se hubiese entregado la cosa o hecha la prestación en que la obligación consistía.

VI.- COSTAS

En aplicación del art. 394.1 LEC deberán imponerse las costas a la parte demandada.

Por lo expuesto

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que acompaño y copias de todo ello, acuerde admitir a trámite la presente demanda, teniendo a quien comparece por parte, con la que se entenderán todas las ulteriores sucesivas diligencias, y dar traslado de la misma a la mercantil demandada en la persona de su representante legal, y seguido que sea el regular procedimiento, se dicte sentencia por la que se condene a la sociedad a entregar a mi mandante el treinta por ciento del edificio de viviendas que se ejecutaban en el solar indicado en la presente demanda, en las condiciones pactadas en el contrato de permuta de fecha [FECHA], con expresa imposición de costas a la sociedad demandada.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
