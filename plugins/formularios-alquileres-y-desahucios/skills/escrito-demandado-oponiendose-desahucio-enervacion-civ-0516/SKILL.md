---
name: escrito-demandado-oponiendose-desahucio-enervacion-civ-0516
description: "Escrito del demandado oponiéndose al desahucio por enervación de la acción. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del demandado oponiéndose al desahucio por enervación de la acción

> Formulario **CIV-0516** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del demandado oponiéndose al desahucio por enervación de la acción» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del demandado oponiéndose al desahucio por enervación de la acción” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:escrito-demandado-oponiendose-desahucio-enervacion-civ-0516`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] MES (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FECHA
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 438.5 LEC
- art. 22.4 LEC

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

- Junto a «…al de desahucio núm. [Nº] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Juicio verbal de desahucio núm. [Nº]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de Don [NOMBRE Y APELLIDOS] con domicilio en [LOCALIDAD], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, ante el Tribunal comparezco y DIGO:

1) Que mi representado ha sido demandado en el juicio de desahucio arriba indicado, por falta de pago de las rentas desde el mes de [MES], cantidad que asciende a [IMPORTE] euros, habiendo recibido requerimiento el día [FECHA] en el que se indica que no procede la enervación.

2) Que dándose las circunstancias para que proceda la enervación, por medio del presente escrito, dentro del plazo establecido en el artículo 438.5 de la LEC, me opongo a la pretensión deducida de contrario en base a los siguientes:

HECHOS Y FUNDAMENTOS

En la demanda se indica la improcedencia de la enervación con fundamento en que se requirió previamente a mi representado para el pago de las rentas.

Sin embargo, el requerimiento practicado en modo alguno puede considerarse válido, puesto carece de la condición de fehaciente exigida por el artículo 22.4 de la LEC, al haberse remitido una carta certificada al domicilio de la vivienda arrendada sin ninguna constancia cierta de su verdadero contenido y sin que fuera recibida por mi representado, quien en ningún momento tuvo conocimiento del requerimiento de pago.

En la demanda se indica que no procede la enervación por haberse producido una enervación anterior.

Esta parte se opone a dicha pretensión, por cuanto la enervación anterior se produjo por causas imputables al arrendador, quien incluyó en los recibos que giraba a mi representado unos incrementos de renta por obras de conservación que en modo alguno estaban pactados y que fueron excluidos de las rentas reclamadas en el juicio verbal de desahucio número [NÚMERO] seguido ante el Tribunal de Instancia número [NÚMERO] (acompaño como documento [Nº DE DOCUMENTO] testimonio de la sentencia dictada en dicho juicio de desahucio).

Por tanto, concurre la excepción prevenida en el último párrafo del artículo 22.4 de la LEC que impide el cómputo de la anterior enervación por ser imputable exclusivamente al arrendador las diferencias que se produjeron en el pago de la renta.

Por tanto, se interesa que, teniendo por formulada esta oposición, se convoque a las partes a la vista conforme a lo dispuesto en el artículo 438.5 de la LEC a fin de dirimir la procedencia de la enervación que pretende realizar esta parte, a cuyo efecto acompaña a este escrito el resguardo de consignación de las cantidades reclamadas, conforme se expresa en el otrosí.

Por todo ello,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito, con su copia y documentos que lo acompañan, que lo admita acordando su unión a los autos de su razón, y que me tenga por personado y parte en la representación que ostento de Don [NOMBRE Y APELLIDOS]; teniendo por formulada oposición a la pretensión de desahucio por concurrir las circunstancias de la enervación, citando a las partes a la vista de juicio verbal y, tras su celebración, dictando resolución declarando enervada la acción con imposición de costas al actor.

OTROSÍ DIGO que, de conformidad a lo dispuesto en el artículo 22.4 de la LEC, acompaño a a este escrito resguardo que acredita el ingreso de las cantidades reclamadas en la demanda y de las adeudadas hasta el momento del pago en la cuenta de consignaciones de este Tribunal, a fin de que se declare enervada la acción de desahucio.

Por lo que,

SUPLICO AL TRIBUNAL tenga por consignada la cantidad citada y se ponga a disposición de la actora, así como que tras los trámites oportunos se dicte resolución que declare enervada la acción de desahucio y terminado el proceso, conforme a lo solicitado en este escrito.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado y Procurador

========================================================================
