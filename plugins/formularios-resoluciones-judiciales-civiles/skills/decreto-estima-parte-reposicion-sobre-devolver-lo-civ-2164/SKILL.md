---
name: decreto-estima-parte-reposicion-sobre-devolver-lo-civ-2164
description: "Decreto que estima en parte la reposición sobre devolver lo cobrado en ejecución provisional. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Decreto que estima en parte la reposición sobre devolver lo cobrado en ejecución provisional

> Formulario **CIV-2164** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Decreto estimando en parte el recurso de reposición declarando haber lugar a reponer el auto que acordó el sobreseimiento de la ejecución provisional, en el sentido de dejar en suspenso el requerimiento de devolución de las cantidades percibidas de la ejecutada y la práctica de tasación de costas causadas a ésta que no sean de la ejecución provisional, hasta que se acredite notificada la resolución de la Audiencia provincial sobre la preparación de recurso de casación contra su sentencia revocatoria.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Decreto que estima en parte la reposición sobre devolver lo cobrado en ejecución provisional» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Decreto que estima en parte la reposición sobre devolver lo cobrado en ejecución provisional” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:decreto-estima-parte-reposicion-sobre-devolver-lo-civ-2164`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] FECHA (5 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] AÑO
- [ ] LOCALIDAD
- [ ] NÚMERO

## Normas que cita el formulario

- art. 533.1 LEC
- art. 535.1 LEC
- art. 533 LEC
- art. 528.3 LEC
- art. 241.2 LEC

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

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [NÚMERO]

PROCEDIMIENTO

Número de identificación informático:

PARTES:

DECRETO DEL LETRADO DE LA ADMINISTRACIÓN DE JUSTICIA

Sr./a Letrado/a de la Administración de Justicia [NOMBRE Y APELLIDOS]

En la Villa de [LOCALIDAD], a [FECHA]

ANTECEDENTES DE HECHO

I.- La compañía de seguros RR SEGUROS Y REASEGUROS [DENOMINACIÓN SOCIAL], S.A., representada por el Procurador/a. Sr./a [NOMBRE Y APELLIDOS], pidió el [FECHA] que se sobreseyera la ejecución provisional, con requerimiento de devolución de cantidad, solicitud de tasación de costas de la instancia, y resarcimiento de daños y perjuicios, todo ello por revocación de condena dineraria en vía de apelación.

II.- En decreto de [FECHA] se acordó el sobreseimiento de la ejecución provisional, el requerimiento de devolución, el traslado de la relación de daños y perjuicios, y se ordenó la tasación de costas.

III.- La ejecutante provisional D./Dña. [NOMBRE Y APELLIDOS], representada por el/la Procurador/a Sr./a. [NOMBRE Y APELLIDOS], interpuso recurso de reposición frente al anterior decreto, que se trasladó a las demás partes en diligencia de ordenación de [FECHA] de [AÑO], produciendo escrito de impugnación RR SEGUROS Y REASEGUROS [DENOMINACIÓN SOCIAL], S.A.

RAZONAMIENTOS JURÍDICOS

PRIMERO.- La recurrente, que hasta el momento del auto que combate era ejecutante provisionalmente, discute que se haya accedido a las peticiones de apremio de la parte adversa, porque la sentencia revocatoria de la de instancia no ha sido notificada a todas las partes, y pende preparación de recurso de casación contra aquélla.

La acreditación, mediante certificación de la Secretaría de la Sección de una sentencia de apelación de la Audiencia Provincial íntegramente revocatoria de la condena pecuniaria que se ejecutaba provisionalmente, impone un sobreseimiento de la ejecución provisional conforme al art. 533.1 LEC, con independencia de que no se hayan efectuado aún todas las notificaciones, al igual que cabría la ejecución provisional de la sentencia de apelación, si hubiera sido la primera condena, desde la notificación en que se tuviera por interpuesto el recurso de casación o extraordinario por infracción procesal, sin atender a que se hubieran producido aún todas las notificaciones (art. 535.1 LEC).

No parece que pueda existir un auténtico sobreseimiento provisional de la ejecución provisional, porque si la eventual sentencia del recurso extraordinario revoca la de segunda instancia y confirma la de primera instancia que en su día se ejecutó provisionalmente, lo que procederá ya no es reabrir la ejecución provisional sino una ejecución definitiva.

SEGUNDO.- No se considera, pues, que deba esperarse siempre a la llegada de los autos de la Audiencia, a condición de que el interesado presente testimonios suficientes para actuar en la pieza separada, hasta que ésta se pueda unir a los autos principales.

Pero en este caso la sentencia revocatoria puede no ser firme, como en el recurso de reposición se pone en conocimiento del Juez ejecutor que se ha presentado escrito de preparación del recurso de casación por la representación de D./Dña. [NOMBRE Y APELLIDOS].

Con demostrarse tal cosa, lo procedente es mantener el sobreseimiento de la ejecución provisional, pero suspender el acuerdo sobre devolución de cantidades, dado que no se sabe si la Audiencia tendrá por preparado el recurso de casación, y sólo entonces, se conocerá aplicable el apartado 1 ó 3 del art. 533 LEC.

Porque, si la sentencia revocatoria es firme, dará paso al requerimiento de devolución, resarcimiento de daños y perjuicios por la ejecución provisional, y reintegro de las costas de la ejecutada, tanto de la ejecución provisional, como de las del declarativo principal (éste último pronunciamiento de la sentencia de la Audiencia).

Pero si la sentencia revocatoria se prepara válidamente para recurrir en casación, se tratará de una devolución, reintegro e indemnización que tiene la singularidad de que quien era ejecutante, luego obligado a devolver, puede oponerse a las actuaciones concretas del apremio, con arreglo al art. 528.3 LEC, cauce que es estrechísimo, pero que de todas formas habrá de enterarse que lo tiene a su disposición.

TERCERO.- En cuanto a la liquidación del resarcimiento no tiene sentido suspender la orden judicial, ya que en cualquier caso procederá declararlos y cuantificarlos y, por de pronto, el Tribunal entiende se habrán de incluir los intereses legales de las cantidades ejecutadas hasta que se devuelvan.

En cuanto a la tasación de costas, lo que corresponde es ceñirla a las de la ejecución provisional, dado que las del declarativo no se considera deban tasarse hasta que conste la firmeza. Aunque el art. 533.1 LEC se refiere a las costas de la ejecución provisional que el ejecutado hubiese satisfecho, no se trata de las reembolsadas al ejecutante (que sería cantidades percibidas a devolver), sino de las irrogadas y que haya satisfecho hasta el momento conforme al art. 241.2 LEC, por lo que no existe pluspetición.

CUARTO.- Tanto la estimación parcial, como las dificultades interpretativas de una norma procesal novedosa y la equivocación de ambos contendientes, en su precipitación por desarbolar al contrario, justifican no pronunciarse en costas de este recurso.

En razón a lo expuesto,

PARTE DISPOSITIVA

Estimando en parte el recurso de reposición interpuesto por el/la Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], en representación de D./Dña. [NOMBRE Y APELLIDOS], frente al decreto de [FECHA], declaro haber lugar a reponerlo, en el sentido de dejar en suspenso el requerimiento de devolución de las cantidades percibidas de la ejecutada y la práctica de tasación de costas causadas a ésta que no sean de la ejecución provisional, hasta que se acredite notificada la resolución de la Secciónde la Audiencia Provincial sobre la preparación de recurso de casación contra su sentencia revocatoria.

Así lo acuerdo y firmo:

Firma del Letrado/a de la Administración de Justicia:

Contra este decreto no cabe recurso alguno.

========================================================================
