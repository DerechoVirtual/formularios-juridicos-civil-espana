---
name: solicitud-asociacion-consumidores-medida-cautelar-cese-civ-1207
description: "Solicitud de asociación de consumidores de medida cautelar de cese de conducta previa a la demanda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de asociación de consumidores de medida cautelar de cese de conducta previa a la demanda

> Formulario **CIV-1207** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Solicitud por una Asociación de Consumidores y Usuarios de medida cautelar previa a la demanda de juicio verbal en la que se pedirá la declaración de nulidad de la cláusula de los contratos-tipo relativa a la comisión de mantenimiento, la devolución de comisiones cobradas ilícitamente y la indemnización de daños y perjuicios.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de asociación de consumidores de medida cautelar de cese de conducta previa a la demanda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de asociación de consumidores de medida cautelar de cese de conducta previa a la demanda” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-asociacion-consumidores-medida-cautelar-cese-civ-1207`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] NOMBRE DE LA PARTE (4 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] LUGAR (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] CALLE
- [ ] DOMICILIO
- [ ] IMPORTE
- [ ] NÚMERO
- [ ] SEDE
- [ ] TEXTO DE LA CLÁUSULA

## Normas que cita el formulario

- art. 723.1 LEC
- art. 85.1 LOPJ
- art. 250.1.12.º LEC
- art. 52.1.14.º LEC
- art. 52.1.16.º LEC
- art. 730.2 LEC
- art. 727.7.ª LEC
- art. 721.1 LEC
- art. 726.1.1.ª LEC
- art. 728.1 LEC
- art. 728.2 LEC
- art. 5 Ley 10/2014
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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de la Asociación [NOMBRE DE LA PARTE] de Consumidores y Usuarios (ACU), domiciliada en [DOMICILIO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], dirigida por la Letrada D./Dña. [NOMBRE Y APELLIDOS], abogado ejerciente del Iltre. Colegio de [LOCALIDAD], con despacho abierto en [LOCALIDAD], calle [CALLE]; ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito vengo a instar DILIGENCIAS CAUTELARES PREVIAS con base a los siguientes:

HECHOS

PRIMERO

Mi mandante es Asociación de Consumidores y Usuarios legalmente constituida e inscrita en el Registro Oficial, como se demuestra con la copia de los estatutos y cajetín registral, que se acompaña con documento n.º [NÚMERO].

SEGUNDO

Los contratos-tipo de "cuenta de ahorro a la vista" que presenta a la firma a los usuarios del servicio de la entidad Caja de Ahorros Provincial [NOMBRE DE LA PARTE] contienen una cláusula —segunda— a fin de que la entidad depositaria pudiera efectuar cargos en concepto de "comisión de mantenimiento", del siguiente tenor literal:

" [TEXTO DE LA CLÁUSULA] "

Se adjunta relación de contratos-tipo, como documentos nos. a [Nº DE DOCUMENTO].

TERCERO

En el ámbito de actuación funcional y personal de la Asociación que patrocino, son numerosas las quejas de particulares a propósito de la importante e injustificada subida de las comisiones de mantenimiento de cuentas de ahorro a la vista, de la que no han tenido conocimiento personalizado, ni mediante publicación en las oficinas de la entidad de crédito.

CUARTO

Es intención de esta parte formular demanda en la que se pedirá la declaración de nulidad de la indicada cláusula por contravenir el art. 81 del Texto Refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias, aprobado por Real Decreto Legislativo 1/2007, de 16 de noviembre, así como la devolución de comisiones cobradas ilícitamente y la indemnización de daños y perjuicios. En el espacio de tiempo hasta que pueda tenerse por perfilada adecuadamente la demanda, atenida a la Ley 1/2000 (LEC), y seguido el respectivo juicio verbal, en tanto que se ejercitará acción de cesación, se dicte sentencia, existe la dificultad de fructuosidad real de ésta, que se desea atajar con la adopción de una medida cautelar de abstención temporal por la Caja Provincial de Ahorros ZZ de cobrar el incremento de comisiones.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA

Con arreglo al art. 723.1 LEC, competente objetivamente el Juez de Primera Instancia, conforme a los arts. 85.1 LOPJ y 45 LEC, lo es territorialmente el que nos dirigimos, puesto que es ante el que habrá de presentarse la demanda de juicio verbal del art. 250.1.12.º LEC, es decir, el del domicilio del demandado, conforme al art. 52.1.14.º, segundo inciso LEC, que coincide con el fuero territorial de toda acción de cesación en defensa de los intereses tanto colectivos como difusos de los consumidores y usuarios del art. 52.1.16.º LEC.

II.- PROCEDIMIENTO

Art. 730 y ss. LEC, y especialmente el art. 730.2 LEC, que regula la posibilidad de solicitarse antes de la presentación de la demanda, y la tramitación, art. 733.1 que establece la regla general de que se proveerá la solicitud previa audiencia del demandado, y art. 734, que contempla la vista a la que se convocará a las partes por el Letrado de la Administración de Justicia para que sea dable contradecir entre partes antes de disponer.

III.- MEDIDA SOLICITADA

Justificación: Se solicita la medida prevenida en el art. 727.7.ª LEC de abstención temporal de llevar a cabo una conducta, que supone una prestación de ‘facere’ con relación a una actividad ilícita, cual es la de exigencia injustificada de las comisiones por mantenimiento de cuentas de ahorro a la vista conforme a la condición general señalada, para asegurar la efectividad de la pretensión que se ejercitará en la demanda y que consistirá en la acción de cesación dirigida a que se condene a la demandada a eliminar de sus condiciones generales la cláusula que contiene aquélla y se reputa nula y a abstenerse de utilizarla en lo sucesivo.

Es útil y congruente con lo que se pedirá, que es la cesación contra la utilización de condiciones generales de la contratación que son nulas, al objeto de asegurar la efectividad de la tutela judicial que pudiera otorgarse en la sentencia estimatoria que se dictare (art. 721.1 LEC), de modo que no pueda verse impedida o dificultada por situaciones producidas durante la pendencia del proceso correspondiente (art. 726.1.1.ª LEC).

Presupuestos: El peligro de retardo o ‘periculum in mora’ (art. 728.1 LEC), y la apariencia de buen derecho o ‘fumus boni iuris’ (art. 728.2 LEC), derivan de la simple exposición del argumento de invalidez de la cláusula contractual:

En desarrollo del art. 5 Ley 10/2014, de 26 de junio, de ordenación, supervisión y solvencia de entidades de crédito, fue dictada la Orden EHA/2899/2011, de 28 de octubre, de transparencia y protección del cliente de servicios bancarios cuyo art. 3 liberalizaba las comisiones por operaciones o servicios prestados por las entidades de crédito, no obstante tener que establecer y hacer públicas dichas entidades, previo registro en el Banco de España, unas tarifas de comisiones y gastos repercutibles con indicación de los supuestos y, en su caso, periodicidad, con que serán aplicables, no pudiendo cargar tipos o cantidades superiores a los contenidos en las mismas o conceptos no mencionados en ellas. Asimismo en su Disposición Final 3ª se facultó al Banco de España para dictar las normas precisas para el desarrollo y ejecución, que se tradujeron en la Circular 5/2012, de 27 de junio, del Banco de España, a entidades de crédito y proveedores de servicios de pago, sobre transparencia de los servicios bancarios y responsabilidad en la concesión de préstamos.

Pues bien, la Caja Provincial de Ahorros [NOMBRE DE LA PARTE] ni ha confeccionado las tarifas, ni ha remitido al Banco de España el folleto informativo que exige la norma tercera de la Circular, ni se han comunicado a los clientes (norma sexta) las normas de valoración de servicios y liquidación de las comisiones —según es forzoso para contratos de duración indefinida—, habiéndose variado sin previo aviso en tiempo prudencial.

Caución: En esta índole de pretensiones de cesación en defensa de los intereses colectivos y difusos de los consumidores y usuarios, puede el tribunal ex art. 728.3 "in fine" LEC dispensar al demandante de medida cautelar del deber de prestar caución, atendiendo a la entidad económica y repercusión social de los intereses afectados, así como a las circunstancias del caso. Debe tenerse presente que, sobre ser difícil la real y exacta cuantificación del supuesto perjuicio para la Caja de Ahorros demandada derivado de eliminar temporalmente la condición de contratación frente a la que se postula, la misma afecta a la práctica totalidad de los clientes de dicha entidad de crédito, y en cuanto a ésta, la posposición del cobro hasta la resolución definitiva del pleito principal no significaría una crisis económica verdaderamente apreciable, según los números de su balance, por lo que la entidad económica de una suspensión cautelar es relevante, pero sin repercusión negativa en la viabilidad de la empresa predisponente, y amplia la repercusión social.

En todo caso, si no hay dispensa, se especifica que se opta por el tipo de aval de compañía de seguros, para responder de los daños y perjuicios que la adopción de la medida cautelar pudiera causar al patrimonio de la Caja de Ahorros demandada, que en principio se justifica en importe de [IMPORTE] euros, sin perjuicio de lo que fije S. Sª. Iltma. oídas las partes, en atención al cálculo que se aporta en documento adjunto elaborado por experto contable.

En su virtud,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, se sirva admitirlo y tenerme por comparecido y parte en la representación que ostento para que, previos los trámites legales oportunos, se sirva adoptar como diligencias cautelares de juicio verbal, con dispensa de la prestación de caución, o para el caso de exigirse, previa la fijación de la caución pertinente, cuya cuantía y condiciones se tiene ofrecida, de:

La abstención temporal de que hasta que recaiga sentencia definitiva en el juicio verbal que se anuncia, la Caja de Ahorros Provincialcontinúe cobrando el incremento de comisiones de mantenimiento de contratos de cuenta de ahorro a la vista conforme a la condición general de la cláusula segunda de tales contratos.

Todo ello con imposición de las costas del proceso cautelar a la parte contraria, si se resistiere a la adopción de las medidas.

Es de Justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO que interesa al derecho de esta parte valerse para la vista de los siguientes medios de prueba:

DOCUMENTAL, consistente en la unión definitiva a los autos de los trece documentos aportados con este escrito.

INTERROGATORIO del representante legal de la Caja Provincial de Ahorros [NOMBRE DE LA PARTE], que deberá ser citado con los apercibimientos legales de poder ser tenido por confeso de hechos en que hubiese intervenido personalmente, y cuya fijación como ciertos le sea enteramente perjudicial.

TESTIFICAL de los siguiente tres individuos, que se manifiesta acudirán voluntariamente a la citación judicial de esta parte:

D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], y D./Dña. [NOMBRE Y APELLIDOS]

SUPLICO AL TRIBUNAL

Que, teniendo por causada la anterior manifestación al efecto oportuno, se digne proveer conforme a lo solicitado, como es Justicia que reitero en lugar y fecha que ya consta.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
