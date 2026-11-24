---
name: solicitud-embargo-preventivo-como-medida-cautelar-civ-1248
description: "Solicitud de embargo preventivo como medida cautelar previa a la demanda principal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de embargo preventivo como medida cautelar previa a la demanda principal

> Formulario **CIV-1248** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito de solicitud de medida cautelar de embargo preventivo de bienes antes de la presentación de la demanda principal, sin audiencia del demandado.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de embargo preventivo como medida cautelar previa a la demanda principal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de embargo preventivo como medida cautelar previa a la demanda principal” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-embargo-preventivo-como-medida-cautelar-civ-1248`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] IMPORTE (9 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] NÚMERO (3 veces)
- [ ] COLEGIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] Nº (2 veces)
- [ ] CALLE
- [ ] IMPORTE EN CIFRA
- [ ] LUGAR
- [ ] MEDIOS DE PRUEBA
- [ ] NOMBRE DE LA REVISTA
- [ ] PLAZO
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 723.1 LEC
- art. 85.1 LOPJ
- art. 249.2 LEC
- art. 50.1 LEC
- art. 730.2 LEC
- art. 733.2 LEC
- art. 32 LEC
- art. 727.1.ª LEC
- art. 721.1 LEC
- art. 726.1.1.ª LEC
- art. 728.1 LEC
- art. 1.911 CC
- art. 728.2 LEC
- art. 728.3 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], dirigido por el Letrado/a D./Dña. [NOMBRE Y APELLIDOS], abogado ejerciente del Ilustre Colegio de [COLEGIO], con despacho abierto en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito vengo a solicitar la medida cautelar de embargo preventivo de los bienes de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], en cuantía suficiente para cubrir la cantidad de [IMPORTE] euros, así como [IMPORTE] euros que se presupuestan para responder de los intereses de la citada cantidad y costas del futuro proceso.

La solicitud se basa en los siguientes:

HECHOS

PRIMERO.- Mi mandante y D./Dña. [NOMBRE Y APELLIDOS] han mantenido durante [PLAZO] una relación comercial en la que D./Dña. [NOMBRE Y APELLIDOS] ha venido suministrando numerosas mercancías a D./Dña. [NOMBRE Y APELLIDOS], que han resultado impagadas, y en total éste adeuda a mi representado la cantidad de [IMPORTE] euros.

Se aporta el contrato que recoge la relación comercial entre las partes (documento n.º [NÚMERO]) y las diferentes facturas derivadas de las entregas realizadas y no pagadas por la parte demandada (documentos números [Nº DE DOCUMENTO]), así como los albaranes del transportista firmados por el destinatario, es decir por D./Dña. [NOMBRE Y APELLIDOS] (documentos números [Nº DE DOCUMENTO]).

SEGUNDO.- Habiendo intentado sin éxito una solución amistosa, al objeto de reclamar dicha cantidad mi mandante envió un requerimiento por conducto notarial al demandado en reclamación de la deuda pendiente cuya copia asimismo se aporta como documento n.º [Nº DE DOCUMENTO]

TERCERO.- No obstante el requerimiento formalmente realizado con fecha [FECHA], no atendido por el demandado, antes de reclamar judicialmente, mi mandante propuso -incluso- un acuerdo de aplazamiento de pago no aceptado por el demandado, como es muestra la carta dirigida por el actor y la contestación de D./Dña. [NOMBRE Y APELLIDOS], que se aportan como documentos números

En dicha contestación fue cuando el demandado aseguró a mi mandante que la empresa no iba bien, careciendo en ese momento de liquidez, siendo el único bien el local donde la empresa desarrolla su actividad.

CUARTO.- Siendo intención de esta parte formular demanda destinada a reclamar la deuda, ha venido en conocimiento que el demandado ha cerrado el negocio que regentaba sin dejar encargado ni persona que lo administre, y pretende desprenderse de los bienes que constituyen su patrimonio, con lo cual se sustraerían los mismos a la posible garantía de satisfacción del crédito que se reclamará.

A través de averiguaciones particulares y de manifestaciones recogidas por mi mandante en la portería del inmueble, esta parte ha podido enterarse sobre la puesta en venta de local comercial en que el demandado tenía instalado su empresa, sito en [LOCALIDAD], que es de su propiedad, y cuya titularidad registral se acredita por certificado del Registro de la Propiedad de [LOCALIDAD] (documento n.º [NÚMERO]).

Esto se corrobora con el cartel de "Se vende. Razón tfno [TELÉFONO] " que figura en la puerta del establecimiento, incorporándose tres fotografías del estado en que se encuentra el local en la actualidad acompañadas como documentos números

Asimismo figura un anuncio inequívoco en la revista inmobiaria " [NOMBRE DE LA REVISTA] ", que aportamos con el presente escrito, en el que se dan los datos de ubicación del local en venta (documento n.º [NÚMERO]).

Hacemos constar que esta parte no conoce otros bienes con los que el demandado pueda hacer frente a la condena dineraria que se solicitará en el pleito principal.

QUINTO.- En el espacio de tiempo hasta que pueda tenerse por perfilada adecuadamente la demanda, y seguido el respectivo juicio ordinario, en tanto que se ejercitará acción de reclamación de cantidad superior a 15.000 euros, se dicte sentencia, existe la dificultad de fructuosidad real de ésta, que se desea atajar con la adopción de una medida cautelar de embargo preventivo de los bienes del deudor hasta alcanzar la cantidad de [IMPORTE] euros reclamados.

SEXTO.- Las circunstancias descritas son, a juicio de esta parte, suficientemente reveladoras de la necesidad y urgencia de solicitar la medida con carácter previo a la interposición de la demanda y que se proceda a acordar la misma sin audiencia previa del demandado, para asegurar la efectividad de la sentencia que pudiera recaer, ofreciendo, prestar caución en la cuantía y forma que más adelante se dirá, sin perjuicio de atender a lo que, en tal sentido, se fije por el órgano jurisdiccional a que me dirijo.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Con arreglo al art. 723.1 LEC, competente objetivamente el Tribunal de Instancia, conforme a los arts. 85.1º LOPJ y 45 LEC, lo es territorialmente el que nos dirigimos, puesto que es ante el que habrá de presentarse la demanda de juicio ordinario del art. 249.2 LEC, es decir, el del domicilio del demandado, conforme al art. 50.1 LEC.

II.- PROCEDIMIENTO.

Art. 730 y ss. LEC, y especialmente el art. 730.2 LEC, que regula la posibilidad de solicitarse medidas cautelares antes de la presentación de la demanda, y en cuanto a la tramitación, se solicita que se sustancie sin la previa audiencia del adverso, conforme al art. 733.2 LEC, por concurrir razones de urgencia que comprometen el buen fin de la medida cautelar si se produce tal contradicción simultánea y la demora en resolver, que la convocatoria a vista aceleraría sin remedio, como se ha razonado.

III.- LEGITIMACIÓN.

La activa corresponde a la actora en virtud de lo dispuesto en el art. 721.1 en relación con el 730.2, ambos de la LEC, pues es persona que interpondrá demanda dentro del plazo legal de veinte días, solicitando con anterioridad la medida cautelar por razones de urgencia. La pasiva a la parte demandada por su condición de deudor y futuro demandado.

IV.- POSTULACIÓN.

El actor está representado por el Procurador que suscribe, habilitado para ejercer en el territorio del Tribunal al que nos dirigimos, y asimismo asistido del Letrado del Ilustre Colegio de Abogados de [COLEGIO] (en cuanto a la debida postulación, si la medida cautelar se solicita antes de la demanda, y necesariamente entonces será urgente, no es preceptiva la representación mediante Procurador de los tribunales, ni la dirección letrada —arts. 23.2.3.º y 31.2.2.º—, aunque si se utiliza, debe enterarse al objeto de poner en marcha el dispositivo de igualdad procesal del art. 32 LEC).

V.- MEDIDA SOLICITADA.

Se solicita una medida cautelar de EMBARGO PREVENTIVO del art. 727.1.ª LEC. Se señala como bien de la demandada susceptible de embargo, por analogía al despacharse embargo ejecutivo (arts. 549.1.3.º y 551.3.1.º LEC), un inmueble, cuya reseña se proporcionará en el suplico, que se entiende alcanzar en su valor a cubrir lo reclamado.

Justificación: La afectación de bienes determinados a las resultas de la efectividad de la tutela judicial que pudiera otorgarse en la sentencia estimatoria que se dictare (art. 721.1 LEC), es útil y congruente con lo que se pedirá, que es la condena a la entrega de una cantidad de dinero (art. 727.1.ª LEC),de modo que no pueda verse impedida o dificultada por situaciones producidas durante la pendencia del proceso correspondiente (art. 726.1.1.ª LEC).

Presupuestos: El peligro de demora procesal o "periculum in mora" (art. 728.1 LEC) se justifica en el que deriva de la responsabilidad patrimonial individual del art. 1.911 CCiv, cuando la conducta del demandado, tendente a excluir el patrimonio de respuesta ante las gestiones que se han alegado, entiende esta parte que evidencia la dificultad en que se puede encontrar mi mandante para obtener la efectividad de la tutela que pudiera otorgársele en una futura sentencia estimatoria de la demanda que esta parte interpondrá, existiendo suficientes indicios de que, de no adoptarse inmediatamente la medida solicitada podría quedar vacío de contenido el derecho de mi patrocinado, al transmitir el demandado el local en que estaba instalada la empresa, para sustraerlo de su patrimonio, y así eludir sus compromisos económicos con el actor, en concreto la responsabilidad que en el futuro sobre el inmueble debería recaer, y no tener ninguna fuente de ingresos conocida, sin que en este peligro se haya colocado por su negligencia el demandante, según apuntilla el art. 728.1, párrafo 2.º LEC.

El "fumus boni iuris" o apariencia de buen derecho resulta de la conjunción del contrato de sumnistro y la prolija aportación documental en que aparece inequívocamente la existencia y subsistencia del crédito ostentado por mi patrocinado, frente al silencio del demandado, habiendo recibido burofax de reclamación contractual por conducto de abogado (art. 728.2 LEC), que acreditan preliminarmente ese juicio provisional e indiciario favorable al fundamento de la pretensión principal que se formulará, que es punto medio entre la pura incertidumbre y la certeza plena que sólo se podrá alcanzar formalmente al término del proceso.

Caución: Presupuesto de la ejecución de la medida cautelar (art. 728.3 LEC), se ofrece prestar caución, para responder de los daños y perjuicios que la adopción de la medida pudiera causar, en cuantía justificada de [IMPORTE] euros ([IMPORTE EN CIFRA] €), optándose la fórmula de aval bancario, con las condiciones que fije S.S.ª, que se estima procedente atendiendo a la importancia real de la pretensión que se quiere asegurar, al fundamento del derecho reclamado, y a la efectividad y cuantía de los posibles daños y perjuicios derivados de la ejecución de la medida, puesto que se procura sencillamente una dificultad de venta.

En su virtud,

SUPLICO AL TRIBUNAL

que, teniendo por recibida esta presente solicitud de medida cautelar, se digne admitirla y, sin audiencia previa de la parte contraria, a la mayor brevedad dicte Auto por el que se decrete el embargo preventivo del local en planta baja en el edificio señalado con el númerode la callede esta ciudad, que es la finca registral n.º [Nº], al librode, tomo, del Registro de la Propiedad nº [Nº],en cantidad suficiente para cubrir el importe de [IMPORTE] euros, comprensiva de principal, intereses y costas que por ahora y sin perjuicio de ulterior liquidación se calculan en la cantidad de [IMPORTE] euros, así como [IMPORTE] euros que se presupuestan para responder de los intereses de la citada cantidad y costas del futuro proceso, bajo condición de prestarse la caución por la parte actora en forma de aval bancario indefinido por cuantía deeuros (€ [IMPORTE]), o la que S.S.ª, con su plazo y condiciones, fije.

OTROSÍ DIGO: Que a los efectos de acreditar que procede la medida instada pues concurren los requisitos que la ley exige, se propone como prueba al efecto, además de la documental aportada, la siguiente:

1.º - La testifical de D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], cuya citación se solicita se realice a través del Tribunal.
2.º - [MEDIOS DE PRUEBA]

SUPLICO AL TRIBUNAL se acuerde admisión y práctica de la prueba propuesta.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
