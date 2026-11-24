---
name: contestacion-demanda-alimentos-progenitor-contra-otro-civ-0287
description: "Contestación a la demanda de alimentos de un progenitor contra el otro para hijos menores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda de alimentos de un progenitor contra el otro para hijos menores

> Formulario **CIV-0287** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Contestación a la demanda en solicitud de alimentos para el hijo menor, reclamados por un progenitor al otro.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda de alimentos de un progenitor contra el otro para hijos menores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda de alimentos de un progenitor contra el otro para hijos menores” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-demanda-alimentos-progenitor-contra-otro-civ-0287`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (10 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] AÑO (3 veces)
- [ ] CALLE (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] COLEGIO
- [ ] DÍA
- [ ] FECHA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE COLEGIADO/A
- [ ] NÚMERO

## Normas que cita el formulario

- art. 142 Código Civil
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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de D. [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo la dirección de la Letrada Dña. [NOMBRE Y APELLIDOS], colegiada nº [Nº DE COLEGIADO/A] del Iltre. Colegio de Abogados de [COLEGIO], con despacho abierto en [LOCALIDAD], calle [CALLE], nº [NÚMERO], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que, en la representación que ostento y dentro del plazo legal, vengo a formular, en virtud de lo dispuesto en los artículos 748.4.º y 753 de la Ley de Enjuiciamiento Civil, CONTESTACIÓN A LA DEMANDA EN SOLICITUD DE ALIMENTOS para el menor [NOMBRE DEL MENOR], interpuesta por Dña. [NOMBRE Y APELLIDOS] frente a mi mandante, en base a los siguientes

HECHOS

PRIMERO.- Nada que oponer a lo relatado en el antecedente fáctico primero de la demanda en cuanto que los datos relacionados son ciertos y notorios.

SEGUNDO.- Incierta la versión del correlativo. Por el contrario a lo que se asevera mendazmente en el ordinal segundo de la demanda, mi mandante nunca se ha negado a llegar a un acuerdo con la actora sobre la cantidad con la que debe contribuir al sostenimiento de las obligaciones alimenticias que legalmente le incumben respecto a su hija menor.

Prueba evidente de su voluntad es que, como se reconoce de adverso, mi mandante siempre ha estado pendiente de las necesidades de su hija, habiéndose cumplido, en la medida que permitían sus posibilidades, un régimen de prestación de alimentos a cargo del progenitor no custodio.

A lo que se niega, por considerarlo injustificado, y en realidad, de imposible cumplimiento por su parte, es a llegar al acuerdo que le propone la demandante.

TERCERO.- Absolutamente incierto. La actora, que dice en la demanda ser agente comercial, en realidad tiene título de ingeniero técnico y desempeña un trabajo fijo y estable en la empresa [DENOMINACIÓN SOCIAL] sita en esta Ciudad, calle [CALLE], percibiendo un sueldo mensual de [IMPORTE] euros, además de dos pagas extraordinarias por el importe cada una de ellas de [IMPORTE] euros; y a su salario deben añadirse los incentivos que recibe anualmente por la consecución de objetivos comerciales, que ascienden a una cantidad aproximada de [IMPORTE] euros.

Prorrateando esta cantidad entre los doce meses del año, resulta que percibe mensualmente la cantidad de [IMPORTE] euros, por lo que en realidad los ingresos de la demandante ascienden casi al doble de la cantidad que señala en su escrito de demanda.

Se adjunta a esta exposición, como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO], copia de la última declaración de IRPF de Dña. [NOMBRE Y APELLIDOS] que ha tenido en su poder mi mandante, y certificado del plan de pensiones con la entidad [DENOMINACIÓN SOCIAL], en que consta el capital acumulado al [DÍA] de [MES] de [AÑO].

Mi patrocinado se incorporó al mercado laboral ya el año [AÑO], aunque mediante contratos a tiempo parcial, en actividades de monitor con funciones de asistencia social, y en la actualidad, aunque trabaja para el Ayuntamiento de [LOCALIDAD], carece de una real estabilidad, habiendo percibido [IMPORTE] euros brutos ( [IMPORTE] euros líquidos) en el año [AÑO], y [IMPORTE] euros brutos ( [IMPORTE] euros líquidos) en los tres primeros meses del año corriente, en labores de jornada de seis horas diarias cinco días a la semana. Se adjunta certificación de haberes como documento número [Nº DE DOCUMENTO] y que, como se ve, es muy inferior a la manifestada de adverso.

CUARTO.- No se acepta el correlativo de la demanda en cuanto a la partida correspondiente a los gastos escolares. Aunque mi patrocinado siempre ha querido lo mejor para su hija y no pretende escatimar gastos en materia tan importante, no le parece razonable la asistencia a un colegio no subvencionado, cuyo centro escolar está muy alejado del domicilio de la menor, y que no se ajusta, por su elevado coste de matriculación -al que se añaden el de las actividades extraescolares, pensión completa y transportes- a las posibilidades económicas de sus padres.

Piensa esta parte que este gasto obedece más a un capricho de la actora que a una necesidad real, y que otros colegios, por un coste inferior, imparten una enseñanza de calidad equiparable a aquel al que asiste la menor.

QUINTO.- Consecuencia de todo lo anterior es que esta parte entiende que procede fijar una pensión de alimentos a cargo del demandado de [IMPORTE] euros, cantidad acorde al nivel de ingresos de ambos progenitores, y que responde a la realidad económica de mi representado.

FUNDAMENTOS DE DERECHO

Conforme con los fundamentos jurídicos I a VI del escrito de demanda sobre capacidad, representación, legitimación, jurisdicción, competencia, procedimiento e intervención del Ministerio Fiscal.

VII.- Fondo del asunto.

Son de aplicación los artículos 142 y siguientes del Código Civil, en relación con el 158.1 del mismo texto legal.

VIII.- Costas.

Deberán ser impuestas a la contraparte las costas en virtud de lo establecido en el artículo 394 de la LEC.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL,

que teniendo por presentado este escrito, con sus documentos y copias de todo ello, se sirva admitirlo, y tener por formulada en tiempo y forma CONTESTACIÓN A LA DEMANDA DE ALIMENTOS para el menor [NOMBRE DEL MENOR], interpuesta por Dña. [NOMBRE Y APELLIDOS] frente a D. [NOMBRE Y APELLIDOS]; y tras los trámites de rigor, previa la intervención del Ministerio Fiscal, se dicte Sentencia, en la que, estimándose los argumentos de esta parte, se acuerde la fijación de una pensión alimenticia a cargo de mi patrocinado de [IMPORTE] euros, con expresa imposición de costas a la parte contraria.

Es de Justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
