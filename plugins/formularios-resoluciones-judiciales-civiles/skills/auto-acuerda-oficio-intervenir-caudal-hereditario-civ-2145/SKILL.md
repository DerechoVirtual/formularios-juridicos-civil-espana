---
name: auto-acuerda-oficio-intervenir-caudal-hereditario-civ-2145
description: "Auto que acuerda de oficio intervenir el caudal hereditario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que acuerda de oficio intervenir el caudal hereditario

> Formulario **CIV-2145** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Modelo de auto acordando, de oficio, la intervención del caudal hereditario del causante, incoándose pieza separada para la declaración de herederos abintestato, procediéndose a la ocupación de los libros, papeles y correspondencia del difunto y formando inventario de los bienes del caudal hereditario.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que acuerda de oficio intervenir el caudal hereditario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que acuerda de oficio intervenir el caudal hereditario” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-acuerda-oficio-intervenir-caudal-hereditario-civ-2145`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] GRUPO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 791.2 LEC
- art. 954 CC
- art. 12 Ley 52/1997
- art. 451 LEC

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

- Junto a «…or la sección de Instrucción del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

AUTO

En [LUGAR], a [FECHA].

Juez/a Sr./a.

ANTECEDENTES DE HECHO

PRIMERO

A raíz de la recepción de testimonio de Diligencias Previas incoadas por la sección de Instrucción del Tribunal de Instancia de [SEDE], plaza n.º [Nº] , se formó expediente para adoptar medidas indispensables de seguridad de los bienes del fallecido D./Doña [NOMBRE Y APELLIDOS], practicándose diligencia de prevención en fecha [FECHA].

SEGUNDO

Se han proveído las medidas conducentes para averiguar si existe disposición testamentaria, y si existen parientes con derecho a la sucesión legítima, habiéndose reportado los oficios y exhortos remitidos, y practicada información testifical, con el resultado de que no hay acto de última voluntad ni pariente llamado a suceder.

RAZONAMIENTOS JURÍDICOS

PRIMERO

De conformidad con el art. 791.2 LEC, cuando de la averiguación resulte que el fallecido no testó y no hay parientes legalmente llamados a la sucesión, se abrirá de oficio pieza separada para la declaración de herederos abintestato, lo que procede en el presente caso, ya que el pariente encontrado en [LOCALIDAD] resulta colateral en quinto grado, al que no se extiende el derecho a heredar abintestato conforme al art. 954 CCiv.

SEGUNDO

Además de lo anterior, puesto que no se certifica disposición testamentaria, ni se conocen parientes que deban heredar legalmente, el tribunal, según indica el mismo precepto, debe acordar, primero, la ocupación de los libros, papeles y correspondencia del difunto, y segundo, alternativamente, el inventario y depósito judiciales, disponiendo lo que proceda sobre la administración del caudal, o el nombramiento de un depositario-administrador con cargo al caudal hereditario, y con facultades para efectuar y garantizar el inventario y depósito.

Se opta por el segundo de los expedientes de intervención, habida cuenta de que los bienes del finado lo permiten, y descargando labor al Tribunal, mediante designación de la Comunidad Autónoma, dado que está previsto el destino al Estado heredero legítimo en la persona de la Generalitat de Catalunya, a tenor del art. 442-12.1 del libro cuarto del Código Civil de Cataluña, relativo a las sucesiones, aprobado por Ley 10/2008, de 10 de julio, al que se dispensará de constituir caución, por aplicación de la Disposición Adicional 4.ª, en relación con art. 12 de la Ley 52/1997, de 27 de noviembre, de Asistencia Jurídica al Estado e Instituciones Públicas

PARTE DISPOSITIVA

Se acuerda la intervención del caudal hereditario de D./Doña [NOMBRE Y APELLIDOS],

1.- Incóese pieza separada para la declaración de herederos abintestato.

2.- Procédase a la ocupación de los libros, papeles y correspondencia del difunto.

3.- Fórmese inventario de los bienes del caudal hereditario, y queden éstos en depósito de la Comunidad Autónoma, a quien se le nombra también administradora, haciéndole saber esta designación al Letrado Jefe de sus Servicios Jurídicos para la aceptación y juramento del cargo, con exención de constituir fianza.

Se señala el próximo día [FECHA], a las [Nº] horas, para la práctica de la diligencia de apertura de la correspondencia, de ocupación, y de constitución del depósito al representante de la entidad administradora.

Con testimonio de la presente resolución y de la aceptación del cargo de la depositaria-administradora, fórmese la pieza separada de administración.

Así lo dispongo, mando y firmo.

Firma del Juez/a

MODO DE IMPUGNACIÓN: Mediante recurso de reposición ante este Tribunal, que deberá interponerse por escrito en el plazo de cinco días hábiles contados desde el siguiente a la notificación, con expresión de la infracción cometida a juicio del recurrente, sin cuyos requisitos no se admitirá, y no obstante lo cual, se llevará a efecto lo acordado (arts. 451 y 452 LEC).

Para interponer el recurso será necesaria la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

========================================================================
