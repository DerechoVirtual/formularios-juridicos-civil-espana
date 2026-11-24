---
name: solicitud-ejecucion-prestaciones-periodicas-sentencia-civ-0351
description: "Solicitud de ejecución de prestaciones periódicas de la sentencia de separación y las provisionales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de ejecución de prestaciones periódicas de la sentencia de separación y las provisionales

> Formulario **CIV-0351** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito solicitando la ejecución de prestaciones periódicas a cuyo pago condena la sentencia de separación, así como la ampliación automáticamente de la ejecución por el importe correspondiente a los nuevos vencimientos de principal de pensiones adeudadas.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de ejecución de prestaciones periódicas de la sentencia de separación y las provisionales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de ejecución de prestaciones periódicas de la sentencia de separación y las provisionales” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-ejecucion-prestaciones-periodicas-sentencia-civ-0351`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] AÑO (7 veces)
- [ ] IMPORTE (7 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DEL HIJO/A (2 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] TIPO DE INTERÉS (2 veces)
- [ ] APELLIDOS
- [ ] CALLE
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] FOLIO
- [ ] LUGAR
- [ ] Nº DE PABELLÓN
- [ ] Nº DE POLÍGONO
- [ ] PORCENTAJE
- [ ] SEDE
- [ ] TOMO

## Normas que cita el formulario

- art. 549.2 LEC
- art. 575.1 LEC
- art. 776 LEC
- art. 773.5 LEC
- art. 774.5 LEC
- art. 578 LEC

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) En la práctica no parece que se esté empleando el art. 578 LEC para la ejecución de las medidas, provisionales o definitivas, por pensiones alimenticias o compensatorias de los procesos especiales matrimoniales, sino que usa en negocios jurídicos con prestaciones aplazadas que son títulos ejecutivos extrajurisdiccionales, no obstante lo cómodo que sería para el indicado servicio. Puede deberse a que no hay concierto en seguir los pasos de los modelos, que no parecen seriamente objetables. Desde luego, cuando el art. 578.2, párrafo 2.º LEC habla de liquidación final como condición de la solicitud ejecutiva, habrá de referirse a una prospección de la que resulte una vez se produzca el pago final de la prestación periódica toda, sin excluir pagos parciales. En cualquier caso, un despacho especial de la ejecución, y los aumentos de embargo (o mejoras de embargo, que significaría traba de otros bienes del ejecutado) por vencimientos ulteriores del débito, son siempre rogados.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de Doña [NOMBRE Y APELLIDOS], como tengo debidamente acreditado mediante escritura de poder que obra en autos de juicio de separación contenciosa n.º [Nº]/[AÑO], seguido en ese Tribunal frente a Don MARIANO [APELLIDOS] a instancias de mi poderdante, comparezco y como mejor en Derecho proceda, DIGO:

Que interesa a mi patrocinada obtener la ejecución, con arreglo a los arts. 776 y 517 y ss. LEC, de las medidas provisionales y definitivas del juicio de separación referenciado, frente al condenado Don [NOMBRE Y APELLIDOS], provisto de DNI n.º [DNI/NIE], domiciliado en [DOMICILIO], calle [CALLE], n.º [NÚMERO], siendo la empresa para la que trabaja [DENOMINACIÓN SOCIAL], sita en [LOCALIDAD], polígono [Nº DE POLÍGONO], pabellón [Nº DE PABELLÓN], lo cual se establece subsidiariamente para los actos de comunicación, si no fuere hallado en el domicilio, con base en los siguientes:

HECHOS

PRIMERO.- Por sentencia de ese Tribunal de fecha [FECHA], además de declararse la separación judicial de Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS], se acordaron como medidas definitivas sendas pensiones alimenticias a cargo del demandado y en favor de sus dos hijos matrimoniales, [NOMBRE DEL HIJO/A] y [NOMBRE DEL HIJO/A], de 300 euros cada una, pagaderas mensualmente, dentro de los cinco primeros días de cada mes, mediante ingreso en la cuenta bancaria que señalara la madre, actualizables cada año conforme al índice de precios al consumo que publique el INE u organismo que lo sustituya.

Anteriormente, por auto de fecha [FECHA] se acordaron medidas provisionales en pieza separada del juicio de separación referenciado, que incluían pensión de levantamiento de cargas familiares a cargo del demandado y en favor de la esposa e hijos comunes de 500 euros mensuales, igualmente pagaderos dentro de los cinco primeros días de cada mes, mediante ingreso en la cuenta bancaria que señalara Doña [NOMBRE Y APELLIDOS], actualizables cada año conforme al índice de precios al consumo que publique el INE u organismo que lo sustituya.

SEGUNDO.- Don [NOMBRE Y APELLIDOS] no ha satisfecho ni uno solo de los pagos a que viene obligado, y el art. 549.2 LEC autoriza a que la demanda ejecutiva se limite en este caso a la solicitud de que se despache ejecución, identificando la resolución cuya ejecución se pretende.

Por consiguiente, a la fecha de esta presentación, adeuda:

Medidas provisionales:

- meses del año [AÑO], a 500 euros, son un principal de [IMPORTE] euros.
- incremento del IPC en año [AÑO], [PORCENTAJE] %, actualiza la pensión a 513,11 euros.
- meses del año [AÑO], a 513,11 euros, son un principal de [IMPORTE] euros.

Medidas definitivas:

meses, a 600 euros, son un principal de [IMPORTE] euros.

Intereses de mora procesal vencidos:

-sobre las cantidades de 500 euros como capital desde el sexto día de cada mes adeudado de año [AÑO], al tipo [TIPO DE INTERÉS] anual; de 513,11 euros como capital desde el sexto día de cada mes del año [AÑO] hasta el mes de [MES], al tipo [TIPO DE INTERÉS] anual; y a este mismo tipo anual desde el sexto día del mes [MES] por cada vencimiento de 600 euros hasta el día de la fecha (art. 575.1 LEC).

Total por principal e intereses vencidos de [IMPORTE] euros ( [IMPORTE] €)

Presupuesto para intereses por devengar y costas: [IMPORTE] euros ( [IMPORTE] €).

Conforme a estos cálculos se presentará liquidación final de la deuda.

TERCERO.- Los títulos jurisdiccionales citados son ejecutivos con arreglo a lo dispuesto en el art. 776 LEC, por relación al art. 517.2. 1.º y 9.º LEC, en tanto que el auto de medidas provisionales es firme, y sólo queda sin efecto por las medidas definitivas de sentencia (art. 773.5 LEC), y la sentencia de separación, aunque ha sido recurrida en apelación por la parte contraria, no ve suspendida la eficacia de las medidas que se hubieran acordado en aquélla, deviniendo firme el pronunciamiento sobre la separación (art. 774.5 LEC).

CUARTO.- Habiéndose de despachar ejecución por deuda de cantidad líquida con vencimientos periódicos, se solicita la ampliación automática a los sucesivos vencimientos mensuales por principal, actualizado anualmente, e intereses legales procesales, salvo que en las fechas de los vencimientos, quinto día de cada mensualidad, consigne el demandado a disposición del Tribunal las cantidades correspondientes, de conformidad con lo dispuesto en el art. 578 LEC, y sin perjuicio de presentar una liquidación final de la deuda.

QUINTO.- Se señala a efectos de embargo los créditos de Don [NOMBRE Y APELLIDOS] frente a la empresa [DENOMINACIÓN SOCIAL], cuya sede ya se ha indicado, por el precio facturado por su actividad de agente comercial afecto, que no se reputan suficientes, por lo que se señala también el pequeño predio rústico en [LOCALIDAD], finca registral n.º [NÚMERO], inscrita en el Registro de la Propiedad de [LOCALIDAD], al tomo [TOMO], folio [FOLIO], considerándola suficiente, siempre y cuando la misma se hallare libre de cargas y gravámenes.

Se solicitan como medidas de garantía del embargo la orden de retención y puesta a disposición del Tribunal librada a [DENOMINACIÓN SOCIAL], y la anotación preventiva de embargo de la finca en el Registro de la Propiedad.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, por presentado este escrito con sus copias, se sirva admitirlo, tenerme por personada y parte en la representación que ostento, y despache ejecución frente a Don [NOMBRE Y APELLIDOS], en razón del auto de medidas provisionales y sentencia de medidas definitivas de la separación contenciosa nº [Nº]/[AÑO] de que conocía el Tribunal, por cantidad de DDeuros (€), correspondientes a principal e intereses vencidos deeuros, y laeuros, que se presupuestan provisionalmente para intereses y costas del procedimiento, y acuerde ampliar automáticamente la ejecución por el importe correspondiente a los nuevos vencimientos de principal de pensiones adeudadas, es decir, por la suma de seiscientos euros, actualizables anualmente, conforme al detalle del cuerpo de este escrito, todo ello sin perjuicio de la definitiva liquidación.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
