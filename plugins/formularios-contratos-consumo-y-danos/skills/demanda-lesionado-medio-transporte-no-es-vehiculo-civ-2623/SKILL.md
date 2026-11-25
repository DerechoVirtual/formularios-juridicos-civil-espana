---
name: demanda-lesionado-medio-transporte-no-es-vehiculo-civ-2623
description: "Demanda del lesionado en un medio de transporte que no es vehículo a motor contra el transportista. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda del lesionado en un medio de transporte que no es vehículo a motor contra el transportista

> Formulario **CIV-2623** del plugin **Contratos civiles y consumo** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 25-11-2026.

## Qué es

Escrito de demanda de juicio ordinario interpuesta por aquel que resultó lesionado en un medio de transporte que no tiene la consideración de vehículo a motor (ferrocarril, tranvía, telesilla...), en reclamación de una indemnización de daños y perjuicios al haber incurrido el transportista en responsabilidad civil.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda del lesionado en un medio de transporte que no es vehículo a motor contra el transportista» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda del lesionado en un medio de transporte que no es vehículo a motor contra el transportista” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-lesionado-medio-transporte-no-es-vehiculo-civ-2623`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles y consumo) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR (21 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] ASEGURADORA (4 veces)
- [ ] Nº (4 veces)
- [ ] FECHA (3 veces)
- [ ] MATRÍCULA (2 veces)
- [ ] FECHAS
- [ ] LUGAR
- [ ] Nº DE COLEGIADO
- [ ] NÚMERO
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 1258 CC
- art. 1902 CC
- art. 10 LEC
- art. 76 LCS
- art. 52.3 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1968.2.º CC
- art. 1964.2 CC
- art. 20 LCS
- art. 155 LEC
- art. 339 LEC

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: La legitimación pasiva de la aseguradora alude a la «responsabilidad civil del vehículo matrícula (MATRÍCULA)»; en transporte ferroviario o similar debe identificarse la póliza de responsabilidad civil del transportista.
- Junto a «…imilar debe identificarse la póliza de responsabilidad civil del transportista.]»: Se mantiene la nota sobre Sección Civil o Sección Única: depende del partido judicial.
- Junto a «…de del partido judicial.] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Si las lesiones se produjeran con motivo de la circulación en un medio de transporte público que tuviera la consideración de vehículo a motor (verbigracia, autocar).

El art. 21 de la Ley 16/1987 de 30 de julio, de Ordenación de los Transportes Terrestres, dice que "en todo transporte público de viajeros, los daños que sufran éstos estarán cubiertos por el seguro obligatorio de viajeros, en los términos que establezca la legislación específica sobre la materia". Dicho artículo debe ser puesto en relación con el art. 2.3 del Reglamento del Seguro Obligatorio de Viajeros (RD 1575/1989 de 22 de diciembre) que dispone que "el Seguro Obligatorio de Viajeros no libera a las Empresas transportistas, a los conductores de los vehículos, o a terceros, de la responsabilidad civil en que, dolosa o culposamente, pudieran incurrir por razón del transporte de personas, ni las prestaciones satisfechas por razón de dicho Seguro reducen el importe de la expresada responsabilidad". En consecuencia, el Seguro Obligatorio de Viajeros ampara a todo viajero de transporte público colectivo, sea o no vehículo a motor (art. 2.1 del Reglamento), y es compatible con la responsabilidad civil del transportista.

Debe diferenciarse la reclamación al transportista por haber incurrido en responsabilidad civil, de la reclamación que puede efectuarse con motivo del Seguro Obligatorio de Viajeros. En el primero de los supuestos, que es el que es objeto de este formulario, deberá acreditarse la negligencia del transportista, correspondiéndole a éste probar que fue diligente en el desarrollo de la relación contractual de transporte y que adoptó las medidas exigibles con arreglo a la diligencia técnica debida. En el segundo de los supuestos no es necesario acreditar negligencia alguna de la transportista, por cuanto el Seguro Obligatorio de Viajeros no es un seguro de responsabilidad civil, sino de accidentes. Ambas reclamaciones son compatibles.

El actor podría optar por acumular dos acciones en una misma demanda instada contra la compañía aseguradora: la acción por responsabilidad civil y la acción en reclamación de las prestaciones comprendidas en el contrato de seguro, de conformidad con lo establecido en los arts. 71 y ss. LEC.

El art. 7 d) de la Ley 35/2006, de 28 de noviembre, LIRPF, dice que están exentas «las indemnizaciones como consecuencia de responsabilidad civil por daños personales, en la cuantía legal o judicialmente reconocida».

En consecuencia, la indemnización que se otorgara en concepto de responsabilidad civil que pudiera reconocerse en sentencia estaría exenta del pago del IRPF.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
