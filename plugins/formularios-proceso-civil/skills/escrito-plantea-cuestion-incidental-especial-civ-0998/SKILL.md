---
name: escrito-plantea-cuestion-incidental-especial-civ-0998
description: "Escrito que plantea cuestión incidental de especial pronunciamiento en juicio ordinario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito que plantea cuestión incidental de especial pronunciamiento en juicio ordinario

> Formulario **CIV-0998** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito formulando cuestión incidental de especial pronunciamiento, en juicio ordinario.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito que plantea cuestión incidental de especial pronunciamiento en juicio ordinario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito que plantea cuestión incidental de especial pronunciamiento en juicio ordinario” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-plantea-cuestion-incidental-especial-civ-0998`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] FECHA (4 veces)
- [ ] CALLE (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] CONTENIDO DEL DOCUMENTO
- [ ] IMPORTE EN CIFRA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 389 LEC
- art. 387 LEC
- art. 809.2 LEC

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

Notas al pie del formulario original:
(1) La postulación es la misma que sea exigible en el pleito principal, puesto que no se establece ninguna excepción en los artículos 23 y 31 de la LEC.

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

N. de R.: Se contempla en este supuesto una cuestión improcedente que es resuelta por auto repeliendo el planteamiento de la misma. Ver (Auto)

AL TRIBUNAL

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], según tengo acreditado debidamente, ante el Tribunal comparezco en autos de juicio Ordinario nº [Nº DE PROCEDIMIENTO] /, seguidos a instancias de D./Dña. [NOMBRE Y APELLIDOS], y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, y al amparo del art. 389 LEC, vengo a formular cuestión incidental de especial pronunciamiento, en base a los siguientes:

HECHOS

PRIMERO.- La cuestión nodal del litigio consiste acordar la liquidación de la sociedad de gananciales que existió como régimen de bienes legal supletorio en el matrimonio que unía al demandante Sr./a. con la demandada Sr./a [NOMBRE Y APELLIDOS] hasta que se disolvió a virtud de la sentencia de la Audiencia Provincial de [LOCALIDAD] de [LOCALIDAD].

SEGUNDO.- La discrepancia radica en el momento a que debe atenderse para determinar el inventario del patrimonio ganancial, y en las bases del inventario conforme al cual deba practicarse la liquidación, avalúo y adjudicación de haberes a los ex-cónyuges.

TERCERO.- Según pura lógica jurídica, primero es determinar lo partible, luego valorar, más tarde dividir, y por último adjudicar, y esta parte está en estos momentos en condiciones de pretender que se excluya del inventario partible de esta liquidación de bienes gananciales la propiedad del inmueble que constituye domicilio familiar, apartamento "dúplex", trasteros y plaza de garaje, sito al nº [NÚMERO] de la calle [CALLE] de [LOCALIDAD], por no corresponder a la comunidad conyugal, sino que la compraventa de fecha [FECHA], fue un negocio simulado relativamente de donación modal del difunto padre de mi mandante D./Dña. [NOMBRE Y APELLIDOS], por lo que es bien privativo.

A tal objeto, se aporta documento privado de fecha [FECHA], que recientemente ha sido descubierto, en que consta [CONTENIDO DEL DOCUMENTO]

FUNDAMENTOS DE DERECHO

I

El incidente, conforme a la doctrina, es una cuestión anormal del proceso, que no pertenece a su orden lógico, y se constituye en crisis objetiva del mismo. Siendo algo distinto del objeto principal del pleito (división de un patrimonio), guarda con éste relación inmediata (pertenencia de un bien al patrimonio divisible), y surge después de planteada demanda y contestación (art. 387 LEC).

II

La cuestión de titularidad del inmueble que se coloca en principal activo del patrimonio ganancial partible, exige que el Tribunal decida sobre ella separadamente en la sentencia antes de entrar a resolver sobre lo que es objeto principal, esto es, las cuota-partes que se adjudiquen a los comuneros de la comunidad conyugal, y por lo tanto, se trata de una cuestión de especial pronunciamiento (art. 389 LEC).

Así análogamente, se preveé un incidente en la formación del inventario cuando se liquida a través del proceso especial, según dispone el art. 809.2 LEC, y era la jurisprudencia en las particiones hereditarias (STS de 21 de mayo de 1992).

III

Las cuestiones incidentales que no tienen señalada en LEC otra tramitación, se ventilan conforme al trámite del art. 393, planteándose por escrito, con aportación documental y solicitud de prueba en su caso, indicándose si tiene el incidente efectos suspensivos o no.

IV

Para determinar lo inventariable en este proceso, en la original tesis de la parte demandante, forma parte del activo el valor económico actualizado del uso en exclusiva del domicilio familiar, que se valora en [IMPORTE] euros ([IMPORTE EN CIFRA] €) por mi representada, que se aventura desde una lectura sesgada de un párrafo de la fundamentación jurídica de la sentencia de divorcio de la instancia, y quiere apoyarse en la STS de 23 de diciembre de 1.993.

El dicho valor se aplica a compensar el crédito de la sociedad de gananciales por el importe de todos los ingresos netos, contraprestación de actividad profesional del actor desde el mes de [MES] de [AÑO], en que abandonó a la ex-esposa, hasta el [FECHA], menos el pobre descuento de las cantidades que se reconoce se entregaron durante la separación de hecho (unos [IMPORTE] euros mensuales) para el sustento.

Como se dijo en la contestación a la demanda, el uso exclusivo de la vivienda, si el inmueble es común, significa que a la cotitularidad del dominio se adosa una titularidad exclusiva del uso como medida judicial (en caso contrario, cuando fuera privativo del cónyuge al que se reputa judicialmente menos necesitado de protección, se crea un "ius in re" limitativo del dominio, un derecho de habitación erigido por sentencia).

El uso exclusivo del domicilio familiar es una medida judicial adoptable como efecto personal de una ruptura matrimonial, ajena al contenido económico del régimen de bienes entre cónyuges, atendiendo a la tutela y dignidad de la parte detentadora del interés más necesitado de una discriminación positiva, que siempre son los hijos comunes en potestad, y en casos como el de autos, la sola esposa para la que, por sus circunstancias personales y del entorno socioeconómico, la pensión compensatoria tiene un contenido abrumadoramente alimenticio.

Pero el domicilio familiar tampoco es de la comunidad conyugal sino privativo de mi patrocinada, a pesar de la apariencia de una compraventa

(Expresados con claridad los hechos en que se constituye la cuestión incidental, y pidiéndose luego la exclusión de un bien del patrimonio partible, pueda aquí extenderse la fundamentación jurídica —en el caso sobre la validez de los negocios traslativos del dominio y la simulación—, o dejarse para la comparecencia del incidente)

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado el presente escrito con sus copias, y documento adjunto, en mérito de lo alegado se digne admitir a trámite cuestión incidental, que se considera de especial pronunciamiento, se convoque a las partes a comparecencia y seguido que sea el oportuno procedimiento, se venga a pronunciar, con la debida separación, en la Sentencia definitiva, que queda excluida del patrimonio inventariable y de la división objeto de litigio, por ser propiedad privativa de mi patrocinada, el apartamento "dúplex", trasteros y plaza de garaje, sito al nº [NÚMERO] de la calle [CALLE] de [LOCALIDAD], con lo demás que sea procedente en Justicia que pido en

OTROSÍ DIGO: Que interesa al derecho de esta parte el recibimiento del incidente a prueba, proponiendo la siguiente:

A) INTERROGATORIO DE LA PARTE CONTRARIA, que deberá ser citada con los apercibimientos legales de poder se tenido por confeso, en caso de incomparecencia injustificada, de los hechos por los que se intente preguntarle, de que tenga conocimiento personal y le sean perjudiciales.
B) DOCUMENTAL, de unión definitiva al incidente del documento privado que se acompaña a este escrito de planteamiento, y de los públicos y privados acompañados al escrito de contestación a la demanda principal.
C) TESTIFICAL de los siguientes individuos:

D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD]

En su virtud,

SUPLICO AL TRIBUNAL que, teniendo por causadas las anteriores manifestaciones a los efectos oportunos, se digne proveer en consecuencia a fin de que se admita y practique en el acto de la vista la prueba propuesta, según es Justicia que reitero en lugar y fecha ‘ut supra’.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
