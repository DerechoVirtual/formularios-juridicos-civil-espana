---
name: contrato-subarriendo-finca-rustica-civ-0546
description: "Contrato de subarriendo de finca rústica. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de subarriendo de finca rústica

> Formulario **CIV-0546** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de subarriendo de finca rústica» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de subarriendo de finca rústica” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-subarriendo-finca-rustica-civ-0546`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (8 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] NÚMERO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE PARCELA (2 veces)
- [ ] Nº DE POLÍGONO (2 veces)
- [ ] PARAJE O MUNICIPIO (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] FECHAS
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MEDIO DE PAGO
- [ ] MES
- [ ] SUCURSAL

## Normas que cita el formulario

- art. 12 Ley 49/2003
- art. 1.851 Código Civil
- art. 1561 Código Civil

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

[ELEGIR UNA OPCIÓN: Intervienen / En representación / Nombre propio]

Exponen

PRIMERO.- Que EL SUBARRENDADOR es arrendatario, de las fincas que a continuación se relacionan:

-"" (Polígono [Nº DE POLÍGONO], parcela [Nº DE PARCELA], en [PARAJE O MUNICIPIO]), con una superficie aproximada de [Nº] hectáreas

-"" (Polígono [Nº DE POLÍGONO], parcela [Nº DE PARCELA], en [PARAJE O MUNICIPIO]), con una superficie aproximada de [Nº] hectáreas

Se adjunta copia de dicho contrato como anexo I.

SEGUNDO.- Que el destino principal de ambas fincas es la siembra de productos cereales, estando libre de cargas, arrendamientos, gravámenes y al corriente en el pago de impuestos, según declara EL SUBARRENDADOR.

TERCERO.- Que EL SUBARRENDATARIO está interesado en que se le arrienden las fincas anteriormente mencionadas, por lo que las Partes, libremente y de común acuerdo, conciertan el presente CONTRATO DE SUBARRIENDO RÚSTICO con arreglo a las siguientes,

ESTIPULACIONES

Objeto del contrato

EL SUBARRENDADOR cede en subarriendo al SUBARRENDATARIO la finca descrita en el Exponendo Primero del presente documento.

[ELEGIR UNA OPCIÓN: Aprovechamientos / Cultivo predeterminado / Cultivo libre]

Reserva de aprovechamientos

Quedan excluidos del subarriendo los siguientes aprovechamientos, principales y compatibles con los que puede realizar el SUBARRENDATARIO:

Estos aprovechamientos podrán ser objeto de cesión a personas distintas del SUBARRENDATARIO, quedando éste obligado a permitir a dichas personas la realización de las faenas agrícolas correspondientes.

Duración del contrato

El presente arrendamiento se conviene y concierta por plazo mínimo de cinco años, en conformidad con el artículo 12 de la Ley 49/2003, de 26 de noviembre, de Arrendamientos Rústicos.

Llegado el término del plazo contractual EL SUBARRENDADOR podrá recuperar la finca, previa notificación fehaciente al SUBARRENDATARIO con un año de antelación.

Prórrogas

Si EL SUBARRENDADOR no recobrara la finca conforme a lo establecido en la cláusula anterior de este contrato porque EL SUBARRENDATARIO no ha puesto la posesión de la finca arrendada a disposición del SUBARRENDADOR al término del plazo inicial estipulado, el contrato se entenderá tácitamente prorrogado por un período de cinco años. Tales prórrogas se sucederán indefinidamente en tanto no se produzca la denuncia del contrato.

EL SUBARRENDATARIO por su parte podrá dar por extinguido el contrato al término de cada año agrícola, notificándoselo al SUBARRENDADOR con un año de antelación.

El subarriendo se extinguirá en todo caso cuando se extinga el arrendamiento del que trae causa.

[ELEGIR UNA OPCIÓN: Importe de la renta / En dinero / En especie]

Pago de la renta

El pago se efectuará entre los días [FECHAS] y [DÍA] de cada mes de septiembre en la cuenta corriente núm. [Nº] que EL SUBARRENDADOR tiene suscrita con la entidad [DENOMINACIÓN SOCIAL] en su sucursal [SUCURSAL].

Retraso en el pago

El retraso en más de [Nº] días en cualquiera de los pagos dará derecho al SUBARRENDADOR a exigir al SUBARRENDATARIO un interés moratorio del % respecto de cada uno de los pagos no satisfechos puntualmente.

Actualización de la renta

Transcurrido el primer año de vigencia del presente contrato, la renta pactada será actualizada anualmente en función de la evolución anual experimentada por el Índice General de Precios al Consumo del Instituto Nacional de Estadística.

La renta actualizada será exigible al SUBARRENDATARIO a partir del mes siguiente a aquél en que EL SUBARRENDADOR se lo notifique por escrito, expresando el porcentaje de alteración aplicado. Se considerará válida la notificación hecha mediante anotación en el recibo de la anualidad precedente.

Avalista

D. [NOMBRE Y APELLIDOS], provisto de D.N.I. número [NÚMERO] y presente en este acto, se constituye en fiador o avalista de las obligaciones contraídas por EL SUBARRENDATARIO con EL SUBARRENDADOR, obligándose solidariamente con EL SUBARRENDATARIO al cumplimiento de las obligaciones arrendaticias y especialmente al pago de la renta, así como a cualquier cantidad económica que se derive del presente contrato o por disposición legal, y a la conservación del buen estado de la finca por toda la duración del contrato, con renuncia expresa a los beneficios de excusión, división.

A tal efecto, acepta de antemano cualquier prórroga o renovación que EL SUBARRENDADOR pudiera conceder, sea cual sea la forma en que se instrumente la misma, sin que, en consecuencia, la concesión de la indicada prórroga o renovación pueda producir los efectos establecidos en el artículo 1.851 del Código Civil.

Reparaciones y mejoras

Obras necesarias

Corresponde al SUBARRENDATARIO efectuar las reparaciones, mejoras e inversiones que sean propias del empresario agrario en el desempeño normal de su actividad y las que le vengan impuestas por disposición legal o por Resolución judicial o administrativa firmes, o por Acuerdo firme de la comunidad de regantes relativo a la mejora del regadío que sea también propia del empresario agrario en el desempeño normal de su actividad, sin que por ello tenga derecho a disminución de la renta, ni a la prórroga del arriendo, salvo que por acuerdo de las partes o de las propias disposiciones legales o resoluciones judiciales o administrativas, resultase otra cosa.

Finalizado el contrato de arrendamiento, EL SUBARRENDATARIO tendrá derecho a pedir una indemnización al SUBARRENDADOR por el aumento del valor de la finca arrendada por las mejoras realizadas, siempre que éstas se hayan efectuado con el consentimiento del SUBARRENDADOR.

Las mejoras hechas durante el arrendamiento se presume que han sido efectuadas a cargo del SUBARRENDATARIO.

Mejoras útiles

Por lo que se refiere a las mejoras útiles y voluntarias, de cualquier naturaleza que sean, realizadas por EL SUBARRENDATARIO en las fincas arrendadas, se estará al régimen establecido por el Código Civil para el poseedor de buena fe.

EL SUBARRENDATARIO podrá realizar obras de accesibilidad en el interior de los edificios de la finca que le sirvan de vivienda, siempre que no provoquen una disminución de la estabilidad o seguridad del edificio y sean necesarias para que puedan ser utilizados de forma adecuada y acorde con la discapacidad o la edad superior a 70 años, tanto del SUBARRENDATARIO como de su cónyuge, de la persona que conviva con EL SUBARRENDATARIO de forma permanente en análoga relación de afectividad con independencia de su orientación sexual, de sus familiares hasta el cuarto grado de consaguinidad que conviva con alguno de ellos de forma permanente y de aquellas personas que trabajen, o presten servicios altruistas o voluntarios para cualquiera de las anteriores en la vivienda enclavada en la finca rústica. Al término del contrato, EL SUBARRENDATARIO estará obligado a reponer la vivienda a su estado anterior, si así se lo exigiera el SUBARRENDADOR

Modificación de la apariencia externa

EL SUBARRENDATARIO no puede, salvo acuerdo expreso entre las partes, hacer desaparecer las paredes, vallas, setos vivos o muertos, zanjas y otras formas de cerramiento o cercado del predio arrendado, si separan dos o más fincas integradas en una misma unidad de explotación, salvo en los tramos necesarios para permitir el paso adecuado de tractores, maquinaria agrícola y cuando las labores de cultivo lo requieran, sin perjuicio de lo que establezca la legislación sobre protección del medio ambiente y protección del patrimonio histórico y de la obligación de devolver las cosas al término del arriendo tal como las recibió, de conformidad con lo dispuesto en el artículo 1561 del Código Civil.

Prohibición de subarriendo

EL SUBARRENDATARIO no podrá ceder o subarrendar la finca o explotación sin el consentimiento expreso del SUBARRENDADOR. Dicho consentimiento no será necesario cuando la cesión o subarriendo se efectúe a favor del cónyuge o de uno de los descendientes del SUBARRENDATARIO. No obstante, el subrogante y el subrogado notificarán fehacientemente al SUBARRENDADOR la cesión o el subarriendo, en el plazo de [Nº] días hábiles a partir de su celebración.

Autorización de subarriendo o traspaso

EL SUBARRENDATARIO podrá subarrendar la finca o ceder el contrato de arrendamiento sin necesidad de contar con el consentimiento del SUBARRENDADOR, teniendo ésta derecho a una elevación de la renta del % en el supuesto de producirse el subarriendo parcial y del % en el supuesto de producirse la cesión del contrato.

Tanto la cesión como el subarriendo deberá notificarse de forma fehaciente al SUBARRENDADOR en el plazo de un mes desde que aquéllos se hubieran concertado. EL SUBARRENDADOR tendrá derecho a resolver el contrato si no se realizase esta notificación o si las condiciones pactadas contravinieran lo dispuesto en este contrato.

Derecho de tanteo y retracto

En toda transmisión ínter vivos de la finca arrendada, incluida la donación, aportación a sociedad, permuta, adjudicación en pago o cualquiera otra distinta de la compraventa, de su nuda propiedad, de porción determinada o de una participación indivisa de aquélla, EL SUBARRENDATARIO tendrá derecho de tanteo y retracto.

Al efecto, EL SUBARRENDADOR notificará de forma fehaciente al SUBARRENDATARIO su propósito de enajenar y le indicará los elementos esenciales del contrato y, a falta de precio, una estimación del que se considere justo.

EL SUBARRENDATARIO tendrá un plazo de [Nº] días hábiles desde que hubiera recibido la notificación para ejercitar su derecho de adquirir la finca en el mismo precio y condiciones, y lo notificará al enajenante de modo fehaciente. A falta de notificación del SUBARRENDADOR, el SUBARRENDATARIO tendrá derecho de retracto durante [Nº] días hábiles a partir de la fecha en que, por cualquier medio, haya tenido conocimiento de la transmisión.

Si el contrato no tuviera precio y EL SUBARRENDATARIO no estuviera conforme con la estimación hecha por EL SUBARRENDADOR, se determinará por un perito independiente nombrado de común acuerdo por las partes, y, en defecto de acuerdo entre ellas, por la jurisdicción civil conforme a las normas de valoración que establece la legislación de expropiación forzosa.

En todo caso, la escritura de enajenación se notificará de forma fehaciente al SUBARRENDATARIO, al efecto de que pueda ejercitar el derecho de retracto o, en su caso, el de adquisición, si las condiciones de la enajenación, el precio o la persona del adquirente no correspondieran de un modo exacto a las contenidas en la notificación previa. El mismo derecho tendrá si no se hubiese cumplido en forma el requisito de la notificación previa. En este caso, el retracto o el derecho de adquisición preferente podrán ser ejercitados durante el plazo de 60 días hábiles a partir de la notificación.

[ELEGIR UNA OPCIÓN: Seguro / Gastos repercutidos al arrendador / No repercutidos]

Incumplimiento contractual

En caso de incumplimiento, EL SUBARRENDADOR podrá instar el desahucio por falta de pago y serán de cargo del SUBARRENDATARIO todos los gastos y costas judiciales y extrajudiciales que origine su incumplimiento, incluso honorarios de Letrado y Procurador aunque la intervención de éstos no fuere preceptiva.

Opción de compra

EL SUBARRENDADOR concede gratuitamente al SUBARRENDATARIO durante la vigencia de este contrato un derecho de opción de compra de la finca arrendada por un precio de [IMPORTE] euros ( €), del cual se deducirán las cantidades abonadas en concepto de renta por EL SUBARRENDATARIO hasta el momento en que haga uso de la opción de compra.

Dicho precio se abonará en [MEDIO DE PAGO] en el momento de hacer uso de la opción y la finca se transmitirá libre de cargas y gravámenes y al corriente en el pago de impuestos.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de la parte

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

Jurisdicción competente y ley aplicable

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, la competencia de los Tribunales que deban conocer del asunto se determinará de conformidad con los criterios de competencia objetiva, funcional y territorial legalmente aplicables.

El presente contrato tiene exclusivamente carácter civil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código Civil y, demás leyes especiales.

[ELEGIR UNA OPCIÓN: Sumisión a tribunales / Sin cláusula penal / Con cláusula penal / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Con cláusula penal]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE SUBARRIENDO RÚSTICO, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(El SUBARRENDADOR)

Fdo. Don [NOMBRE Y APELLIDOS]

(El SUBARRENDATARIO)

========================================================================
