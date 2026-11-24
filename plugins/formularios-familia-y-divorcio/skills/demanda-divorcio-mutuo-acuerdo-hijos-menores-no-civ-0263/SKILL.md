---
name: demanda-divorcio-mutuo-acuerdo-hijos-menores-no-civ-0263
description: "Demanda de divorcio de mutuo acuerdo con hijos menores no emancipados. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio de mutuo acuerdo con hijos menores no emancipados

> Formulario **CIV-0263** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio de mutuo acuerdo con hijos menores no emancipados» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio de mutuo acuerdo con hijos menores no emancipados” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-mutuo-acuerdo-hijos-menores-no-civ-0263`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] AÑO (3 veces)
- [ ] FECHA (3 veces)
- [ ] MES (3 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] CALLE
- [ ] FOLIO
- [ ] LUGAR Y FECHA
- [ ] NOMBRE DEL HIJO/A 1
- [ ] NOMBRE DEL HIJO/A 2
- [ ] NÚMERO
- [ ] SECCIÓN
- [ ] SEDE
- [ ] TOMO
- [ ] VECINDAD CIVIL

## Normas que cita el formulario

- art. 81 Código Civil
- art. 90.3 CC
- art. 81 CC

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

- Junto a «…CIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…volución del original, ante la Sección Civil del Tribunal de Instancia de [SEDE]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA

-SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD-

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales en nombre de los esposos Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS], mayores de edad, de profesión [PROFESIÓN] el marido y de profesión [PROFESIÓN] la esposa, vecinos de la localidad de [LOCALIDAD], con domicilio en calle [CALLE], número [NÚMERO], cuya representación acredito mediante escritura de poderes que acompaño para su unión a los autos mediante testimonio, previo cotejo y devolución del original, ante la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda comparezco y como mejor proceda en Derecho, DIGO:

Que en la indicada representación, siguiendo instrucciones de mis principales, promuevo petición de DIVORCIO DE MUTUO ACUERDO, la cual baso en los siguientes

HECHOS

PRIMERO.- Mis principales contrajeron matrimonio en forma [ELEGIR: civil / religiosa], el día [FECHA], del mes de [MES], del año [AÑO], en la localidad de [LOCALIDAD], conforme acredito mediante certificación literal de matrimonio expedida por el Registro Civil, que acompaño como documento núm. uno, constando inscrito el mismo en el Tomo [TOMO], Folio [FOLIO], Sección [SECCIÓN], de lo que se deduce que se cumple con creces el requisito que exige el Código Civil del transcurso de tres meses desde la celebración del matrimonio.

SEGUNDO.- Del citado matrimonio nacieron y viven en la actualidad, [NOMBRE DEL HIJO/A 1] y [NOMBRE DEL HIJO/A 2] nacidos, respectivamente, el día [FECHA], del mes de [MES], del año [AÑO], y el día [FECHA], del mes de [MES], del año [AÑO], según acredito mediante las respectivas certificaciones literales de nacimiento expedidas por el Registro Civil de [LOCALIDAD], que acompaño como documentos núms. dos y tres.

TERCERO.- El domicilio familiar está sito en [LOCALIDAD], según acredito mediante certificación de empadronamiento, que acompaño como documento núm. cuatro.

CUARTO.- El régimen económico del matrimonio es el de sociedad de gananciales, ya que ambos esposos tenían vecindad civil [VECINDAD CIVIL] cuando contrajeron matrimonio y no se han otorgado capitulaciones matrimoniales.

QUINTO.- Siendo voluntad de ambas partes proceder a la disolución por divorcio de mutuo acuerdo, acompañan como documento núm. cinco, la preceptiva propuesta de convenio regulador, a fin de que, previa su ratificación por separado, e Informe del Ministerio Fiscal, sea aprobado judicialmente y queden regulados conforme al mismo los efectos derivados de dicha disolución.

A los anteriores Hechos le son de aplicación los siguientes.

FUNDAMENTOS DE DERECHO

PRIMERO.- COMPETENCIA.- Es competente este Tribunal por razón del domicilio conyugal o del domicilio de cualquiera de los conforme prevé el artículo 769.2 de la Ley de Enjuiciamiento Civil.

SEGUNDO.- PROCEDIMIENTO.- Es de aplicación el procedimiento previsto en el artículo 777 de la Ley de Enjuiciamiento Civil, en la nueva redacción dada por la Ley 8/2021 de 2 de junio, a cuyo tenor:

“Si hubiera hijos menores, o hijos mayores con discapacidad y medidas de apoyo atribuidas a sus progenitores, el Tribunal recabará informe del Ministerio Fiscal sobre los términos del convenio relativos a los hijos y serán oídos cuando se estime necesario de oficio o a petición del fiscal, partes o miembros del equipo técnico judicial o del propio hijo. Estas actuaciones se practicarán durante el plazo a que se refiere el apartado anterior o, si este no se hubiera abierto, en el plazo de cinco días.”

TERCERO.- LEGITIMACIÓN.- La ostentan ambas partes por su condición de cónyuges del matrimonio con hijos menores cuyo divorcio de mutuo acuerdo se solicita, de conformidad con lo previsto en el art. 81 y 86 del Código Civil.

CUARTO.- INTERVENCIÓN DEL MINISTERIO FISCAL. Existiendo hijos menores de edad, y de conformidad con lo establecido en los artículos 749 y 777.5 ambos de la LECiv, debe ser parte el Ministerio Fiscal.

QUINTO.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD. La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional, de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia, por tratarse en sí de un acuerdo consensual y voluntario entre las partes, necesitando únicamente la homologación del mismo por parte del Tribunal, siendo que el convenio regulador (arts. 775.2 y 777.9 LEC y art. 90.3 CCiv) se entiende acreditativo de haber realizado esa actividad negociadora.

SEXTO.- DIVORCIO DE MUTUO ACUERDO.- El artículo 86 en relación con el art. 81 del Código Civil, en la nueva redacción dada por la Ley 8/2021, establece que: “Se decretará judicialmente el divorcio, cualquiera que sea la forma de celebración del matrimonio, a petición de uno solo de los cónyuges, de ambos o de uno con el consentimiento del otro, cuando concurran los requisitos y circunstancias exigidos en el artículo 81”.

El artículo 81 CC dispone:

Se decretará judicialmente la separación cuando existan hijos menores no emancipados o hijos mayores respecto de los que se hayan establecido judicialmente medidas de apoyo atribuidas a sus progenitores, cualquiera que sea la forma de celebración del matrimonio:

1.º A petición de ambos cónyuges o de uno con el consentimiento del otro, una vez transcurridos tres meses desde la celebración del matrimonio. A la demanda se acompañará una propuesta de convenio regulador redactada conforme al artículo 90 de este Código.

2.º A petición de uno solo de los cónyuges, una vez transcurridos tres meses desde la celebración del matrimonio. No será preciso el transcurso de este plazo para la interposición de la demanda cuando se acredite la existencia de un riesgo para la vida, la integridad física, la libertad, la integridad moral o libertad e indemnidad sexual del cónyuge demandante o de los hijos de ambos o de cualquiera de los miembros del matrimonio.

A la demanda se acompañará propuesta fundada de las medidas que hayan de regular los efectos derivados de la separación.

SÉPTIMO.- EFECTOS. Artículos 89 y 90 del Código Civil.

En su virtud

Suplico al Tribunal

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y lo admita; por promovido por el Procurador que suscribe, con quien se entiendan las sucesivas diligencias, en nombre y representación de Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS], con devolución de la escritura de poderes acompañada una vez quede testimonio en autos, petición de DISOLUCIÓN MATRIMONIAL POR DIVORCIO DE MUTUO ACUERDO; y, por los trámites procesales pertinentes, previa ratificación de las partes por separado, audiencia de los menores y con intervención del Ministerio Fiscal, dicte sentencia por la que, dando lugar a la disolución, determine como efectos derivados de la misma los contenidos en la propuesta de convenio regulador aportado como documento núm. cinco, el cual sea íntegramente aprobado.

Es justicia que insto en [LUGAR Y FECHA].

Firmas de Letrado y Procurador.

========================================================================
