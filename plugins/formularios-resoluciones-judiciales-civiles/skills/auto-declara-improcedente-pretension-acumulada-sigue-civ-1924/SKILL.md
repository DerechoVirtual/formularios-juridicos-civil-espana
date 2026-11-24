---
name: auto-declara-improcedente-pretension-acumulada-sigue-civ-1924
description: "Auto que declara improcedente la pretensión acumulada y sigue el proceso respecto de la otra. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que declara improcedente la pretensión acumulada y sigue el proceso respecto de la otra

> Formulario **CIV-1924** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto dictado tras la audiencia previa, declarando improcedente la acción de cumplimiento contractual que pretendía ejercitarse acumulada a la acción de resolución contractual. Documento adapatado a la reforma orgánica de la LO 1/2025.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que declara improcedente la pretensión acumulada y sigue el proceso respecto de la otra» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que declara improcedente la pretensión acumulada y sigue el proceso respecto de la otra” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-declara-improcedente-pretension-acumulada-sigue-civ-1924`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] CALLE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] GRUPO
- [ ] LUGAR
- [ ] MANIFESTACIÓN DE LA PARTE
- [ ] NOMBRE DE LA PARTE
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 71 LEC
- art. 416.1.5.ª LEC
- art. 419 LEC
- art. 71.3 LEC
- art. 399 LEC
- art. 71.2 LEC

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

Auto dictado tras la audiencia previa, declarando improcedente la acción de cumplimiento contractual que pretendía ejercitarse acumulada a la acción de resolución contractual.

Documento adapatado a la reforma orgánica de la LO 1/2025.


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

AUTO

Ilmo. Sr./a Magistrado-Juez D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

HECHOS

PRIMERO

En este Tribunal se sigue procedimiento de juicio ordinario interpuesto por [ÓRGANO O PERSONA], frente a la Comunidad de Propietarios del n.º [NÚMERO] de la calle [CALLE] de [LOCALIDAD].

SEGUNDO

En su escrito de contestación a la demanda la parte demandada ha alegado la improcedencia de la acumulación de acciones pretendida por la actora, por entender que no cabe por incompatibilidad.

TERCERO

Celebrada la audiencia previa al juicio del pasado día [FECHA] por la mercantil actora se manifestó que [MANIFESTACIÓN DE LA PARTE]

RAZONAMIENTOS JURÍDICOS

PRIMERO

Establece el art. 71 LEC requisitos para la acumulación de acciones, y el art. 416.1.5.ª LEC que en el acto de la audiencia previa, descartado el acuerdo entre las partes, el Tribunal resolverá, del modo previsto en los artículos siguientes, sobre cualesquiera circunstancias que puedan impedir la válida persecución y término del proceso mediante sentencia sobre el fondo, y en especial sobre el defecto legal en el modo de proponer la demanda o la falta de claridad o precisión en la determinación de la petición que se deduzca.

Señala el art. 419 LEC que si en la demanda se hubiesen acumulado diversas acciones y el demandado en su contestación se hubiera opuesto motivadamente a esta acumulación, el tribunal, oyendo previamente al actor en la misma audiencia, resolverá oralmente sobre la procedencia y admisibilidad de la acumulación, siguiendo la audiencia y el proceso su curso respecto de la acción o acciones que según la resolución judicial puedan constituir el objeto del proceso.

SEGUNDO

La sociedad demandada ejerce acción de cumplimiento de contrato de mantenimiento de aparatos ascensores, al reclamar las mensualidades del precio periódico desde [FECHA] hasta la presentación de la demanda, y al propio tiempo, la resolutoria, dado que se considera la resolución unilateral por la Comunidad demandada incumplimiento, pero se postula el resarcimiento de daños y perjuicios -lucro cesante- asumiendo la resolución, que calcula en un porcentaje de cuotas pendientes por cobrar, incluidas las devengadas que se reclaman.

Es evidente que no se ejercitan dichas acciones de manera eventual, es decir, no se condiciona la pretensión subsidiaria a que se desestime la principal, por lo que se ejercen simultáneamente acciones que se excluyen entre sí, de suerte que la elección de una impida o haga ineficaz el ejercicio de la otra, en términos del art. 71.3 LEC. Inadmisible, además, por falta de concreción en ‘petitum’ (art. 399 LEC en relación con el art. 416.1.5.ª LEC), ya que, al no extenderse la petición al conjunto de los objetos, sino al de uno u otro, y poder existir dos fundamentaciones alternativas, que resultan incompatibles (con prohibición de lo dispuesto en el art. 71.2 LEC), la representación de la parte demandada no puede saber a ciencia cierta cuál de las dos pretensiones, la de resolución o la de cumplimiento, ha de ser objeto de contestación, con lo que se le genera la indefensión proscrita constitucionalmente.

TERCERO

A la vista de las alegaciones formuladas por la demandada y las aclaraciones respecto a la verdadera pretensión ejercitada, efectuadas por la actora en el acto de la comparecencia, y que expresó que se ejercita la resolución de contrato con indemnización de daños y perjuicios, procede decretar esta acción para seguir el curso del proceso.

PARTE DISPOSITIVA

Se declara improcedente la acción de cumplimiento contractual que pretendía ejercitar, acumulada a la acción de resolución contractual [NOMBRE DE LA PARTE], representada por el Procurador/a de los Tribunales Sr./a [NOMBRE Y APELLIDOS], y acuerdo de prosecución del juicio en ejercicio de la acción de resolución contractual, única pretensión objeto de litigio frente a la COMUNIDAD DE PROPIETARIOS DEL N.º [NÚMERO] DE LA CALLE [CALLE] DE [LOCALIDAD].

Así lo acuerdo, mando y firmo:

Firma del Juez/a

Contra la presente resolución cabe interponer, en el plazo de cinco días, recurso de reposición (arts. 452 y ss. LEC) ante el mismo Tribunal.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

========================================================================
