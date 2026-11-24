---
name: demanda-juicio-cambiario-contra-aceptante-letra-firmo-civ-1154
description: "Demanda de juicio cambiario contra el aceptante de una letra que firmó además un pagaré impagado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio cambiario contra el aceptante de una letra que firmó además un pagaré impagado

> Formulario **CIV-1154** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio cambiario sobre acción directa contra la mercantil aceptante de una letra de cambio, que, a su vez, es firmante de un pagaré impagado, contra la que se ejercita también acción directa acumulada.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio cambiario contra el aceptante de una letra que firmó además un pagaré impagado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio cambiario contra el aceptante de una letra que firmó además un pagaré impagado” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:demanda-juicio-cambiario-contra-aceptante-letra-firmo-civ-1154`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (13 veces)
- [ ] IMPORTE EN CIFRA (13 veces)
- [ ] Nº DE DOCUMENTO (7 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] ENTIDAD BANCARIA (4 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] DÍA
- [ ] LUGAR
- [ ] MES Y AÑO
- [ ] PARTE DEMANDADA
- [ ] SEDE

## Normas que cita el formulario

- art. 820 Ley 1/2000
- art. 51.1 LEC
- art. 819 LEC
- art. 71.2 LEC
- art. 73.1.2 LEC
- art. 822 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales, que actúa en nombre y representación de [NOMBRE DEL REPRESENTADO/A], representación y circunstancias de la sociedad representada que constan en la copia de escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que en la representación que ostento, vengo a interponer demanda de Juicio Cambiario contra la entidad [DENOMINACIÓN SOCIAL], con domicilio social en [LOCALIDAD], y cuyo establecimiento abierto al público en que han surgido las relaciones derivadas de los negocios de emisión de títulos de crédito, se haya sito en [LOCALIDAD], en reclamación de [IMPORTE] euros ([IMPORTE EN CIFRA] €) en concepto de principal, más lo que deba adicionarse en concepto de intereses y costas, conforme se concretará.

Dicha demanda se basa en los siguientes:

HECHOS

PRIMERO.- Mi mandante es tenedora legítima de una letra de cambio, que en fecha [FECHA] procedió a librar por importe de [IMPORTE] euros ([IMPORTE EN CIFRA] €) y debidamente aceptada por la mercantil demandada [DENOMINACIÓN SOCIAL], con vencimiento al [FECHA]; figurando en la misma como domicilio de pago el de la cuenta de la librada sita en el Banco [ENTIDAD BANCARIA] de esta localidad. Ello se acredita con la dicha letra de cambio (DOCUMENTO Nº [Nº DE DOCUMENTO]).

SEGUNDO.- Mi mandante había extendido la letra mencionada a la orden de la Caja de Ahorros [ENTIDAD BANCARIA], que al vencimiento la presentó para su pago en el establecimiento de la demandada, quien no la abonó, por lo que fue entregada al Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], para su protesto por falta de pago, el cual se realizó en término legal y sin que mediara ninguna manifestación en contra. Se adjunta para demostración el acta notarial levantada al efecto (DOCUMENTO Nº [Nº DE DOCUMENTO]).

TERCERO.- Lo anterior ocasionó además unos gastos bancarios que ascienden a la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), que deben adicionarse a los del protesto notarial de [IMPORTE] euros ([IMPORTE EN CIFRA] €), y en fin, al nominal de la letra de cambio impagada, lo que arroja un total que se reclama como principal por la letra de cambio impagada de [IMPORTE] euros ([IMPORTE EN CIFRA] €). Así se acredita con la carta de adeudo en cuenta, que es el DOCUMENTO Nº [Nº DE DOCUMENTO], figurando los honorarios por el protesto en factura cosida al mismo acta.

CUARTO.- Independientemente de lo anterior, la mercantil demandada [DENOMINACIÓN SOCIAL], también hizo entrega a mi patrocinada de un pagaré contra su cuenta corriente del Banco [ENTIDAD BANCARIA] de esta localidad, por importe de [IMPORTE] euros ([IMPORTE EN CIFRA] €) y fecha de vencimiento de [DÍA] de [MES Y AÑO], a la orden de mi mandante [NOMBRE DEL REPRESENTADO/A], siendo pagadero en la entidad que figura en el mismo, Caja de Ahorros [ENTIDAD BANCARIA], la cual lo presentó al cobro en su fecha, y se le denegó su pago tal y como consta en la diligencia que aparece extendida en el reverso del referido pagaré, debidamente fechada y firmada, dentro del término hábil. Así resulta del mentado pagaré inatendido que se aporta anexo con la indicada diligencia (DOCUMENTO Nº [Nº DE DOCUMENTO]).

QUINTO.- La falta de pago del pagaré ocasionó gastos bancarios, por el servicio de cobranza y comunicación por correo, que ascienden a la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), que deben sumarse al nominal del pagaré, lo que arroja un total que se reclama como principal por el pagaré inatendido de [IMPORTE] euros ([IMPORTE EN CIFRA] €). Así demuestra carta de adeudo en cuenta, que es el DOCUMENTO Nº [Nº DE DOCUMENTO].

El total reclamado en este proceso como principal es de [IMPORTE] euros ([IMPORTE EN CIFRA] €), más un 30% calculado para los intereses moratorios legales vencidos y por vencer y las costas procesales.

SEXTO.- Habiendo resultado estéril el intento de solución amistosa para resarcirse del importe de sus créditos documentados, se fuerza la presente demanda. Se acompañan copias del burofax remitido y recibido como DOCUMENTO Nº [Nº DE DOCUMENTO].

Con los anteriores hechos guardan relación aplicativa los siguientes:

FUNDAMENTOS DE DERECHO

I. Ejercitándose en esta demanda las acciones dimanantes de una letra de cambio y de un pagaré, se interpone ante el Tribunal de Instancia que ha de conocer de ella, conforme a las regla sobre competencia territorial imperativa establecida en el art. 820 de la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil (LEC), en relación con el art. 51.1 LEC y 85.1º LOPJ, dado que en localidad del partido de los Tribunales a que me dirijo está sito el establecimiento abierto al público de la sociedad demandada en que nacieron las relaciones jurídicas constituídas por los negocios de libramiento de la letra y del pagaré.

II. La acción cambiaria puede ejercitarse, tanto en la vía ordinaria, como a través del proceso especial cambiario, conforme al art. 49.pfo.2º Ley 19/85 de 16 de julio, Cambiaria y del Cheque (LCCH), reformado por Disposición Final 10ª.2 LEC, a lo que se remite el art. 96 LCCH, a propósito de la acción dimanante del pagaré.

III. El proceso especial cambiario de los arts. 819-27 LEC es un juicio especial documental en que la legitimación se acredita preliminarmente mediante aportación de un título formal (art. 821.1 y 2.pfo.1º LEC), que en el caso, son una letra de cambio, cuya corrección dimana de la concurrencia en las mismas de todas y cada una de las menciones que exigen los arts. 1 a 13 LCCH, y un pagaré, cuya corrección deriva del cumplimiento de las exigencias de los arts. 94 y 95 LCCH.

Aparece en ambos documentos la firma del representante legal de aquel contra quien se dirige el proceso (aceptante de la letra, art. 33 LCCH, y firmante del pagaré, art. 97 LCCH), que no ha sido tachada de inauténtica.

IV.- Arts. 23 y 31 LEC, según los cuales no se excepciona para el juicio cambiario que la comparecencia en juicio se efectúe por medio de Procurador, y bajo dirección y firma de Letrado.

V. La acción cambiaria puede ser directa contra el aceptante y sus avalistas o de regreso contra cualquier otro obligado, y el tenedor podrá reclamar a la persona contra la quien ejercite la acción directa —como es caso, contra aceptante—, sin necesidad de protesto —aunque en el caso lo ha habido—, el importe de la letra de cambio no pagada, los réditos de la cantidad anterior devengados desde la fecha de vencimiento de la letra calculados al tipo de interés legal del dinero incrementado en dos puntos, y los demás gastos, incluidos los del protesto y los de comunicaciones (art. 58 en relación con el art. 49.1 LCCH).

VI. La acción derivada del pagaré puede ser directa contra el firmante, que asume obligación como el aceptante de la letra de cambio (art. 97 LCCH), que tampoco precisa de protesto, aunque en el caso ha operado la declaración equivalente, y así se acredita, declaración cual es la de la entidad bancaria domiciliataria a través de la Cámara de Compensación, en que se acredita el impago (art. 51, en relación con art. 96 LCCH).

Se reclama el importe del pagaré, los réditos de dicha cantidad devengados desde el día del vencimiento, y calculados al tipo del interés legal del dinero aumentado en dos puntos, los gastos del adeudo bancario y la comunicación por correo (art. 58, en relación con art. 96 LCCH).

VII. La letra de cambio tendrá aparejada ejecución a través del juicio cambiario que regula la Ley de Enjuiciamiento Civil en el Capítulo II, Título III, del Libro IV, por la suma determinada en el título y por las demás cantidades indicadas, sin necesidad de reconocimiento judicial de las firmas. El ejercicio de la acción cambiaria, a través del proceso especial cambiario, se someterá al procedimiento establecido en la Ley de Enjuiciamiento Civil, con las particularidades previstas en los artículos anteriores y las que a continuación se expresan (arts. 66 y art. 68 LCCH).

Posibilidad de pretender y proceso adecuado al que se remite el art. 96 LCCH con respecto a la acción dimanante del pagaré impagado.

VIII. Conforme al art. 71.2 LEC, el actor puede acumular en la demanda cuantas acciones le competan contra el demandado, aunque provengan de diferentes títulos, en cuanto que no sean incompatibles, lo que se hace en el presente caso mediante acumulación inicial simple objetiva, que por su materia no han de verse en juicio de diferente tipo (‘a contrario’ del art. 73.1.2º LEC), sino en el proceso especial cambiario, sin ninguna clase de prohibición legal, y resultando las acciones dimanantes de la letra de cambio y del pagaré, conforme al art. 819 LEC ámbito común del mismo cauce, sin posibilidad de alteración de las reglas de jurisdicción y competencia.

IX. Aunque el deudor atienda en el plazo legal del requerimiento al pago, y ponga a disposición de mis mandantes la suma de dinero reclamado, con entrega a aquél de la letra y el pagaré, poniéndose término al proceso, serán de cargo del deudor todas las costas procesales (art. 822 en relación con 583 LEC).

Por lo expuesto,

SUPLICO AL TRIBUNAL,

que teniendo por presentado este escrito de demanda con los documentos que se acompañan, se admitan uno y otros, se sirva tener por admitidas las pretensiones acumuladas contra [PARTE DEMANDADA], en ejercicio de la acción cambiaria directa como deudora aceptante, y en ejercicio de la acción derivada del pagaré como firmante, se mande:

Requerir a la deudora [DENOMINACIÓN SOCIAL] a fin de que pague la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) importe del principal de la letra de cambio y de [IMPORTE] euros ([IMPORTE EN CIFRA] €) importe del principal del pagaré, en ambos casos con sus gastos de protesto, devolución bancaria y comunicaciones que se han cuantificado, más los réditos desde la fecha del vencimiento calculados al tipo de interés legal del dinero incrementado en dos puntos, así como las costas del juicio que, prudencialmente y por ahora, han de fijarse en [IMPORTE] euros ([IMPORTE EN CIFRA] €) y [IMPORTE] euros ([IMPORTE EN CIFRA] €), respectivamente.

Ordenar el inmediato embargo preventivo de bienes de la deudora por la citada suma total, por si no se atendiera el requerimiento de pago en el plazo legal de diez días, y

Para el caso de que no se satisfagan las dichas cantidades, ni tampoco formule oposición la deudora, se despache la ejecución contra sus bienes, hasta el pago de los demandados a mis representados de cuanto se acredita a razón de la letra de cambio y del pagaré, bases de las pretensiones acumuladas.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
