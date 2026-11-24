---
name: auto-estima-eficacia-civil-sentencia-canonica-nulidad-civ-1873
description: "Auto que estima la eficacia civil de sentencia canónica de nulidad matrimonial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que estima la eficacia civil de sentencia canónica de nulidad matrimonial

> Formulario **CIV-1873** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto por el que se reconoce eficacia civil a la sentencia de nulidad matrimonial dictada por un Tribunal Eclesiástico (art. 80 CC y art. 778 LEC), tras oír al otro cónyuge y al Ministerio Fiscal, cuando solo se pide el reconocimiento de eficacia civil y no medidas.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que estima la eficacia civil de sentencia canónica de nulidad matrimonial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que estima la eficacia civil de sentencia canónica de nulidad matrimonial” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-estima-eficacia-civil-sentencia-canonica-nulidad-civ-1873`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A (2 veces)
- [ ] ALEGACIONES DEL CÓNYUGE Y DEL MINISTERIO FISCAL
- [ ] CONTENIDO DE LA RESOLUCIÓN CANÓNICA
- [ ] FIRMA
- [ ] GRUPO
- [ ] NOMBRE Y APELLIDOS DEL SOLICITANTE
- [ ] Nº
- [ ] Nº DE CUENTA
- [ ] PROVINCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 80 CC
- art. 778.1 LEC
- art. 44 Ley 29/2015
- art. 458.2 LEC

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

AUTO

D./Dña. [NOMBRE Y APELLIDOS], Magistrado-Juez de la [ELEGIR: Sección de Familia, Infancia y Capacidad / Sección Civil] del Tribunal de Instancia de [SEDE], plaza n.º [Nº].

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

ANTECEDENTES DE HECHO

PRIMERO.– Por el/la Procurador/a D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL SOLICITANTE], se ha presentado demanda de solicitud de eficacia civil de la resolución canónica sobre la nulidad del matrimonio que formó con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], sin que solicitara adopción o modificación de medidas.

La resolución canónica es la siguiente: sentencia del Tribunal Eclesiástico de [LOCALIDAD], de fecha [DÍA] de [MES] de [AÑO], que [CONTENIDO DE LA RESOLUCIÓN CANÓNICA].

SEGUNDO.– De la anterior solicitud se ha dado audiencia por diez días al otro cónyuge y al Ministerio Fiscal, dentro de cuyo plazo D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], a través de su mandatario procesal D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], [ALEGACIONES DEL CÓNYUGE Y DEL MINISTERIO FISCAL].

FUNDAMENTOS DE DERECHO

PRIMERO.– Conjuntando el carácter aconfesional del Estado con la toma en consideración de la creencia religiosa dominante en la sociedad española, que fuerza a mantener relaciones de cooperación con la Iglesia Católica (art. 16.3 CE), se tiene reconocida la actividad de jurisdicción de aquella en el Acuerdo entre el Estado Español y la Santa Sede de 3 de enero de 1979 (art. VI.2), y se desarrolló en el art. 80 CC, asumiéndose que determinadas decisiones de la Iglesia Católica puedan alcanzar efectos de cosa juzgada material como si de sentencias de un juez civil español se trataran.

SEGUNDO.– Corresponde al juez civil plenitud de conocimiento en todas aquellas cuestiones que exceden del mero reconocimiento de la eficacia civil de lo que constituye pronunciamiento principal, de la sentencia de nulidad canónica o la decisión del Papa sobre matrimonio rato y no consumado, como es doctrina constitucional (STC 6/1997), y si no se pide más que el reconocimiento de eficacia civil, aunque la audiencia por plazo de diez días al otro cónyuge y al Ministerio Fiscal que establece el art. 778.1 LEC, que veda acudir al juicio ordinario o al de nulidad del matrimonio, no lo explicita, resulta factible que el consorte putativo, según la sentencia canónica (al igual que el Fiscal), se oponga a la homologación, según ha sido el caso.

TERCERO.– Conforme al art. 80 CC, que remite a los requisitos para el reconocimiento de resoluciones extranjeras o «exequátur», el juez civil ha de determinar si la resolución eclesiástica resulta ajustada al Derecho del Estado, lo cual se limita a la comprobación de si es auténtica, no se ha dictado en rebeldía, es firme, si se han respetado los principios constitucionales del proceso y, en fin, si no se vulnera el orden público matrimonial del Reino.

Es así que el demandado D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE] ha sido parte personada en el procedimiento canónico, aunque no haya alegado ni expuesto ni participado en prueba alguna, con lo que no se colocó en rebeldía procesal ante la sentencia, de lo que deriva que, cumpliéndose todas las demás exigencias, procede reconocer su eficacia en el plano civil por el Estado, dado que los arts. 44 y siguientes de la Ley 29/2015, de 30 de julio, de cooperación jurídica internacional en materia civil, no urgen una contienda procesal, sino la comparecencia que viabilice la efectiva contradicción, aunque esta no se produzca por voluntad de la parte.

PARTE DISPOSITIVA

1.– Se acuerda reconocer eficacia civil a la resolución dictada por el Tribunal Eclesiástico de [LOCALIDAD], el día [DÍA] de [MES] de [AÑO], por la que se declaró la nulidad del matrimonio celebrado en [LOCALIDAD], con fecha [DÍA] de [MES] de [AÑO], entre D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], sin especial declaración de costas.

2.– Comuníquese el presente auto al Encargado del Registro Civil de [LOCALIDAD].

Así lo acuerdo, mando y firmo.

Firma del Juez/a: [FIRMA]

Contra la presente resolución cabe recurso de apelación para ante la Audiencia Provincial de [PROVINCIA], que se ha de interponer mediante escrito que se ha de presentar en este Tribunal en plazo de veinte días hábiles contados desde el siguiente al de la notificación, exponiendo el apelante las alegaciones en que se base la impugnación, además de citar la resolución apelada y los pronunciamientos que impugna (art. 458.2 LEC).

Para interponer el recurso será necesaria la constitución de un depósito de 50 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [Nº DE CUENTA], indicando en el campo concepto del resguardo de ingreso que se trata de un «Recurso» código 02-Apelación. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª LOPJ).

No están obligados a constituir el depósito para recurrir los declarados exentos en la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.
