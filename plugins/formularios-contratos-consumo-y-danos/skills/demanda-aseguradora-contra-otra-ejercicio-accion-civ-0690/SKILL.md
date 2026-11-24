---
name: demanda-aseguradora-contra-otra-ejercicio-accion-civ-0690
description: "Demanda de una aseguradora contra otra en ejercicio de la acción de repetición. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de una aseguradora contra otra en ejercicio de la acción de repetición

> Formulario **CIV-0690** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario por la que una aseguradora que ha pagado la totalidad de la indemnización de un siniestro (incendio de un vehículo), existiendo un seguro múltiple o concurrencia de seguros sobre el mismo riesgo e interés, reclama a la otra aseguradora la parte proporcional que le corresponde, mediante la acción de repetición del art. 32 de la Ley de Contrato de Seguro. Formulario adaptado a la reforma procesal de la LO 1/2025.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de una aseguradora contra otra en ejercicio de la acción de repetición» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de una aseguradora contra otra en ejercicio de la acción de repetición” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-aseguradora-contra-otra-ejercicio-accion-civ-0690`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA ASEGURADORA DEMANDADA (3 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA ASEGURADORA DEMANDANTE (3 veces)
- [ ] FECHA (3 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA ENTIDAD TOMADORA (2 veces)
- [ ] IMPORTE ASEGURADO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NIF (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL ARRENDATARIO (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] AÑO
- [ ] COLEGIO DE ABOGADOS
- [ ] CORREO ELECTRÓNICO
- [ ] DOMICILIO
- [ ] DÍA
- [ ] MARCA
- [ ] MATRÍCULA
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] MODELO
- [ ] NOMBRE DEL PERITO
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR
- [ ] Nº DE COLEGIADO
- [ ] NÚMERO
- [ ] PARTES DEL CONTRATO DE RENTING
- [ ] SEDE
- [ ] SUMA ASEGURADA DE LA DEMANDADA
- [ ] SUMA ASEGURADA DE LA DEMANDANTE
- [ ] TELÉFONO
- [ ] TOMADOR

## Normas que cita el formulario

- art. 21 LOPJ
- art. 85 LOPJ
- art. 50 LEC
- art. 51 LEC
- art. 253 LEC
- art. 251.1 LEC
- art. 2 Ley 10/2012
- art. 10 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1145 Código Civil
- art. 1101 Código Civil
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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador/a de los Tribunales, en nombre y representación de [DENOMINACIÓN SOCIAL DE LA ASEGURADORA DEMANDANTE], S.A. de Seguros y Reaseguros (demandante), con NIF n.º [NIF], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO] (colegiado/a n.º [Nº DE COLEGIADO] del Iltre. Colegio de Abogados de [COLEGIO DE ABOGADOS]) y, como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito, y en la representación acreditada, promuevo demanda de juicio ordinario en reclamación de [IMPORTE] euros de principal, más intereses de demora, ejercitando acción de repetición, contra [DENOMINACIÓN SOCIAL DE LA ASEGURADORA DEMANDADA], S.A. de Seguros y Reaseguros, con NIF n.º [NIF], con domicilio en [LOCALIDAD], calle [DOMICILIO], n.º [NÚMERO], provista de teléfono n.º [TELÉFONO] y correo electrónico [CORREO ELECTRÓNICO], con objeto de que, tramitado el procedimiento en legal forma, en su día se dicte sentencia de conformidad con el suplico de esta demanda, que baso en los siguientes

HECHOS

PRIMERO.– Mi representada, [DENOMINACIÓN SOCIAL DE LA ASEGURADORA DEMANDANTE], S.A. de Seguros y Reaseguros, en el ejercicio de su actividad empresarial aseguradora, concertó con [DENOMINACIÓN SOCIAL DE LA ENTIDAD TOMADORA], mercantil dedicada al renting, un contrato de seguro de daños en relación con el bien de su propiedad, el vehículo marca [MARCA], modelo [MODELO] y matrícula [MATRÍCULA]. Entre los riesgos asegurados se encontraba el de incendio, por una cantidad de [IMPORTE ASEGURADO].

En prueba de ello acompañamos como DOCUMENTO Nº 1 la póliza de seguro a que hemos hecho referencia.

SEGUNDO.– El usuario de dicho vehículo era D./Dña. [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL ARRENDATARIO], como titular de un contrato de renting sobre el mismo, concertado con la anteriormente identificada sociedad mercantil [DENOMINACIÓN SOCIAL DE LA ENTIDAD TOMADORA].

D./Dña. [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL ARRENDATARIO] tenía a su vez asegurado el vehículo con la compañía aseguradora [DENOMINACIÓN SOCIAL DE LA ASEGURADORA DEMANDADA], hoy demandada, entre cuyas contingencias aseguradas se encontraba la de incendio, valorándose el vehículo en la cantidad de [IMPORTE ASEGURADO], y ello en cumplimiento de la condición general 6.ª del contrato de renting, en la que se establecía que «el arrendatario asume los riesgos de la pérdida total o parcial del bien arrendado, obligándose a concertar a su cargo un seguro que cubra todos los riesgos».

En prueba de lo expuesto acompañamos como DOCUMENTO Nº 2 el contrato de renting suscrito entre [PARTES DEL CONTRATO DE RENTING], y como DOCUMENTO Nº 3 la póliza de seguro concertada entre [TOMADOR] y la demandada sobre dicho vehículo.

TERCERO.– El [FECHA] se produjo el siniestro por el cual el vehículo resultó destruido de manera total a causa de un incendio.

Tras la oportuna reclamación por parte de la titular del vehículo, y valorándose el mismo en la cantidad de [IMPORTE], según el informe emitido por el perito [NOMBRE DEL PERITO], en fecha [FECHA] mi representada procedió al pago del mismo.

En prueba de ello se acompaña como DOCUMENTO Nº 4 el burofax remitido por la titular del vehículo, como DOCUMENTO Nº 5 el informe pericial de producción del siniestro y valoración del vehículo siniestrado, y como DOCUMENTO Nº 6 el finiquito suscrito por el indemnizado que acredita el pago de la indemnización.

CUARTO.– En consecuencia con lo anteriormente expuesto, dado que mi mandante tenía asegurado el vehículo en [SUMA ASEGURADA DE LA DEMANDANTE] y la demandada en [SUMA ASEGURADA DE LA DEMANDADA], procede aplicar dicha proporción a la cantidad efectivamente abonada por mi representada como consecuencia del siniestro, correspondiendo por lo tanto a la demandada el pago de la cantidad de [IMPORTE], importe objeto de reclamación en la presente litis.

QUINTO.– En atención a las buenas relaciones comerciales que tradicionalmente han existido entre las partes, previamente a la interposición de la presente demanda se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], pero hasta este momento ni se ha solventado la deuda ni se ha ofrecido alternativa alguna.

Por este motivo nos vemos obligados a acudir a la vía judicial, reclamando una solución a nuestra pretensión, que consiste en que la demandada abone a [DENOMINACIÓN SOCIAL DE LA ASEGURADORA DEMANDANTE] (demandante) la cantidad de [IMPORTE] euros.

Se acompaña como documento nº [Nº DE DOCUMENTO].

FUNDAMENTOS DE DERECHO

I.– JURISDICCIÓN Y COMPETENCIA

Los arts. 21 y 22 de la LOPJ y 36 de la LEC atribuyen con carácter general a la jurisdicción de nuestro Estado y al orden civil el conocimiento de esta materia. Los arts. 85 de la LOPJ y 45 de la LEC designan a los Tribunales de Instancia como los órganos que específicamente resolverán estos pleitos (competencia objetiva y funcional). Finalmente, el art. 50 de la LEC fija la competencia territorial general, en el caso de demanda a persona jurídica, atendiendo al domicilio del demandado (en relación con el art. 51 LEC en cuanto a la sucursal).

II.– PROCEDIMIENTO

En aplicación de los arts. 248.2.1.º, 249.2 y 251 de la LEC y en atención a la cuantía reclamada, el pleito se tramitará por el cauce del juicio declarativo ordinario.

III.– CUANTÍA

Según exige el art. 253 de la LEC, fijamos la cuantía de la demanda en [IMPORTE] euros, en atención a lo establecido en el art. 251.1 de la LEC.

[OPCIONAL — si ha lugar]
Acompañamos modelo 696 de autoliquidación de tasa judicial, en cumplimiento de lo exigido por el artículo 2 de la Ley 10/2012, de 20 de noviembre.

IV.– LEGITIMACIÓN

El art. 10 de la LEC legitima para comparecer y actuar en juicio a los titulares de la relación jurídica u objeto litigioso. En este caso, la demandante lo es como acreedora en ejercicio de la acción de repetición, y la demandada, en su condición de deudora.

V.– POSTULACIÓN

En aplicación de los arts. 23 y 31 de la LEC, las partes deberán comparecer representadas por procurador y asistidas por letrado.

VI.– CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

FONDO DEL ASUNTO

PRIMERO.– Se ejercita la acción de repetición contenida en el artículo 32 de la Ley de Contrato de Seguro, según el cual: «Cuando en dos o más contratos estipulados por el mismo tomador con distintos aseguradores se cubran los efectos que un mismo riesgo puede producir sobre el mismo interés y durante idéntico período de tiempo, el tomador del seguro o el asegurado deberán, salvo pacto en contrario, comunicar a cada asegurador los demás seguros que estipule. Si por dolo se omitiera esta comunicación, y en caso de sobreseguro se produjera el siniestro, los aseguradores no están obligados a pagar la indemnización.

Una vez producido el siniestro, el tomador del seguro o el asegurado deberá comunicarlo, de acuerdo con lo previsto en el artículo dieciséis, a cada asegurador, con indicación del nombre de los demás.

Los aseguradores contribuirán al abono de la indemnización en proporción a la propia suma asegurada, sin que pueda superarse la cuantía del daño. Dentro de este límite el asegurado puede pedir a cada asegurador la indemnización debida, según el respectivo contrato. El asegurador que ha pagado una cantidad superior a la que proporcionalmente le corresponda podrá repetir contra el resto de los aseguradores.

Si el importe total de las sumas aseguradas superase notablemente el valor del interés, será de aplicación lo previsto en el artículo 31.»

En este supuesto existe, como contempla el citado artículo, una concurrencia de seguros, porque la contingencia que produjo el siniestro, el incendio, estaba doblemente asegurada, ya que, aunque existan dos tomadores distintos, los seguros concertados con dos aseguradoras distintas cubrían, en idéntico periodo de tiempo, los efectos de un mismo riesgo, incendio, producido sobre un mismo interés, que en última instancia es el del arrendatario del vehículo. En este sentido, la Sentencia de la Audiencia Provincial de Madrid, Sección 25.ª, n.º 399/2015, de 1 de diciembre, rec. 357/2015, fundamento de derecho quinto, dice: «Partiendo de ello es evidente que el requisito de tomador único -de contratante único-, que como presupuesto del seguro múltiple parece establecerse por el párrafo primero del reseñado artículo 32 de la Ley de Contrato de Seguro, carece de todo sentido, ya que resulta perfectamente posible -como ya señalaron las sentencias de 20 de octubre de 2004 y 30 de septiembre de 2003 de la Sección Decimocuarta de esta Audiencia Provincial y reiteraron las de esta misma Sección de 7 de diciembre de 2005, 8 de mayo de 2007 y 5 de octubre de 2012- la existencia de un seguro múltiple concertado por varios tomadores, cuando exista una pluralidad de intereses subjetivos objeto de un mismo aseguramiento, pues carece de sentido que la finalidad perseguida con el artículo 32 se pierda solo por tal circunstancia, ya que lo relevante es la realidad del sobreseguro -esto es, que el capital asegurado resulte superior al valor real del bien asegurado- y no la figura del contratante, pues de otro modo la ignorancia de los aseguradores de tal circunstancia puede favorecer el pago de cantidades superiores al importe del daño.

Por ello, debe aceptarse, incluso, que en determinados supuestos, aun cuando exista dualidad de tomadores, si el asegurado-perjudicado es el mismo y concurre el resto de las notas que definen el seguro múltiple, con el fin de respetar el principio indemnizatorio en sus dos vertientes, se sostenga la existencia de seguro múltiple y se apliquen sus consecuencias (distribución de la cuota de responsabilidad sobre las compañías aseguradoras en lo que aquí interesa).»

SEGUNDO.– Resultan también de aplicación los artículos 45 a 49 de la Ley de Contrato de Seguro, en cuanto que regulan la contingencia que da lugar al ejercicio de la acción de repetición que mediante esta demanda se efectúa.

TERCERO.– El art. 1145 del Código Civil, de aplicación supletoria, establece que: «El pago hecho por uno de los deudores solidarios extingue la obligación.

El que hizo el pago sólo puede reclamar de sus codeudores la parte que a cada uno corresponda, con los intereses del anticipo.

La falta de cumplimiento de la obligación por insolvencia del deudor solidario será suplida por sus codeudores, a prorrata de la deuda de cada uno.»

CUARTO.– Los arts. 1101, 1108 y 1109 del Código Civil dan las pautas para el cálculo de los intereses devengados.

COSTAS

En aplicación del art. 394.1 de la LEC deberán imponerse a la demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos que acompaño y copia de todo ello, acuerde el Letrado de la Administración de Justicia admitir a trámite la presente demanda, dar traslado de la misma a la demandada y citar a las partes a la audiencia previa a fin de que, en su día y seguido el juicio por todos sus trámites legales, se dicte sentencia por la que se condene a [DENOMINACIÓN SOCIAL DE LA ASEGURADORA DEMANDADA], S.A. Compañía de Seguros y Reaseguros (demandada), a abonar a mi representada la cantidad de [IMPORTE] euros, más los intereses legales correspondientes desde [FECHA], todo ello con expresa imposición de costas a la demandada.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del abogado/a: [NOMBRE Y APELLIDOS] Firma del procurador/a: [NOMBRE Y APELLIDOS]
