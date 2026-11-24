---
name: demanda-juicio-cambiario-accion-directa-contra-unico-civ-1153
description: "Demanda de juicio cambiario por acción directa contra el único aceptante de una letra a plazo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio cambiario por acción directa contra el único aceptante de una letra a plazo

> Formulario **CIV-1153** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio cambiario sobre acción directa contra un único librado aceptante, basada en letra de cambio, con plazo expreso de vencimiento (noventa días vista) y declaración equivalente a protesto notarial en el reverso.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio cambiario por acción directa contra el único aceptante de una letra a plazo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio cambiario por acción directa contra el único aceptante de una letra a plazo” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:demanda-juicio-cambiario-accion-directa-contra-unico-civ-1153`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] IMPORTE EN CIFRA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] DÍA
- [ ] FECHA
- [ ] LUGAR
- [ ] MES Y AÑO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NÚMERO

## Normas que cita el formulario

- art. 85.1 LOPJ
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

AL TRIBUNAL

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de [NOMBRE DEL REPRESENTADO/A], con domicilio en [LOCALIDAD], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO]; ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que en la representación que ostento vengo a formular demanda de Juicio Cambiario contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], con base en los siguientes:

HECHOS

PRIMERO.- En razón del crédito derivado de las relaciones comerciales entabladas entre partes, mi mandante libró y es tenedora legítima de una letra de cambio, que fue aceptada por el demandado, y en las que se consignó como domicilio de pago el de la cuenta número [NÚMERO] del Banco [ENTIDAD BANCARIA] de la localidad de [LOCALIDAD], con importe nominal de [IMPORTE] euros ([IMPORTE EN CIFRA] €), fecha de libramiento el [DÍA] de [MES Y AÑO], y vencimiento a ‘noventa días vista’, efecto que se acompaña como documento nº [Nº DE DOCUMENTO].

SEGUNDO.- La letra mencionada fue librada por mi representada a la orden de la Caja de Ahorros [ENTIDAD BANCARIA], y esta tomadora la presentó al vencimiento para su pago en el citado Banco domiciliatario, que denegó el pago, mediante la oportuna declaración firmada y fechada que aparece en el reverso de la cambial que se adjunta como documento nº [Nº DE DOCUMENTO].

TERCERO.- Ante tal impago la Caja de Ahorros tenedora cargó la letra en cuestión en la cuenta de mi principal, libradora, junto con los gastos que había ocasionado y que suman [IMPORTE] euros ([IMPORTE EN CIFRA] €), acompañándose la carta de adeudo bancario por la devolución de la letra como documento nº [Nº DE DOCUMENTO].

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Art. 820 LEC en relación con lo dispuesto en el art. 85.1º LOPJ, en cuanto se previene que será competente el Tribunal de Instancia del domicilio del demandado, fuero necesario controlable de oficio.

II.- LEGITIMACIÓN.

La legitimación activa corresponde al demandante, que se afirma acreedor de lo que se reclama, librador y tenedor legítimo de las letras de cambio base documental del proceso, conforme a los artículos 19 y 49 de la Ley 19/85 de 16 de julio, Cambiaria y del Cheque (LCCh), mientras que la pasiva corresponde al demandado por ser deudor de lo que se reclama que figura como librador aceptante de la letra aportada, ya que en virtud de lo dispuesto en el art. 33 LCCh, por el hecho de la aceptación se obliga a pagar la letra a su vencimiento.

III.- PROCEDIMIENTO.

El juicio cambiario del Capítulo II del Título III del Libro IV "De los procesos especiales" LEC, al que se remite el art. 68 LCCh, reformado por Disposición Final 10ª.4 LEC.

IV.- POSTULACIÓN Y DEFENSA.

Arts. 23 y 31 LEC, según los cuales no se excepciona para el juicio cambiario que la comparecencia en juicio se efectúe por medio de Procurador, y bajo dirección y firma de Letrado.

V.- FUNDAMENTOS MATERIALES.

Se aporta con la demanda la letra de cambio base de este proceso declarativo especial y documental, de las que es tenedor y titular de la acción cambiaria mi mandante, figurando en el reverso de las mismas la nota correspondiente a su impago puesta por el domiciliatario conforme a lo prevenido en el art. 51 LCCh.

Las letras de cambio llevan aparejada ejecución a través de juicio cambiario, conforme al art. 66 LCCh, alternativa de la acción directa derivada de aquéllas respecto del declarativo ordinario, sin necesidad de protesto, para reclamar lo previsto en los arts. 58 y 59 LCCh (art. 49.pfo.2º LCCh).

En base al título aportado y conforme al art. 58 LCCh se reclama el importe nominal de las letra, más los intereses al tipo del 11 % anual estipulados e indicados en la propia letra (art. 6 LCCh, ya que fueron giradas con la fórmula "a noventa días vista"), y los intereses de ambas cantidades desde la fecha de vencimiento al tipo de interés legal del dinero incrementado en dos puntos, más los gastos bancarios ocasionados.

VI.- COSTAS.

Deberán ser impuestas al demandado todas las costas procesales que se causen, aunque pagare en el acto del requerimiento (arts. 394 y 822 LEC).

Por lo expuesto,

SUPLICO AL TRIBUNAL,

que teniendo por presentado este escrito de demanda, en ejercicio de la acción cambiaria directa, se sirva admitirlo teniéndome por parte en la representación que ostento, mandando se sigan conmigo las sucesivas actuaciones, y se sirva admitir proceso especial cambiario por la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) como principal, más la de [IMPORTE] que se calculan por gastos, intereses y costas, sin perjuicio de su ulterior liquidación, y mandando se requiera de pago al deudor, que si no se atendiera, determinará la efectividad del embargo preventivo de bienes suficientes por las cantidades mentadas, se siga el juicio por sus trámites, a fin de que se despache ejecución contra el demandado para pago al acreedor de las cantidades reclamadas, con expresa condena en costas y lo demás procedente,

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
