---
name: demanda-ejecutiva-basada-auto-cuantia-maxima-seguro-civ-1618
description: "Demanda ejecutiva basada en auto de cuantía máxima por el seguro obligatorio de vehículos de motor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva basada en auto de cuantía máxima por el seguro obligatorio de vehículos de motor

> Formulario **CIV-1618** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda ejecutiva contra compañía de seguros fundada en un Auto de cuantía máxima dictado por la Sección de Instrucción del Tribunal de Instancia por hechos cubiertos por seguro obligatorio de responsabilidad civil derivada del uso y circulación de vehículos a motor, sin que hasta la fecha se haya procedido a su abono por la aseguradora.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva basada en auto de cuantía máxima por el seguro obligatorio de vehículos de motor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva basada en auto de cuantía máxima por el seguro obligatorio de vehículos de motor” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-basada-auto-cuantia-maxima-seguro-civ-1618`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] IMPORTE EN CIFRA (6 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] MATRÍCULA (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] ASEGURADORA (2 veces)
- [ ] MARCA/MODELO (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE DOCUMENTO
- [ ] PARTE DEMANDADA
- [ ] PLAZO
- [ ] SEDE

## Normas que cita el formulario

- art. 52.1.9.º LEC
- art. 517.2.8.º LEC
- art. 539.1 LEC
- art. 517 LEC
- art. 539.2 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a. de los Tribunales, actuando en nombre y representación de [NOMBRE DEL REPRESENTADO/A], con domicilio en [LOCALIDAD] y D.N. I. número [NÚMERO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que en la representación que ostento formulo DEMANDA EJECUTIVA contra la Compañía de Seguros [ASEGURADORA], con domicilio en [LOCALIDAD], en reclamación de la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) en concepto de principal e intereses ordinarios y moratorios vencidos, más otros [IMPORTE] euros ([IMPORTE EN CIFRA] €) presupuestados provisionalmente para hacer frente a los intereses que, en su caso, puedan devengarse durante la ejecución y a las costas de ésta, demanda que formulo con base en los siguientes

HECHOS

PRIMERO.- El día [FECHA] se produjo un accidente de tráfico que tuvo lugar en la localidad de [LOCALIDAD] y en el que se vieron involucrados mi cliente, como conductor del vehículo modelo [MARCA/MODELO], matrícula [MATRÍCULA] del que es propietario y que en ese momento se hallaba asegurado por la Compañía [ASEGURADORA], y D./Dña. [NOMBRE Y APELLIDOS], titular del vehículo modelo [MARCA/MODELO], matrícula [MATRÍCULA], asegurado por Seguros

En el citado accidente de circulación intervino la Guardia Civil de Tráfico que levantó el correspondiente atestado, en el que tras las correspondientes declaraciones de los implicados, observar in situ los vehículos y levantar el pertinente croquis, se concluía que la causa probable del accidente era la invasión del vehículo matrícula [MATRÍCULA] la parte izquierda de la calzada.

SEGUNDO.- Como consecuencia del citado accidente de circulación mi representado sufrió una serie de lesiones que motivaron que permaneciera incapacitado durante [PLAZO], quedándole unas secuelas consistentes en

Aplicando el baremo a mi patrocinado le correspondería percibir las siguientes cantidades [IMPORTE]

TERCERO.- A raíz de todo lo acontecido se incoaron por la Sección de Instrucción del TI número [NÚMERO] de [LOCALIDAD], las Diligencias Previas número [NÚMERO], que posteriormente se convirtieron en el Juicio por delito leve número [NÚMERO] de dicho Tribunal, cuyos archivos dejamos designados a los efectos oportunos.

CUARTO.- El día [FECHA] se dictó sentencia en los citados autos de Juicio por delito leve que fue absolutoria para el denunciado D./Dña. [NOMBRE Y APELLIDOS], si bien con posterioridad se dictó por el mismo Tribunal el auto de fecha [FECHA] en el que se establecía como cantidad máxima a reclamar la de [IMPORTE] euros ([IMPORTE EN CIFRA] €) a cargo de la aseguradora ahora demandada y a favor de mi mandante como perjudicado en el citado accidente de circulación. El auto citado adquirió firmeza, acompañándose el correspondiente testimonio con la presente demanda.

QUINTO.- Por mi patrocinado se ha intentado infructuosamente percibir de parte de la aseguradora la cantidad fijada, viéndose obligado a interponer la correspondiente demanda.

SEXTO.- Mi representado tiene conocimiento de que el ejecutado es titular de los siguientes bienes susceptibles de embargo [DESCRIPCIÓN DEL BIEN], bienes que son suficientes para el fin de la ejecución.

A los anteriores hechos resultan de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.-

El Juez territorialmente competente para la ejecución del Auto de cuantía máxima, previsto en los artículos 13 y 17 del Texto Refundido de la Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor, es el del lugar en que se causaron los daños, en atención a lo establecido en el art. 52.1.9.º LEC, por constituir dicho Auto de Cuantía máxima un título judicial, recogido en el art. 517.2.8.º LEC, lo que excluye la aplicación del art. 545.3, y su remisión a los arts. 50 y 51 de dicho cuerpo legal (Acuerdo de la Sala Primera del TS de 11-3-2004).

II.- LEGITIMACIÓN.-

El art. 538 de la Ley de ritos regula que es parte en el proceso de ejecución la persona o personas que piden y obtienen el despacho de la ejecución y la persona o personas frente a las que ésta se despacha, añadiendo que sólo podrá despacharse ejecución a instancia de quien aparezca como acreedor en el título ejecutivo frente a, entre otros, quien aparezca como deudor en el mismo título.

En el presente caso, mi representado es acreedor frente al ejecutado de un crédito dinerario derivado de un auto de cantidad máxima por hechos ocasionados por el uso y circulación de vehículos de motor, por lo que tienen legitimación activa y pasiva, respectivamente.

III.- POSTULACIÓN.-

Conforme a lo dispuesto en el art. 539.1 de la LEC, la demanda viene firmada por abogado y Procurador/a., ya que es preceptiva la intervención de dichos profesionales.

IV.- TÍTULO.-

El art. 517 de la LEC dispone que la acción ejecutiva deberá fundarse en un título que tenga aparejada ejecución, encontrándose entre éstos el auto que establezca la cantidad máxima reclamable en concepto de indemnización, dictado en casos de rebeldía del acusado o de sentencia absolutoria o sobreseimiento en procesos penales incoados por hechos, cubiertos por el Seguro Obligatorio de Responsabilidad Civil derivada del uso y circulación de vehículos de motor.

Los artículos 13 y 17 del Texto Refundido de la Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor regulan el contenido del auto de cantidad máxima a los efectos de constituir título ejecutivo.

V.- REQUISITOS FORMALES.-

La presente demanda contiene todos los requisitos enumerados en el art. 549 de la Ley Procesal Civil, ya que se ha indicado cual es el título en que se funda, la tutela ejecutiva que se pretende y las personas frente a las que se interesa el despacho de la ejecución y los bienes del ejecutado susceptibles de embargo conocidos por mi poderdante. Por último se acompaña a la demanda ejecutiva la documentación necesaria de la contemplada en el art. 550 del mismo texto legal.

VI.- INTERESES.-

Procede la condena al pago del interés del art. 20.4.º de la Ley del Contrato de Seguro, en virtud de lo dispuesto en el artículo 9 del Texto Refundido de la Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor.

VII.- COSTAS.-

En virtud de lo dispuesto en el art. 539.2 en relación con el 583 de la LEC, las costas de esta ejecución deberán ser impuestas al ejecutado, ya que ha sido quien ha originado la necesidad de este procedimiento al no haber cumplido con lo establecido en el contrato suscrito por las partes en que se basan las presentes actuaciones.

De conformidad con lo anteriormente expuesto,

SUPLICO AL TRIBUNAL:

Que teniendo por presentado este escrito con los documentos acompañados y copia de todo ello, se sirva admitirlo, ordenando se entiendan conmigo las sucesivas diligencias y en nombre de mi patrocinado se me tenga por comparecido y parte y por presentada demanda ejecutiva para que, una vez examinados los requisitos y presupuestos procesales, el título ejecutivo y los actos de ejecución que se solicitan, así como la propia competencia, se despache ejecución frente a [PARTE DEMANDADA] por el importe de la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) en concepto de principal, [IMPORTE] euros ([IMPORTE EN CIFRA] €) en concepto de intereses devengados hasta la fecha, más otros [IMPORTE] euros ([IMPORTE EN CIFRA] €) presupuestados provisionalmente para los intereses que puedan generarse durante la ejecución y las costas de ésta, procediéndose a requerir de pago al deudor y si no pagase en el acto, el tribunal procederá al embargo de los bienes designados en la relación fáctica de esta demanda, todo ello con la finalidad de que mi poderdante sea satisfecho en la totalidad de la deuda de la que esta ejecución dimana, con imposición de las costas derivadas de esta ejecución al ejecutado.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
