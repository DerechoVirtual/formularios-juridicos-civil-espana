---
name: demanda-juicio-cambiario-accion-regreso-contra-civ-1152
description: "Demanda de juicio cambiario por acción de regreso contra el librador de un cheque impagado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio cambiario por acción de regreso contra el librador de un cheque impagado

> Formulario **CIV-1152** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio cambiario basada en una acción de regreso contra el librador, deudor del negocio causal (arrendamiento de obra) derivada de un cheque impagado protestado notarialmente en tiempo y forma.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio cambiario por acción de regreso contra el librador de un cheque impagado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio cambiario por acción de regreso contra el librador de un cheque impagado” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:demanda-juicio-cambiario-accion-regreso-contra-civ-1152`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (9 veces)
- [ ] IMPORTE EN CIFRA (7 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] NÚMERO (4 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO
- [ ] ENTIDAD BANCARIA
- [ ] LUGAR
- [ ] Nº DE DOCUMENTO

## Normas que cita el formulario

- art. 820 LEC
- art. 45 LEC
- art. 819 LEC
- art. 821.1 LEC
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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de la entidad [DENOMINACIÓN SOCIAL], domiciliada en [DOMICILIO], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que siguiendo instrucciones de mi mandante, formulo demanda de Juicio Cambiario contra D./Dña. [NOMBRE Y APELLIDOS], vecino de [LOCALIDAD] con domicilio en [LOCALIDAD] (se aportarán todos los datos de identificación, números de teléfono, fax, etc. a fin de su localización; y todos los domicilios que se conozcan y el orden para lograr la comunicación) [NOMBRE Y APELLIDOS], en reclamación del importe impagado de un cheque por la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), demás responsabilidades que se indicarán y costas en base en los siguientes:

HECHOS

PRIMERO.- En pago de una obra ejecutada en su casa por mi mandante al demandado, D./Dña. [NOMBRE Y APELLIDOS] hizo entrega a aquél de un cheque nº [NÚMERO] librado por D./Dña. [NOMBRE Y APELLIDOS] en fecha [FECHA] por la suma de [IMPORTE] euros ( [IMPORTE] €) contra depósito en cuenta corriente a cargo del Banco

Se acompaña como Doc. Nº [NÚMERO], el referido cheque.

SEGUNDO.- Presentado al cobro el mencionado cheque, resultó impagado por el librado Banco [ENTIDAD BANCARIA], por falta de fondos.

Se acompaña como Doc. Nº [NÚMERO] copia del acta de protesto notarial en la que no consta que se haya puesto tacha de falsedad, ni alegado falta absoluta de representación.

TERCERO.- Los gastos ocasionados por el impago del efecto, incluidos los de protesto y comunicaciones, ascienden a [IMPORTE] euros ([IMPORTE EN CIFRA] €). Se acompaña la cuenta de los gastos producidos como Doc. Nº [NÚMERO].

CUARTO.- El diez por ciento del importe del cheque impagado asciende a la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), sumando la cantidad impagada, más los gastos y el recargo del porcentaje que queda indicados, resulta un total de [IMPORTE] euros ([IMPORTE EN CIFRA] €), que constituyen la cantidad reclamada por esta demanda, además de los réditos de las obligaciones impagadas desde la fecha de presentación del cheque, calculados a tipo de interés legal vigente del dinero, incrementado en dos puntos, así como las costas del juicio que, de modo provisional, se estiman en [IMPORTE] euros ([IMPORTE EN CIFRA] €).

FUNDAMENTOS DE DERECHO

I. La competencia territorial corresponde a los Tribunales de esta población, por ser el lugar del domicilio de los demandados, conforme al art. 820 LEC.

II.- Por lo que se refiere a la competencia objetiva y a la clase de procedimiento, ha de conocer un Tribunal de Instancia (arts. 45 LEC y 85.1º LOPJ), en Juicio Cambiario, de los arts. 819 a 827 LEC, conforme indica art. 68 de la Ley Cambiaria y del Cheque 19/85 de 16 de Julio (LCCh), reformado por Disposición Final 10ª.4 LEC.

III. La legitimación activa deriva de acreditarse por mi representado la calidad de portador del cheque a quien le conceden acción para reclamar contra el librador mediante protesto notarial los arts. 146 y 148 LCCh, y por lo que respecta a la pasiva, proviene de aseverarse la calidad de librador firmante que ostenta D./Dña. [NOMBRE Y APELLIDOS], demandado.

IV.- Arts. 23 y 31 LEC, según los cuales no se excepciona para el juicio cambiario que la comparecencia en juicio se efectúe por medio de Procurador, y bajo dirección y firma de Letrado.

V. La acción emana de un cheque, que es un título que lleva aparejada ejecución, sin necesidad de reconocimiento judicial de firma, a través del juicio cambiario, procedimiento a los que se remiten los nuevos contenidos de arts. 66 y 68, a que reenvía el art. 153, todos LCCh.

El título se acompaña a esta demanda, como exige el art. 821.1 LEC.

La corrección formal deriva de que contiene el cheque todos y cada uno de los requisitos de arts. 106 a 119 LCCh.

VI. La acción es de regreso —no hay acción directa en el cheque—, y de entre quienes el portador tiene derecho a demandar, individual o conjuntamente, sin beneficio de orden (art. 148 LCCh), al no haber circulado el cheque, permanece solo el librador, deudor del negocio causal, frente al portador acreedor inicial, mi mandante.

El cheque ha sido protestado en tiempo y forma, al día siguiente de la presentación al cobro, por su vencimiento, conforme al art. 146 LCCh.

VII. Art. 149 LCCh: "El tenedor puede reclamar de aquel contra quien se ejercita la acción: 1º: El importe del cheque no pagado; 2º: Los réditos de dicha cantidad devengados desde el día de la presentación del cheque calculados al tipo legal de interés del dinero aumentado en dos puntos; 3º: Los gastos, incluidos los de protesto y las comunicaciones; 4º: El 10% del importe no cubierto del cheque "

VIII. Aunque atienda el deudor en el acto del requerimiento de pago, serán de su cargo las costas causadas, conforme al art. 822 LEC.

En su virtud,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito, con el título y documentos que lo acompañan y copias de todo ello, se sirva tenerme por comparecido y parte en la representación que ostento, y se admita la corrección formal del cheque, y por ello la demanda de juicio cambiario contra D./Dña. [NOMBRE Y APELLIDOS] en reclamación de la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), más los intereses legales y costas procesales, en la cantidad que por ahora, y sin perjuicio de definitiva liquidación, se calcula de [IMPORTE] euros ([IMPORTE EN CIFRA] €), se requiera al demandado de pago en plazo legal, y se proceda a trabar inmediato embargo preventivo de bienes suficientes para responder de la cantidad reseñada para caso de no ser abonada toda, y siguiendo el juicio por sus trámites, se formule de adverso o no la oposición, bien se dicte auto por el que se despache la ejecución, bien se dicte, por trámite de juicio verbal, sentencia por la que se declare al demandado responsable del pago de las cantidades reclamadas, en todo caso para pasar a hacer trance hasta remate de los bienes embargados, y con su producto pago completo a mi representada de lo que se acredite por los conceptos indicados,

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
