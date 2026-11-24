---
name: escrito-ampliacion-objetiva-demanda-civ-0860
description: "Escrito de ampliación objetiva de la demanda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de ampliación objetiva de la demanda

> Formulario **CIV-0860** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito dirigido al Tribunal de Instancia solicitando la ampliación objetiva de la demanda inicialmente formulada.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de ampliación objetiva de la demanda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de ampliación objetiva de la demanda” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-ampliacion-objetiva-demanda-civ-0860`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] TIPO DE ACCIÓN (3 veces)
- [ ] AÑO (2 veces)
- [ ] CONCEPTO
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] OBJETO DE LA RECLAMACIÓN
- [ ] PETICIÓN
- [ ] SEDE
- [ ] TIPO DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 401 LEC
- art. 73 LEC
- art. 399 LEC

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

- Junto a «…O]/[AÑO]. A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Juicio [TIPO DE PROCEDIMIENTO] n.º [Nº DE PROCEDIMIENTO]/[AÑO].

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], según tengo acreditado en los autos referenciados, ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que mediante el presente escrito, y en la representación que acredito, amplio la demanda de juicio ordinario en el ejercicio de la acción de [TIPO DE ACCIÓN] deducida por esta parte contra D./Dña. [NOMBRE Y APELLIDOS], con objeto de que se tenga también por ejercitada contra dicho demandado, ya circunstanciado en autos, la acción en reclamación de [OBJETO DE LA RECLAMACIÓN], teniendo por ampliada la demanda principal, para que en su día se dicte sentencia de conformidad con el suplico de este escrito de ampliación de demanda que baso en los siguientes

HECHOS

(Reproducir los de la demanda y añadir a los que sustenten la ampliación con determinación de las circunstancias de nuevo conocimiento que han motivado la ampliación de la demanda).

El demandado D./Dña. [NOMBRE Y APELLIDOS], no ha contestado aún a la demanda que ha dado origen a los presentes autos.

A los hechos antecedentes resultan de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

Legitimación

Procedimiento

En atención a la ampliación formulada la cuantía del juicio pasaría a ser la de [IMPORTE] euros por [CONCEPTO].

1) AMPLIACIÓN DE DEMANDA: El art. 401 de la LEC establece que “antes de la contestación podrá ampliarse la demanda para acumular nuevas acciones a las ya ejercitadas o para dirigirlas contra nuevos demandados”.

Art. 71 de la LEC: Establece que el actor podrá acumular en la demanda cuantas acciones le competan contra el demandado, aunque provengan de diferentes títulos, siempre que aquellas no sean incompatibles entre sí.

Art. 72 de la LEC: Podrán acumularse, ejercitándose simultáneamente, las acciones que uno tenga contra varios sujetos o varios contra uno, siempre que entre esas acciones exista un nexo por razón del título o causa de pedir.

2) Por su parte el art. 73 de la LEC determina los requisitos para la admisibilidad de la acumulación:

“1.º Que el Tribunal que deba entender de la acción principal posea jurisdicción y competencia por razón de la materia o por razón de la cuantía para conocer de la acumulada o acumuladas. Sin embargo, a la acción que haya de sustanciarse en juicio ordinario podrá acumularse la acción que, por sí sola, se habría de ventilar, por razón de su cuantía, en juicio verbal.

2.º Que las acciones acumuladas no deban, por razón de su materia, ventilarse en juicios de diferente tipo.

3.º Que la ley no prohíba la acumulación en los casos en que se ejerciten determinadas acciones en razón de su materia o por razón de algún tipo de juicio que se haya de seguir.”

Analizando las acciones acumuladas en la demanda se llega a la conclusión de que su ejercicio conjunto no vulnera ninguno de los límites antedichos.

Art. 401.2 de la LEC: ampliada la demanda, “el plazo para contestar a la demanda se volverá a contar desde el traslado de la ampliación de la demanda”.

3) (En su caso) Acompañamos modelo 696 de liquidación de la tasa judicial de esta ampliación.

Fondo

(desarrollar fundamentos de derecho aplicables a los hechos que sirven de base a la acción ejercitada).

Costas

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito, se sirva admitirlo, teniendo por ampliada la demanda de juicio ordinario en ejercicio de la acción de [TIPO DE ACCIÓN] dirigida contra D./Dña. [NOMBRE Y APELLIDOS], acordando admitir a trámite la presente ampliación de demanda y teniendo por ejercitada también contra dicho demandado la acción de [TIPO DE ACCIÓN] dándole traslado de este escrito de ampliación para que la conteste en plazo legal, y dando a los autos el impulso procedimental pertinente en su día se dicte sentencia por la que se condene al demandado D./Dña. [NOMBRE Y APELLIDOS] a [PETICIÓN] (detallar las peticiones reproduciendo las de la demanda y las nuevas que correspondan a la ampliación, expresándolas con la debida separación que exige el art. 399 5 de la LEC), con expresa imposición de las costas del juicio al demandado.

Es justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].
