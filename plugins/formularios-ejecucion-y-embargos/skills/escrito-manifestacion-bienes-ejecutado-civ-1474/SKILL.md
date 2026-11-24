---
name: escrito-manifestacion-bienes-ejecutado-civ-1474
description: "Escrito de manifestación de bienes del ejecutado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de manifestación de bienes del ejecutado

> Formulario **CIV-1474** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de manifestación de bienes del ejecutado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de manifestación de bienes del ejecutado” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-manifestacion-bienes-ejecutado-civ-1474`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº (3 veces)
- [ ] AÑO (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DÍA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MARCA/MODELO (2 veces)
- [ ] MES (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] SEDE (2 veces)
- [ ] COLEGIO
- [ ] DESCRIPCIÓN DE LOS DOCUMENTOS
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] ENTIDAD BANCARIA
- [ ] LUGAR
- [ ] MATRÍCULA
- [ ] Nº DE PROCEDIMIENTO

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…miento: / A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO]

Procedimiento: /

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

Dª/D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], representación que tengo acreditada en autos de ejecución nº [Nº DE PROCEDIMIENTO], seguidos contra mi representado a instancia de D./Dª [NOMBRE Y APELLIDOS], bajo la dirección técnica de D./Dª [NOMBRE Y APELLIDOS], Letrado del Ilustre Colegio de Abogados de [COLEGIO], comparezco ante el Tribunal y como mejor proceda en Derecho DIGO

Que por el presente escrito, siguiendo instrucciones expresas de mi mandante, formulo MANIFESTACIÓN DE BIENES, conforme a los siguientes

HECHOS

Por providencia de fecha [DÍA] de [MES] de [AÑO] este Tribunal requirió a mi representado para que manifestara bienes y derechos suficientes para cubrir la cuantía de la ejecución, con apercibimiento de las sanciones en las que podría incurrir de no dar exacto cumplimiento a lo requerido.

Por el presente escrito, dentro del plazo otorgado, mi representado, con el fin de dar satisfacción al citado requerimiento, manifiesta que es propietario de los siguientes bienes:

1. Bienes inmuebles:

Finca rústica, plantada de naranjos, sita en [LOCALIDAD] Es titular de una cuota indivisa del cincuenta por ciento sobre la citada finca, que se encuentra libre de arrendatarios y ocupantes.

Vivienda en [DESCRIPCIÓN DEL BIEN] Esta vivienda constituye el domicilio familiar, es de titularidad ganancial y se encuentra gravada con una hipoteca en favor de la entidad [DENOMINACIÓN SOCIAL] en garantía de [IMPORTE] euros ( €) de principal, [IMPORTE] euros ( €) de intereses remuneratorios y [IMPORTE] euros ( €) para costas y gastos.

2. Vehículos automóviles:

Turismo marca [MARCA/MODELO], modelo [MARCA/MODELO], matrícula [MATRÍCULA]

3. Cuentas corrientes:

Cuenta corriente número [NÚMERO] en la entidad bancaria [ENTIDAD BANCARIA] con un saldo, a fecha de hoy, de [IMPORTE] euros ( €).

4. Valores mobiliarios:

Participaciones sociales números [Nº] a [Nº] en la sociedad [DENOMINACIÓN SOCIAL], inscrita en el registro Mercantil de [LOCALIDAD]

Como fundamento de los anteriores hechos se acompañan los siguientes DOCUMENTOS [DESCRIPCIÓN DE LOS DOCUMENTOS]

Resultan aplicables a los hechos expuestos, los siguientes

FUNDAMENTOS DE DERECHO

ÚNICO.- El artículo 589 de la Ley de Enjuiciamiento Civil establece: "1. Salvo que el ejecutante señale bienes cuyo embargo estime suficiente para el fin de la ejecución, el Letrado de la Administración de Justicia requerirá, mediante diligencia de ordenación, de oficio al ejecutado para que manifieste relacionadamente bienes y derechos suficientes para cubrir la cuantía de la ejecución, con expresión, en su caso, de cargas y gravámenes, así como, en el caso de inmuebles, si están ocupados, por qué personas y con qué título.

2. El requerimiento al ejecutado para la manifestación de sus bienes se hará con apercibimiento de las sanciones que pueden imponérsele, cuando menos por desobediencia grave, en caso de que no presente la relación de sus bienes, incluya en ella bienes que no sean suyos, excluya bienes propios susceptibles de embargo o no desvele las cargas y gravámenes que sobre ellos pesaren.

3. El Letrado de la Administración de Justicia podrá también, mediante decreto, imponer multas coercitivas periódicas al ejecutado que no respondiere debidamente al requerimiento a que se refiere el apartado anterior.

Para fijar la cuantía de las multas, se tendrá en cuenta la cantidad por la que se haya despachado ejecución, la resistencia a la presentación de la relación de bienes y la capacidad económica del requerido, pudiendo modificarse o dejarse sin efecto el apremio económico en atención a la ulterior conducta del requerido y a las alegaciones que pudiere efectuar para justificarse.

Frente a estas resoluciones del Letrado de la Administración de Justicia cabrá recurso directo de revisión, sin efecto suspensivo, ante el Tribunal que conozca de la ejecución."

Por el presente escrito se da exacto cumplimiento al requerimiento del Letrado de la Administración de Justicia, antes citado, por el que se ordenaba a mi representado/a la manifestación de sus bienes.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito junto con sus documentos y copias, lo admita y tenga por cumplimentado el requerimiento efectuado y por realizada la manifestación de bienes y derechos.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
