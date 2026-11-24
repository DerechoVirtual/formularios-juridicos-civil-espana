---
name: manifestacion-herencia-intestada-conyuge-como-heredero-civ-0416
description: "Manifestación de herencia intestada por el cónyuge como heredero único. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Manifestación de herencia intestada por el cónyuge como heredero único

> Formulario **CIV-0416** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Manifestación de herencia intestada por el cónyuge como heredero único» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Manifestación de herencia intestada por el cónyuge como heredero único” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:manifestacion-herencia-intestada-conyuge-como-heredero-civ-0416`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (16 veces)
- [ ] AÑO (7 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] DÍA (6 veces)
- [ ] MES (6 veces)
- [ ] NÚMERO (4 veces)
- [ ] DATOS REGISTRALES (2 veces)
- [ ] FOLIO
- [ ] IMPORTE
- [ ] LIBRO
- [ ] LUGAR
- [ ] NIF
- [ ] Nº
- [ ] TOMO

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

MANIFESTACIÓN DE LA HERENCIA DE D./Dª [NOMBRE Y APELLIDOS] - SU ESPOSO/A D./Dª [NOMBRE Y APELLIDOS]

En [LUGAR], a [DÍA] de [MES] de [AÑO].,

D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en [LOCALIDAD], y con DNI/NIF [NIF],

INTERVIENE en su propio nombre y derecho, como único interesado en la sucesión de D./Dª [NOMBRE Y APELLIDOS], y previos los asesoramientos técnicos y jurídicos correspondientes, procede a realizar la manifestación de herencia del/la indicado/a causante, para lo que

EXPONE

FALLECIMIENTO, ESTADO CIVIL Y ÚLTIMA VOLUNTAD DE D./Dª [NOMBRE Y APELLIDOS], titular del documento nacional de identidad, número [NÚMERO]: Dicho/a señor/a falleció en [LOCALIDAD], de donde era natural y vecino/a, el día [DÍA] de [MES] de [AÑO], en estado de casado con D./Dª [NOMBRE Y APELLIDOS], de cuyo único matrimonio, no tuvo descendiente alguno, habiéndole premuerto sus ascendientes. No consta que dicho señor/a hubiera otorgado disposición testamentaria alguna, por lo que instada ante D./Dª [NOMBRE Y APELLIDOS], Notario/a de [LOCALIDAD], la correspondiente acta de requerimiento de declaración de herederos abintestato, con fecha [DÍA] de [MES] de [AÑO], bajo el número [NÚMERO] de protocolo, se declaró "único/a heredero/a abintestato de D./Dª [NOMBRE Y APELLIDOS], a su citado/a esposo/a, D./Dª [NOMBRE Y APELLIDOS] ", mediante acta de notoriedad de fecha [DÍA] de [MES] de [AÑO], número [NÚMERO] de protocolo. Copias autorizadas de las referidas actas se acompañarán a la presente donde proceda.

Consecuentemente con lo hasta ahora expuesto, el/la único/a interesado/a en la herencia de D./Dª [NOMBRE Y APELLIDOS] es el/la citado/a esposo/a del/la causante, D./Dª [NOMBRE Y APELLIDOS]

INVENTARIO Y AVALÚO.- El único bien relicto por el/la causante, de carácter privativo del mismo, según el título que se dirá, es el siguiente: Se valora dicha finca, en la cantidad de [IMPORTE] EUROS -EUROS-. INSCRIPCIÓN.- Pendiente de inscripción el título que se dirá, se cita como referencia registral la del Registro de la Propiedad de [LOCALIDAD], HOY [DATOS REGISTRALES], tomo [TOMO], libro [LIBRO], folio [FOLIO], finca número [NÚMERO] -antes [DATOS REGISTRALES] y antes -.TÍTULO.- Le pertenecía al/la causante dicha finca, con carácter privativo, por adjudicación en la herencia de su padre, D./Dª [NOMBRE Y APELLIDOS], fallecido el día [DÍA] de [MES] de [AÑO], en virtud de escritura autorizada por D./Dª [NOMBRE Y APELLIDOS], Notario/a que fue de [LOCALIDAD], el día [DÍA] de [MES] de [AÑO], la cual se encuentra pendiente de inscripción (o el título que proceda).

CARGAS Y ARRIENDOS.- Libre de unas y otros, así como al corriente en el pago de los gastos de comunidad.

REFERENCIA CATASTRAL:.- Así resulta y se acredita con la exhibición del recibo justificativo del pago del Impuesto sobre Bienes Inmuebles del año [AÑO], del cual se acompaña una copia. Igualmente se ha solicitado y obtenido, de la Oficina Virtual del Catastro, a estos solos efectos, conforme a la Ley 2/2011, de Economía Sostenible, una certificación catastral descriptiva y gráfica telemática de la finca descrita, copia de la cual también se acompaña.

TRIBUTOS.- Se manifiesta que la finca se encuentra al corriente en el pago del Impuesto sobre Bienes Inmuebles. No obstante, en relación al artículo 65.1 de la Ley Reguladora de las Haciendas Locales, se advierte que el inmueble objeto de esta declaración está afecto al pago de la cuota tributaria correspondiente al Impuesto sobre Bienes Inmuebles que pudiera haber pendiente, no habiéndose obtenido la correspondiente información del Ayuntamiento, por las posibles deudas pendientes del mismo, conociéndose las consecuencias que de ello pudieran derivarse.

ACEPTACIÓN DE LA HERENCIA Y ADJUDICACIÓN.- D./Dª [NOMBRE Y APELLIDOS], por la presente hace solemne manifestación de la herencia de su esposo/a D./Dª [NOMBRE Y APELLIDOS], y como único/a heredero/a abintestato del/la mismo/a se ADJUDICA la finca descrita, por el valor expresado.

DETERMINACIONES FISCALES: Se hace constar que el/la causante era residente en la Comunidad Autónoma de [LOCALIDAD], en los cinco años anteriores desde la fecha de su fallecimiento, así como que el/la heredero/a tiene su residencia en dicha Comunidad con fecha superior a un año desde la fecha del devengo del Impuesto. Por lo que solicita las reducciones y bonificaciones que les sean aplicables en el Impuesto sobre Sucesiones y Donaciones en esta Comunidad; y que su patrimonio preexistente es de cuantía inferior al previsto para la aplicación de coeficientes multiplicadores en la determinación de la cuota tributaria del Impuesto sobre Sucesiones.

Y en virtud de lo expuesto, quedan formalizadas la operaciones sucesorias de la herencia de D./Dª [NOMBRE Y APELLIDOS], dándose el/la único/a interesado/a por satisfecho/a y pagado/a, con la adjudicación hecha a su favor, igual a su haber, y en prueba de conformidad firma con la fecha indicada en el encabezamiento de la presente que queda extendido en [Nº] folios de papel común.

Firma del/la declarante.

========================================================================
