---
name: contestacion-demanda-divorcio-pide-modificar-medidas-civ-0074
description: "Contestación a la demanda de divorcio que pide modificar las medidas fijadas en la separación previa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda de divorcio que pide modificar las medidas fijadas en la separación previa

> Formulario **CIV-0074** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda de divorcio que pide modificar las medidas fijadas en la separación previa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda de divorcio que pide modificar las medidas fijadas en la separación previa” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-demanda-divorcio-pide-modificar-medidas-civ-0074`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] DÍA
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

- Junto a «…FANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚM DE [LOCALIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚM DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello, comparezco en este TRIBUNL con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, me persono en los autos de juicio de divorcio núm. [Nº DE PROCEDIMIENTO]/[AÑO], instados por D./Dª [NOMBRE Y APELLIDOS], tras habérseme dado traslado de la demanda conforme a lo dispuesto en el art. 753 de la Ley de Enjuiciamiento Civil, y formulo CONTESTACIÓN A LA DEMANDA, con base en los siguientes

HECHOS

De acuerdo con el correlativo de la demanda, en relación con los datos de celebración del matrimonio.

De acuerdo con el correlativo de la demanda, en relación con los datos del hijo común.

De acuerdo con el correlativo de la demanda, en relación con la existencia de sentencia de separación previa dictada en procedimiento seguido de mutuo acuerdo, en el que se homologó el correspondiente convenio regulador.

Nada tiene que oponer mi representado/a a la pretensión de divorcio del/de la actor/a.

En relación con las medidas definitivas acordadas por los esposos en el convenio regulador de su separación matrimonial y homologadas por el Tribunal en el procedimiento de separación a que se ha hecho referencia en el HECHO TERCERO, mi representado/a, considera que deben mantenerse, en su totalidad, en la sentencia de divorcio que se dicte en el presente procedimiento.

A diferencia de lo que sostiene el demandante en el HECHO QUINTO de su demanda, no resulta conveniente para el menor la sustitución del actual régimen de guarda y custodia individual por otro de guarda y custodia compartida, y esto debido a las siguientes razones:

Es cierto que cuando se dictó la sentencia de separación, el domicilio del/de la demandante se encontraba en una ciudad distinta al de mi representado/a y que en la actualidad se ha trasladado a la misma ciudad y zona. Pero ello nada tiene que ver con el deseo de tener mayor relación con su hijo sino con el inicio de una convivencia como pareja de hecho con D./Dª [NOMBRE Y APELLIDOS], al que ambos cónyuges habían tratado como vecino/a durante años y a cuyo domicilio se ha trasladado el/la demandante.

Por otra parte, a pesar de que el domicilio actual del/de la actor/a se encuentra próximo al de mi representado/a, lo cierto es que debido a su profesión - viajante de comercio - aquél pasa largas temporadas (varias semanas enteras cada mes) fuera de su hogar, lo que le impediría atender a su hijo debidamente bajo un régimen de custodia compartida.

En cuanto a los deseos del menor, el mismo ha sido influenciado por su padre/madre, que continuamente intenta predisponerlo en contra de mi representado/a y trata de ganarse su voluntad con regalos caros y actitudes permisivas contraproducentes para el desarrollo personal y maduración del menor, tal y como se demostrará en el período probatorio.

Finalmente, la solicitud de guarda y custodia compartida por parte del/de la actor/a obedece a su deseo de venganza en relación con mi representado/a al haber tenido noticia de que éste/a le fue infiel durante su matrimonio, lo que se demostrará en período de prueba. Es, por tanto, ajena al interés del menor.

En consecuencia con lo anterior, debe mantenerse la obligación del actor de satisfacer la pensión de alimentos prevista en la sentencia de separación, en iguales términos, ya que no se ha producido desde entonces una alteración sustancial de las circunstancias que se tuvieron en cuenta para fijarla.

A los anteriores hechos les son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

COMPETENCIA, PROCEDIMIENTO, LEGITIMACIÓN Y POSTULACIÓN PROCESAL.-

Conformes con la competencia objetiva y territorial del Tribunal, la legitimación de las partes, y el procedimiento, compareciendo esta parte con la debida representación técnica y asistencia letrada.

DERECHO SUSTANTIVO

Dado que el vigente art. 86 del Código civil, no requiere causa alguna de divorcio, bastando para poder solicitarlo y que sea decretado por el Juez el transcurso de tres meses desde el matrimonio, nada hay que oponer a este extremo.

En cambio, en cuanto a las medidas definitivas que propone el/la demandante, mi representado/a manifiesta su disconformidad con aquellas que suponen una modificación de las adoptadas, en su día, en la sentencia de separación y que se refieren a la guarda y custodia del hijo menor y, en relación con ésta, a la pensión de alimentos que viene obligado a satisfacer el/la demandante.

El art. 92.8 del Código civil dispone que, excepcionalmente, aun cuando no haya acuerdo entre los progenitores, "el Juez, a instancia de una de las partes, con informe (anteriormente la norma hacía referencia al informe "favorable" del Ministerio Fiscal, sin embargo, el término entrecomillado ha sido declarado inconstitucional y nulo por Sentencia 185/2012, de 17 de octubre, del Pleno del Tribunal Constitucional -BOE núm. 274, de 14 de noviembre de 2012-)del Ministerio Fiscal, podrá acordar la guarda y custodia compartida, fundamentándola en que de esta forma se protege adecuadamente el interés superior del menor". Ahora bien, tal y como queda de manifiesto a la vista de los hechos expuestos en este escrito de contestación, no resulta de interés para el hijo menor el acogimiento de una custodia compartida, por lo que debe desestimarse tal pretensión y, con ella, la de modificar el régimen de los alimentos, manteniéndose las medidas definitivas establecidas en la sentencia de separación.

COSTAS.- Deben ser impuestas al/ a la demandante, de acuerdo con el art. 394 de la Ley de Enjuiciamiento civil.

Por lo expuesto:

SUPLICO AL TRIBUNAL

Que tras admitir este escrito con los documentos que lo acompañan, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta en tiempo y forma CONTESTACIÓN A LA DEMANDA CONTENCIOSA DE DIVORCIO y, previos los trámites procesales oportunos, dicte en su día sentencia por la que se declare el divorcio y, desestimando la demanda en relación con las medidas definitivas cuya modificación se pretende, dicte sentencia por la que se absuelva a la demandada de las pretensiones ejercitadas de contrario, y se confirmen las medidas definitivas aprobadas en la sentencia previa de divorcio, con expresa condena en costas de la parte actora.

En virtud de lo expuesto,

En [LOCALIDAD], a [DÍA], de [MES], de [AÑO]

Firma y número del Letrado

Firma del Procurador

========================================================================
