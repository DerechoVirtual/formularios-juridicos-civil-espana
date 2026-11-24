---
name: demanda-contenciosa-modificacion-medidas-reducir-civ-0013
description: "Demanda contenciosa de modificación de medidas para reducir la pensión de alimentos de un hijo menor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contenciosa de modificación de medidas para reducir la pensión de alimentos de un hijo menor

> Formulario **CIV-0013** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda contenciosa de modificación de medidas definitivas por la que el progenitor obligado al pago solicita la reducción de la pensión de alimentos de un hijo menor de edad, por haberse producido una alteración sustancial de sus circunstancias económicas (en el modelo, pérdida del empleo y paso a subsidio de desempleo), conforme al art. 775 LEC.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contenciosa de modificación de medidas para reducir la pensión de alimentos de un hijo menor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contenciosa de modificación de medidas para reducir la pensión de alimentos de un hijo menor” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-contenciosa-modificacion-medidas-reducir-civ-0013`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (9 veces)
- [ ] FECHA (7 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO/A (5 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (5 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] AÑO (3 veces)
- [ ] NOMBRE DEL HIJO/A (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] SEDE (2 veces)
- [ ] CLASE DE PROCEDIMIENTO
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL DE LA EMPRESA
- [ ] DOCUMENTO ACREDITATIVO
- [ ] DÍA
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] SECTOR

## Normas que cita el formulario

- art. 775.1 LEC
- art. 81 CC
- art. 749.2 LEC
- art. 770 LEC
- art. 775.2 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…son de mutuo acuerdo o propuestas por un cónyuge con el consentimiento del otro.»: comprobar la redacción vigente del art. 775 LEC tras la Ley 42/2015, la Ley 8/2021 y la LO 1/2025.

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

A LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA DE [SEDE] [OPCIONAL — si ha lugar: Y, EN SU DEFECTO, A LA SECCIÓN CIVIL O SECCIÓN ÚNICA COMPETENTE POR RAZÓN DE LA MATERIA]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº DE DOCUMENTO], y bajo la dirección técnica de D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], Letrado/a ejerciente en el Ilustre Colegio de la Abogacía de [COLEGIO], con despacho abierto en [LOCALIDAD], calle [DOMICILIO], ante el Tribunal comparezco y, como mejor proceda en Derecho,

DIGO

Que mediante el presente escrito formulo DEMANDA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A], cuyo domicilio es [DOMICILIO], basándola en los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A] y mi representado/a se hallan [ELEGIR: separados / divorciados] en virtud de sentencia firme de fecha [FECHA], dictada por [ÓRGANO JUDICIAL QUE DICTÓ LA SENTENCIA: Sección de Familia, Infancia y Capacidad / Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]], en los autos de [CLASE DE PROCEDIMIENTO] n.º [Nº DE PROCEDIMIENTO].

SEGUNDO.- En el fallo de la citada sentencia se adoptaba como medida definitiva, entre otras, la fijación de una cantidad de [IMPORTE] euros mensuales para alimentos del hijo común menor de edad [NOMBRE DEL HIJO/A], a cargo de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE].

TERCERO.- Dicha sentencia, que es firme y ejecutoria, no ha sido modificada por ninguna otra resolución firme. Se acompaña testimonio de la sentencia como DOCUMENTO N.º [Nº DE DOCUMENTO].

CUARTO.- Al tiempo de recaer dicha resolución mi patrocinado/a disponía de un puesto de trabajo remunerado en la empresa [DENOMINACIÓN SOCIAL DE LA EMPRESA], percibiendo unos ingresos netos de [IMPORTE] euros.

QUINTO.- Como consecuencia de la crisis sufrida por el sector de [SECTOR], D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] fue despedido/a en fecha [FECHA], encontrándose actualmente en situación de desempleo, como se acreditará oportunamente.

Desde el [FECHA] hasta el [FECHA], el demandante pasa a percibir una cantidad de [IMPORTE] euros en concepto de subsidio de desempleo, y desde el [FECHA] hasta el [FECHA] la cantidad subsidiada se reduce a [IMPORTE] euros, como acredita la certificación que se acompaña como documento número [Nº DE DOCUMENTO].

Las circunstancias económicas del/de la demandante, desde la sentencia de [ELEGIR: separación / divorcio], han sufrido una modificación peyorativa y, de un sueldo superior a [IMPORTE] euros mensuales, ha pasado a ganar [IMPORTE] euros, reducción que debe considerarse sustancial.

SEXTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO: MEDIACIÓN / NEGOCIACIÓN ENTRE ABOGADOS / OTRO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento n.º [Nº DE DOCUMENTO] [DOCUMENTO ACREDITATIVO].

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA

Conforme a lo establecido por el art. 775.1 LEC, en la redacción dada por la Ley 42/2015, de 5 de octubre, es competente para conocer del presente procedimiento el Tribunal al que me dirijo, por ser el que acordó la medida que se quiere modificar.

II.- LEGITIMACIÓN

La legitimación activa y pasiva para intervenir en el procedimiento corresponde a ambos progenitores (arts. 81, 86, 90 y 91 CC). Con arreglo al art. 749.2 LEC, deberá ser parte el Ministerio Fiscal, por existir hijos menores en el matrimonio.

III.- PROCEDIMIENTO

La modificación de las medidas definitivas tiene asignado el procedimiento previsto en el art. 770 de la LEC, o lo que es lo mismo, los trámites del procedimiento principal de separación o divorcio, de conformidad con la redacción del art. 775.2 LEC dada por la Ley 15/2005, de 8 de julio, dado que no son de mutuo acuerdo o propuestas por un cónyuge con el consentimiento del otro.

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3, en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- FUNDAMENTOS DE DERECHO MATERIALES O SOBRE EL FONDO DEL ASUNTO

La modificación de medidas solicitada tiene su amparo legal en el art. 91, párrafo primero, in fine, del CC, esto es, en una alteración de las circunstancias fácticas sobre las que se proyectó la fijación de las concretas medidas acordadas anteriormente con motivo de la [ELEGIR: separación / divorcio], prevención que es presupuesto de este proceso, según la mención explícita del art. 775.1 LEC; y dicha alteración ha de calificarse como sustancial, es decir, de importancia, afectando no a aspectos secundarios o accesorios: la sentencia de [ELEGIR: separación / divorcio] es de [AÑO]; en [AÑO] el/la demandante pierde su trabajo como consecuencia del despido, y en el mismo año hasta la actualidad pasa a percibir el subsidio de desempleo. Se ha pasado de una situación de trabajo a una de paro subsidiado, lo que de por sí permite considerar cumplido el presupuesto fáctico del art. 91 citado.

Y para restablecer el equilibrio de las consideraciones fácticas y jurídicas tenidas en cuenta en la cuantificación de la sentencia de [ELEGIR: separación / divorcio], ha de fijarse una nueva cuantía que tenga en cuenta la importancia de la disminución de ingresos y que, a ser posible, mantenga la proporcionalidad entre éstos y la pensión alimenticia que se observó en aquella sentencia anterior. Con tales parámetros procede fijar una cantidad de [IMPORTE] euros como nueva pensión a abonar por D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] a D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A] en concepto de pensión por alimentos para su hijo común [NOMBRE DEL HIJO/A], a satisfacer dentro de los cinco primeros días de cada mes y actualizable conforme al IPC cada año, habida cuenta que el importe del subsidio no alcanza los [IMPORTE] euros mensuales, todo ello sin perjuicio de nueva modificación, a favor o en contra, cuando se produzcan nuevas alteraciones sustanciales de las circunstancias.

VI.- COSTAS

No hay razón para inaplicar el principio del vencimiento en punto a costas procesales, en armonía con el art. 394 LEC, a fin de que esta parte salga indemne de que se le reconozca su derecho frente a la resistencia de la parte demandada.

En su virtud,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito junto con los documentos y copias que se acompañan, se sirva admitirlo, teniéndome por parte en la representación que acredito y por formulada solicitud de modificación de medidas definitivas contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A], y previos los trámites legales, se dicte sentencia por la que se acuerde la modificación de las medidas que se establecieron en la sentencia de [ELEGIR: separación / divorcio] de fecha [FECHA], y en su lugar se fije una cantidad de [IMPORTE] euros mensuales a abonar por D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] a D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A] en concepto de pensión por alimentos para su hijo común [NOMBRE DEL HIJO/A], a satisfacer dentro de los cinco primeros días de cada mes y actualizable conforme al IPC cada año, con expresa condena en costas a la parte demandada.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
