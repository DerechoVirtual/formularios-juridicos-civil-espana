---
name: escrito-tercero-titular-no-registral-vivienda-familiar-civ-0267
description: "Escrito del tercero titular no registral de la vivienda familiar que se opone a su embargo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del tercero titular no registral de la vivienda familiar que se opone a su embargo

> Formulario **CIV-0267** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del tercero titular no registral de la vivienda familiar que se opone a su embargo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del tercero titular no registral de la vivienda familiar que se opone a su embargo” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:escrito-tercero-titular-no-registral-vivienda-familiar-civ-0267`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (8 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] FECHA (4 veces)
- [ ] Nº (3 veces)
- [ ] SEDE (3 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] PISO (2 veces)
- [ ] PUERTA (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] COLEGIO
- [ ] CURSO
- [ ] DENOMINACIÓN SOCIAL
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE DEL CENTRO
- [ ] NOMBRE DEL MENOR
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 593 LEC

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

- Junto a «…AD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LOS DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…idos ante esta Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LOS DE [SEDE]

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre y representación de Don [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], comparezco en los autos de procedimiento ejecutivo [Nº DE PROCEDIMIENTO] promovidos por Don [NOMBRE Y APELLIDOS] contra Don [NOMBRE Y APELLIDOS], seguidos ante esta Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] y, como mejor proceda en Derecho, DIGO:

Que en méritos del requerimiento efectuado por ese Tribunal a mi principal y al amparo de lo previsto en el artículo 593 de la LEC y en relación con el eventual embargo sobre el bien inmueble sito en la localidad de [LOCALIDAD], calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], y supuestamente propiedad de [NOMBRE DE LA PARTE], esta parte dentro del plazo de cinco días allí conferido, mediante el presente escrito pasa a OPONERSE AL EMBARGO sobre dicho bien con base en las siguientes

ALEGACIONES

PRIMERA.- ADQUISICIÓN VIVIENDA.

Que la finca sobre la que se pretende el embargo pertenece realmente a mi mandante Don [NOMBRE Y APELLIDOS] desde el día [FECHA] del mes [MES] del año [AÑO] en que el ejecutado [NOMBRE DE LA PARTE], aún hoy aparente propietario al resultar el titular registral, vendió mediante documento privado la finca a mi principal, entregando la posesión de la finca en aquel mismo acto, según resulta del propio documento y de sus pactos. En prueba de lo manifestado se acompaña ejemplar auténtico del documento privado de compraventa, como Documento núm. [Nº], que constituye a su vez el principio de prueba escrito que exige el artículo 595.3 de la Ley de Enjuiciamiento Civil como fundamento de la pretensión de mi principal.

SEGUNDA.- VIVIENDA FAMILIAR.

Que dicha vivienda constituye además el domicilio familiar de mi representado y que ocupa junto a su cónyuge e hijos, todos ellos menores de edad. La realidad de la transmisión recogida en el documento privado que queda aportado y el carácter de domicilio familiar resulta acreditada mediante los documentos que a continuación se indican, la mayoría de los cuales son de fecha anterior, incluso, al nacimiento de la obligación recogida en el título del que deriva el presente procedimiento:

a) Certificado del padrón municipal acreditativo de la primera fecha de ocupación por parte de mi mandante y su familia de la finca de referencia, que acompaño como Documento núm. [Nº DE DOCUMENTO].

b) Certificado del colegio público [NOMBRE DEL CENTRO] acreditativo de que el hijo menor [NOMBRE DEL MENOR] cursa estudios desde el curso académico [CURSO] en el indicado centro por ser el que le corresponde en función de la ubicación de la vivienda familiar de los padres, que acompaño como Documento núm. [Nº DE DOCUMENTO].

c) Solicitud de alta de línea telefónica de fecha [FECHA], así como contrato realizado con la compañía telefónica [DENOMINACIÓN SOCIAL] en el momento de dar de alta la línea telefónica, que acompaño como Documentos núms. y [Nº DE DOCUMENTO].

d) Póliza de contratación de suministro de energía eléctrica suscrito con la compañía suministradora a título de dueño de fecha [FECHA], así como recibos de consumos del último año, que acompaño como Documentos núms. a [Nº DE DOCUMENTO].

e) Póliza de contratación de suministro de gas natural suscrito con las compañía suministradora a título de dueño de fecha [FECHA], así como recibos de consumos del último año, que acompaño como Documentos núms. a [Nº DE DOCUMENTO].

f) Actas de Junta de copropietarios del inmueble en el que se ubica la finca, celebradas al amparo de la Ley de Propiedad Horizontal y en las que resulta presente mi principal como propietario del piso [PISO] puerta [PUERTA] que constituye la finca cuyo embargo se pretende, que acompaño como Documentos núms. a [Nº DE DOCUMENTO].

g) Acta notarial de manifestaciones recogida por el Ilustre Notario de esta ciudad Don [NOMBRE Y APELLIDOS], y recogidas de los vecinos del mismo inmueble y en las que se constata el carácter de ser la vivienda en cuestión el domicilio familiar de representado, que acompaño como Documento núm. [Nº DE DOCUMENTO].

TERCERA.- NO PROCEDENCIA DEL EMBARGO.

Que a la vista del documento privado de compraventa y demás documentos aportados, entiende esta parte que no procede el embargo sobre dicha finca por ser propiedad de mi principal, no pertenecer ya al demandado ejecutado, y ser el domicilio familiar de mi representado y su familia.

Por lo expuesto,

SOLICITO AL TRIBUNAL: Que teniendo por presentado este escrito con los documentos acompañados (en su caso, y copia de todo), se sirva admitirlo y en sus méritos, haya por acreditada la plena propiedad y dominio de mi representado sobre el bien inmueble cuyo embargo se pretendía en los presentes Autos, y como quiera que trata de la vivienda familiar del mismo y en evitación de una tercería de dominio y previo dar traslado a las partes ejecutante y ejecutada a los fines de que manifiesten lo que a su derecho convenga, resuelva abstenerse de acordar el embargo pretendido, prosiguiendo la ejecución sobre otros bienes propiedad del ejecutado.

Es Justicia que insto en (lugar y fecha).

Firmas de Letrado y Procurador.

========================================================================
