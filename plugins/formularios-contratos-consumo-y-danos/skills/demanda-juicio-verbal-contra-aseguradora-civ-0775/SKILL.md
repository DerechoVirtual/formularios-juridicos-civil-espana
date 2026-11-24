---
name: demanda-juicio-verbal-contra-aseguradora-civ-0775
description: "Demanda de juicio verbal contra la aseguradora por incumplimiento del seguro combinado del hogar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal contra la aseguradora por incumplimiento del seguro combinado del hogar

> Formulario **CIV-0775** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio declarativo ejercitando acción contra aseguradora por incumplimiento de contrato de seguro combinado del hogar

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal contra la aseguradora por incumplimiento del seguro combinado del hogar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal contra la aseguradora por incumplimiento del seguro combinado del hogar” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-verbal-contra-aseguradora-civ-0775`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] FECHA (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] ASEGURADORA (3 veces)
- [ ] CALLE (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] DIRECCIÓN (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] Nº (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] DOMICILIO
- [ ] LETRA
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] Nº DE PÓLIZA
- [ ] SEDE
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 9.2 LOPJ
- art. 45 LEC
- art. 68 LEC
- art. 52.2 LEC
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 10 LEC
- art. 1 LCS
- art. 1157 CC
- art. 251 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 18 LCS
- art. 20 LCS
- art. 394 LEC
- art. 309 LEC
- art. 337.2 LEC

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
- Junto a «…objetiva y funcional (art. 45 LEC) la Sección Civil del Tribunal de Instancia de»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) La opción del modelo, con las adaptaciones precisas, es también aplicable para las reclamaciones que excedan de 15.000 euros, que se tramitarán como juicio ordinario.

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en esta villa, calle [CALLE], n.º [NÚMERO], según acredito con la escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro como documento nº [Nº DE DOCUMENTO]; asistido por el Letrado en ejercicio abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito interpongo DEMANDA DE JUICIO VERBAL en reclamación de cantidad, contra la compañía anónima de seguros [ASEGURADORA], domiciliada en [DOMICILIO], c./ [DIRECCIÓN] n.º [NÚMERO], con base en los siguientes:

HECHOS

PRIMERO

El pasado [FECHA] mi mandante, como titular de la vivienda [DIRECCIÓN] suscribió con la entidad aseguradora demandada una póliza de seguro combinado del hogar a fin de asegurar diversos riesgos en relación con la citada vivienda.

El seguro contratado tenía por objeto la cobertura de los siguientes riesgos expresamente garantizados: incendio, explosión y caída de rayo, gastos de desescombro, actos vandálicos, privación de uso o pérdida de alquileres, daños por agua, rotura de cristales, mármoles y loza sanitaria, robo, expoliación y hurto sobre el continente y el contenido, así como los perjuicios originados por la disminución patrimonial que pudiera derivarse de responsabilidad contraída por daños ocasionados a terceras personas.

En las condiciones generales del contrato, al describir el riesgo de "daños a la vivienda, mobiliario y enseres", causados por incendio, explosión y rayo" (condición [Nº], letra [LETRA]), se dice:

"Mediante esta garantía se indemnizarán los daños y pérdidas materiales causados a los bienes asegurados por un incendio o explosión, tanto si se origina dentro del edificio como en sus proximidades, así como por la caída del rayo aun cuando no se produzca incendio. Quedan también cubiertos:

Los gastos de extinción de incendio ocasionados por la aplicación de las medidas necesarias adoptadas por la Autoridad o por el asegurado, para controlar o para extinguir el incendio o para impedir su propagación.

Los gastos de salvamento que ocasione el transporte de los objetos asegurados, con el fin de salvarlos del siniestro cubierto por esta garantía, así como su estancia en un establecimiento guardamuebles por un período máximo de dos meses.

Los daños ocasionados por la acción del humo que tengan su origen en un incendio o en escapes repentinos que se produzcan en los aparatos de combustión y calefacción, aun cuando dichos eventos sucedan fuera de la vivienda asegurada.

El límite de esta garantía es el 100% de la suma asegurada."

Asimismo, en el apartado de las condiciones generales relativo a las "definiciones", se explica: "Incendio, explosión y rayo: Se entiende por incendio el abrasamiento y combustión con llama capaz de propagarse de un objeto a otros objetos que no estaban destinados a ser quemados en el lugar y el momento en que se produce."

A fin de su acreditación se acompañan a este escrito de demanda como documentos núms. el título de propiedad de la vivienda asegurada, póliza de contrato de seguro, condiciones generales y particulares, y recibo de pago de la prima correspondiente al período comprendido entre [FECHA] y

SEGUNDO

Con fecha [FECHA], como consecuencia de un cortocircuito producido en una base de enchufe eléctrico se declaró un incendio produciéndose daños materiales en la vivienda del demandante consistentes en

TERCERO

Del mencionado siniestro y de sus correspondientes consecuencias mi representado dio oportuno parte a su compañía aseguradora [ASEGURADORA], la demandada, a fin de que ésta tramitase las diligencias pertinentes para la indemnización a mi mandante por los daños sufridos en la vivienda, cuya reparación ascendió a [IMPORTE] €, importe que tuvo que ser pagado por mi representado ante la reiterada oposición de la demandada a reparar y/o pagar la indemnización por entender que dichos daños están excluidos de la cobertura de la póliza, cuya vigencia y certeza no se discute.

Se aportan como documentos núms [Nº DE DOCUMENTO], copia del parte de declaración de siniestro, carta de rechazo del siniestro, atestado policial y facturas de las reparaciones efectuadas por los profesionales contratados por mi poderdante.

CUARTO

A la demandada se le ha reclamado el pago a mi mandante de la indemnización por los daños causados en la vivienda asegurada, objeto de cobertura de la póliza, cuyo coste de reparación ha tenido que ser sufragado por mi representado ante el incumplimiento injustificado de sus obligaciones contractuales, habiendo resultado inútil cualquiera de las gestiones amistosas realizadas para que recobrar de su aseguradora la indemnización derivada del siniestro, por lo que se ve mi patrocinada en la necesidad de acudir al auxilio jurisdiccional.

OCTAVO.- Así, previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A los anteriores hechos les son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Sobre materia de la competencia genérica del orden civil de la jurisdicción (art. 9.2 LOPJ), tiene la competencia objetiva y funcional (art. 45 LEC) la Sección Civil del Tribunal de Instancia de esta villa, que por turno de reparto corresponda (art. 68 LEC), y la territorial, puesto que el domicilio del demandante se halla en la localidad de [LOCALIDAD] (art. 52.2 LEC y 24 LCS).

II.- CAPACIDAD

Mi mandante es persona física, mayor de edad, en pleno ejercicio de sus derechos civiles, por lo que tiene capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC, como lo es la entidad demandada [ASEGURADORA], persona jurídico mercantil con capacidad para ser parte que se reconoce en el art. 6.1.3.º LEC, debiendo comparecer en juicio por medio de sus representantes legales (art. 7.4 LEC).

III.- LEGITIMACIÓN

Como titulares de la relación jurídica litigiosa que actúan como partes (art. 10 LEC), la legitimación activa corresponde a la demandante por ser la parte que ha cumplido sus obligaciones como asegurado en el contrato de seguro (arts. 1 y 7 LCS) y como acreedor frente al incumplimiento contractual de la demandada, en base a los arts. 1157 y 1158 CCiv; y la pasiva la tiene la demandada como entidad aseguradora y parte del contrato de seguro, al amparo de lo dispuesto por el art. 1 LCS y en cuanto deudora por incumplimiento de sus obligaciones contractuales al no haber indemnizado a mi representado por el siniestro producido.

IV.- PROCEDIMIENTO

El juicio verbal a que se refieren los arts. 248, 250.2 y 437 y ss. LEC, por ser la cuantía reclamada inferior a 15.000 euros.

V.- CUANTÍA

La cuantía de la demanda asciende al importe reclamado, conforme a la regla 1.ª del art. 251 LEC, por lo que no quedan excepcionados los litigantes de representación técnica y defensa letrada con Procurador y Abogado habilitados ante el tribunal (arts. 23.1 y 31.1 LEC).

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FONDO DEL ASUNTO

El art. 1 LCS establece que "El contrato de seguro es aquel por el que el asegurador se obliga, mediante el cobro de una prima y para el caso de que se produzca el evento cuyo riesgo es objeto de cobertura a indemnizar, dentro de los límites pactados, el daño producido al asegurado o a satisfacer un capital, una renta u otras prestaciones convenidas", disponiendo el art. 2 que "Las distintas modalidades del contrato de seguro, en defecto de Ley que les sea aplicable, se regirán por la presente Ley, cuyos preceptos tienen carácter imperativo, a no ser que en ellos se disponga otra cosa. No obstante, se entenderán válidas las cláusulas contractuales que sean más beneficiosas para el asegurado".

Se invoca también la aplicación del art. 18 LCS, toda vez que "El asegurador está obligado a satisfacer la indemnización al término de las investigaciones y peritaciones necesarias para establecer la existencia del siniestro y, en su caso, el importe de los daños que resulten del mismo. En cualquier supuesto, el asegurador deberá efectuar, dentro de los cuarenta días, a partir de la recepción de la declaración del siniestro, el pago del importe mínimo de lo que el asegurador pueda deber, según las circunstancias por él conocidas.

Cuando la naturaleza del seguro lo permita y el asegurado lo consienta, el asegurador podrá sustituir el pago de la indemnización por la reparación o la reposición del objeto siniestrado".

Igualmente son de aplicación los arts. 1254 a 1258, sobre interpretación de los contratos, y la clásica batería de preceptos del derecho de obligaciones integrada por los arts. 1088, 1089, 1090, 1091, 1096, 1097, 1101, 1157 y 1158 CCiv.

Innegable que hubo un daño en la vivienda asegurada estando en vigor la póliza de contrato de seguro, habiéndose materializado el riesgo objeto de cobertura, y hallándose mi patrocinado al corriente en el pago de las primas correspondientes a dicha póliza, el asegurador debió pagar el coste de reparación como prestación indemnizatoria derivada del contrato de seguro. Al no hacerlo ha incumplido grave y culpablemente el contrato y debe satisfacer a mi representado el importe de la reparación que ha pagado.

VIII.- INTERESES

Deben reconocerse a mi patrocinado los del régimen especial del art. 20 LCS al haber incurrido en mora la entidad aseguradora demandada.

IX.- COSTAS

Conforme al art. 394 LEC, las costas procesales han de imponerse a la parte demandada.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que tenga por presentado este escrito con sus documentos y copias de todo ello, teniéndome por comparecido y parte en la representación que ostento, y ordenando se entiendan conmigo las sucesivas actuaciones; se sirva admitir a trámite la demanda de juicio verbal que se interpone, acuerde dar traslado al demandado para que comparezca y la conteste, y seguido el juicio por sus trámites, se venga a dictar sentencia que condene al demandado al pago de la cantidad de [IMPORTE] euros que se reclama como principal, más lo que representen los intereses por mora del art. 20 LCS, con costas procesales.

Es Justicia que se pide en [LOCALIDAD]

OTROSÍ PRIMERO DIGO: Que interesa al derecho de esta parte valerse para el acto de la vista de los siguientes medios de PRUEBA:

A) INTERROGATORIO DE LA PARTE CONTRARIA, a fin de que sea citado D./Dña. [NOMBRE Y APELLIDOS], como representante legal de la sociedad demandada, que intervino personalmente en los hechos que justifican la demanda, conforme al art. 309 LEC.

B) DOCUMENTAL consistente en:

- que se remita oficio a la comisaría de la Policía local de [LOCALIDAD], a fin de que remita al Tribunal el atestado n.º [NÚMERO], elaborado por razón del siniestro acaecido el día [FECHA]
- que se requiera a la Compañía de Seguros demandada para aportación a la vista del original de la póliza de seguro [Nº DE PÓLIZA] concertado con el demandante [ÓRGANO]

C) TESTIFICAL, para que se proceda a citar judicialmente a las siguientes personas para ser interrogadas en la vista:

D./Dña. [NOMBRE Y APELLIDOS], de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [CALLE]

D./Dña. [NOMBRE Y APELLIDOS], de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [CALLE]

D) PERICIAL, mediante aportación con este escrito del informe designado como documento n.º [NÚMERO], elaborado por el Técnico del Servicio de Prevención, Extinción de Incendios y Salvamento de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], que podrá ser citado en [LOCALIDAD], para que de conformidad con el art. 337.2 LEC comparezca a la vista, a fin de que exponga su informe, y se sujete a las preguntas, objeciones o propuestas de aclaración, rectificación o ampliación que se le formulen.

En su virtud,

SUPLICO AL TRIBUNAL que, teniendo por causada la precedente solicitud de prueba a los efectos oportunos, se digne ordenar todo lo conducente para su práctica.

OTROSÍ SEGUNDO DIGO: Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II en relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Por lo expuesto,

AL TRIBUNAL NUEVAMENTE SUPLICO que, teniendo por hechas las anterior manifestación, se admita y provea en consecuencia.

Reitero Justicia en lugar y fecha "ut supra".

Firma del Abogado/a	Firma del Procurador/a
