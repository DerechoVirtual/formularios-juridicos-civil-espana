---
name: diligencia-ordenacion-convoca-audiencia-sobre-division-civ-2126
description: "Diligencia de ordenación que convoca a audiencia sobre la división tras disolverse los gananciales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Diligencia de ordenación que convoca a audiencia sobre la división tras disolverse los gananciales

> Formulario **CIV-2126** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DILIGENCIA DE ORDENACIÓN SR. LETRADO DE LA ADMINISTRACIÓN DE JUSTICIA Firmas Diligencia de ordenación convocando a los cónyuges a comparecencia para ser oídos sobre la división del patrimonio conyugal y formándose pieza separada para la adecuada tramitación de todo lo relacionado con la disolución y liquidación de la sociedad de gananciales.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Diligencia de ordenación que convoca a audiencia sobre la división tras disolverse los gananciales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Diligencia de ordenación que convoca a audiencia sobre la división tras disolverse los gananciales” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:diligencia-ordenacion-convoca-audiencia-sobre-division-civ-2126`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] FECHA (3 veces)
- [ ] LUGAR (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] GRUPO
- [ ] NÚMERO

## Normas que cita el formulario

- art. 541.3 LEC

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
(1) El objeto de la audiencia de los cónyuges, a la que parece que debe convocarse al acreedor -que tiene derecho a participar en las divisiones patrimoniales afectantes a su deudor-, no está definido, y, en interpretación favorable a la acción ejecutiva, pudiera concedérsele un arbitrio al ejecutor para depurar situaciones de irresponsabilidad técnica, pero en que se contempla una utilización del gasto en beneficio familiar, o una estrategia de composición de masas patrimoniales, gananciales y privativas, para eludir la agresión del acreedor, puesto que la facultad disolutoria está pensada para proteger a un cónyuge frente a la errada gestión patrimonial del otro, y no para burlar acreedores. En todo caso, en defecto de acuerdo de liquidación que pueda aprobarse, se deja entrada a las reglas de los arts. 807 y ss. LEC (Capítulo II del Título II del Libro IV), habiéndose de fijar judicialmente un plazo máximo para llevar a cabo la liquidación y, una vez efectuada, se sustituirá el embargo por el de determinados bienes adjudicados al cónyuge ejecutado.

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

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA

Procedimiento: Ejecución de Título Judicial n.º [Nº]/[AÑO]

Número de Identificación Informática:

Partes:

DILIGENCIA DE ORDENACIÓN SR. LETRADO DE LA ADMINISTRACIÓN DE JUSTICIA [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

Dada cuenta, y

1.- Habiendo ejercitado Doña [NOMBRE Y APELLIDOS], representada por el Procurador/a. Sr./a. [NOMBRE Y APELLIDOS], la opción por la disolución de la sociedad de gananciales con el ejecutado Don [NOMBRE Y APELLIDOS], a fin de que se sustituya el embargo de bienes comunes por el de la parte que corresponda en los mismos al ejecutado, de conformidad con lo dispuesto en el art. 541.3 LEC, cítese a los indicados cónyuges, y a la mercantil acreedora CLÍNICA [DENOMINACIÓN SOCIAL] S.L. (arts. 1.082 y 1.083 CCiv en relación con arts. 1.401, 1.402 y 1.410 CCiv), a comparecencia para ser oídos sobre la división del patrimonio conyugal, a cuyo acto deberán acudir personalmente o representados por Procurador con poder especial para renunciar, transigir, allanarse, o apartarse con sobreseimiento del asunto.

Se señala para celebrar la comparecencia el día [FECHA], a las [Nº] horas, en la Sala de Vistas del Tribunal.

2.- Fórmese pieza separada para la adecuada tramitación de todo lo relacionado con la disolución y liquidación de la sociedad de gananciales.

3.-Quede en suspenso el proceso de ejecución en cuanto a los bienes comunes.

Contra esta resolución cabe interponer recurso de reposición, mediante escrito ante el LAJ que se presenta dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, y sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita

Así lo acuerdo y firmo,

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma del Letrado/a de la Administración de Justicia:
