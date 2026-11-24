---
name: acta-inicio-procedimiento-mediacion-familiar-civ-0003
description: "Acta de inicio de un procedimiento de mediación familiar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de inicio de un procedimiento de mediación familiar

> Formulario **CIV-0003** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de inicio de un procedimiento de mediación familiar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de inicio de un procedimiento de mediación familiar” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:acta-inicio-procedimiento-mediacion-familiar-civ-0003`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº (4 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LUGAR (2 veces)
- [ ] MES (2 veces)
- [ ] LOCALIDAD
- [ ] NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN

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

ACTA INICIAL DE LA MEDIACIÓN

En [LUGAR], a [DÍA] de [MES] de [AÑO].

D. [NOMBRE Y APELLIDOS], mediador de la institución [NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN], con el numero, [Nº]

MANIFIESTA

Que la citada comparecencia lo ha sido a efectos de ser informados de la mediación familiar que pueden iniciar para resolver las controversias derivadas del cese de la convivencia conyugal, tanto en el aspecto económico como en las relaciones paterno filiales, habiendo sido informados sobre sus derechos y deberes, principios rectores de la mediación, de las características del procedimiento, de su duración y de los honorarios profesionales.

Que, a la vista de la información recibida, manifiestan que tienen la intención de resolver el conflicto por vía extrajudicial y aceptan desarrollar la mediación para la resolución del conflicto planteado en el proceso antes expresado dentro de los siguientes

Términos

Designación de mediador

Ambas partes de común acuerdo designan como mediador a quien suscribe D. [NOMBRE Y APELLIDOS], cuyas circunstancias constan en el encabezamiento.

Objeto del conflicto que se somete a mediación

Que el conflicto que se somete a mediación es el derivado del cese de la convivencia conyugal de ambas partes a fin de regular lo procedente sobre los efectos personales y patrimoniales derivados de la disolución de su matrimonio que tienen intención de instar judicialmente y en especial:

- Ejercicio de la patria potestad y régimen de guarda y visitas de los hijos comunes [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS], de [Nº] y [Nº] años de edad respectivamente.

- Pensión económica que debe satisfacerse en su caso en concepto de alimentos y educación de los hijos comunes.

- Atribución del domicilio familiar.

- Aspectos patrimoniales derivados de la disolución del matrimonio y de la liquidación del régimen de gananciales.

Programa de actuaciones y duración máxima del procedimiento

El programa de actuaciones comprenderá las sesiones de mediación que pudieran ser necesarias (individuales y/o conjuntas) a criterio del mediador, en atención al principio de flexibilidad y al principio de igualdad.

Las partes acuerdan que el plazo de duración máxima del procedimiento de mediación será de [Nº] meses a contar desde la firma del presente documento

Coste de la mediación

El coste de la mediación se dividirá por igual entre las partes firmantes, y se abonará a la finalización del procedimiento.

El coste de la mediación incluirá los honorarios del mediador a razón de [IMPORTE] euros por sesión, con una cifra máxima de [IMPORTE] euros.

Aceptación y asunción de obligaciones

Las partes declaran haber sido informadas acerca de las características básicas de la mediación, Y manifiestan su voluntad de participar en la mediación y asumir las obligaciones que de ella se deriven, observando el deber de confidencialidad en relación a cualquier documento o manifestación que se realice en el procedimiento, salvo el acuerdo total o parcial que pudiera alcanzarse, y tanto las partes, como el mediador se comprometen a aceptar y cumplir estos principios básicos.

Lugar de celebración y lengua del procedimiento

Que ambas partes convienen que la mediación se desarrolle en [LOCALIDAD] y que el idioma en el que se sustanciará el procedimiento será el castellano.

Y para que así conste, se extiende esta acta con un ejemplar para cada una de las partes, a uno solo efecto, al lugar y fecha indicados.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

========================================================================
