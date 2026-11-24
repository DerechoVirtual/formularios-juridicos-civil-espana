---
name: decreto-admite-tramite-medidas-provisionales-previas-civ-1853
description: "Decreto que admite a trámite las medidas provisionales previas a la demanda y cita a los cónyuges. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Decreto que admite a trámite las medidas provisionales previas a la demanda y cita a los cónyuges

> Formulario **CIV-1853** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Decreto del Letrado de la Administración de Justicia por el que se tienen por solicitadas medidas provisionales previas a la demanda de separación del matrimonio, se cita a los cónyuges a la comparecencia del art. 771.2 LEC y se da cuenta al Tribunal para adoptar, si procede, los efectos inmediatos del art. 102 CC.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Decreto que admite a trámite las medidas provisionales previas a la demanda y cita a los cónyuges» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Decreto que admite a trámite las medidas provisionales previas a la demanda y cita a los cónyuges” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:decreto-admite-tramite-medidas-provisionales-previas-civ-1853`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL SOLICITANTE (2 veces)
- [ ] AÑO
- [ ] DATOS DE LOS HIJOS
- [ ] DOMICILIO
- [ ] DÍA
- [ ] FECHA
- [ ] FIRMA
- [ ] GRUPO
- [ ] HORA
- [ ] MES
- [ ] NOMBRE DEL HIJO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº DE CUENTA
- [ ] NÚMERO

## Normas que cita el formulario

- art. 102 CC
- art. 771.1 LEC
- art. 104 CC
- art. 771.2 LEC
- art. 92 CC

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

DECRETO DEL LETRADO/A DE LA ADMINISTRACIÓN DE JUSTICIA

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Sr./Sra. Letrado/a de la Administración de Justicia [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

PRIMERO.– Por D./Dña. [NOMBRE Y APELLIDOS DEL SOLICITANTE], vecino/a de [LOCALIDAD], [DOMICILIO], se ha presentado escrito que solicita la adopción de medidas provisionales previas a la demanda que se propone promover frente a D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], sobre separación del matrimonio, acompañando [NÚMERO] documentos.

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]
— De lo expuesto por la parte solicitante se desprende que no existen hijos menores ni hijos con discapacidad con medidas de apoyo en el matrimonio.
— De lo expuesto por la parte solicitante se desprende que existen hijos menores o con discapacidad con medidas de apoyo en el matrimonio: [DATOS DE LOS HIJOS].

SEGUNDO.– En el mismo escrito se solicita la adopción inmediata de los efectos del art. 102 CC y la medida provisional de la salida de D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE] del domicilio familiar, con atribución del uso exclusivo del mismo y del ajuar doméstico al solicitante [ELEGIR: y a su hijo/a [NOMBRE DEL HIJO/A] / (suprimir si no hay hijos)].

FUNDAMENTOS DE DERECHO

PRIMERO.– Este Tribunal es competente territorialmente para conocer de las medidas solicitadas, por tener su domicilio la parte solicitante en esta circunscripción (art. 771.1 LEC).

SEGUNDO.– Procede la adopción de las medidas provisionales con carácter previo a la presentación de la demanda en los procesos matrimoniales, a petición de cualquiera de los cónyuges (art. 104 CC y art. 771.1 LEC).

TERCERO.– Previamente a la adopción de las medidas, el LAJ debe convocar a las partes a la comparecencia prevista en el párrafo 1.º del art. 771.2 LEC.

CUARTO.– Establece el art. 771.2 LEC, párrafo 2.º, que de la misma resolución convocando a la comparecencia se dará cuenta en el mismo día al Tribunal para la adopción, si procede, de los efectos a que se refiere el art. 102 CC, custodia de los hijos y uso de la vivienda y ajuar familiares.

PARTE DISPOSITIVA

1.– Se tienen por solicitadas por D./Dña. [NOMBRE Y APELLIDOS DEL SOLICITANTE] medidas provisionales previas a la demanda que se propone promover frente a D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], sobre separación del matrimonio.

2.– Cítese a los expresados cónyuges a una comparecencia, que tendrá lugar en la Sala de Audiencias de este Tribunal el día [FECHA], a las [HORA] horas.

3.– En la cédula de citación infórmese a los cónyuges del objeto de la comparecencia y adviértaseles:

a) Que deben acudir asistidos de abogado y representados por procurador.

b) Que deben acudir con las pruebas de que intenten valerse.

c) Que, dentro de los cinco días siguientes a la citación, deben indicar qué personas, por no poder presentarlas ellos mismos, deben ser citadas por el tribunal para que declaren como partes o como testigos, facilitando los datos y circunstancias precisas para su citación (art. 440, párrafo 4.º, LEC).

d) Que, si pretenden recabar el informe de especialistas al que se refiere el art. 92 CC, deben solicitarlo igualmente dentro de los tres días siguientes a la recepción de la citación.

e) Que su falta de asistencia puede determinar que se consideren como ciertos los hechos alegados por su cónyuge para fundamentar sus peticiones sobre medidas provisionales de carácter patrimonial.

4.– Dése cuenta en el día de hoy al Tribunal de la petición de medidas inmediatas para que resuelva lo que proceda.

Así lo acuerdo y firmo.

Firma del Letrado/a de la Administración de Justicia: [FIRMA]

Contra esta resolución cabe interponer recurso de reposición, mediante escrito ante el LAJ que se presentará dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, y sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesaria la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [Nº DE CUENTA], indicando en el campo concepto del resguardo de ingreso que se trata de un «Recurso» código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.
