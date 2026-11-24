---
name: estatutos-subcomunidad-plazas-garaje-trasteros-civ-0623
description: "Estatutos de una subcomunidad de plazas de garaje y trasteros. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Estatutos de una subcomunidad de plazas de garaje y trasteros

> Formulario **CIV-0623** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Estatutos de una subcomunidad de plazas de garaje y trasteros» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Estatutos de una subcomunidad de plazas de garaje y trasteros” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:estatutos-subcomunidad-plazas-garaje-trasteros-civ-0623`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (3 veces)
- [ ] AÑO
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA COMUNIDAD
- [ ] NÚMERO

## Normas que cita el formulario

- art. 396 Código Civil

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

DISPOSICIÓN GENERAL

Los presentes estatutos tienen por objeto regular el régimen jurídico, económico, organizativo y funcional de la subcomunidad de garajes constituida en la COMUNIDAD GENERAL DE PROPIETARIOS [NOMBRE DE LA COMUNIDAD] Nº [NÚMERO] de [LOCALIDAD], compuesta de [Nº] plantas de sótano divididas en un total de [Nº] plazas de garaje y [Nº] trasteros.

TÍTULO I.-CONFIGURACIÓN OBJETIVA DE LA PROPIEDAD

Artículo 1.- El local objeto del presente régimen especial, forma parte de la Comunidad del edificio [DIRECCIÓN], en la proporción reconocida en la escritura de constitución de la propiedad horizontal, y se subdivide en plazas de garaje y cuartos trasteros, susceptibles de aprovechamiento independiente, a los que se señalará a cada uno, la cuota de participación que corresponda a la superficie útil de cada plaza o trastero en relación al total del local subdividido.

Artículo 2.-. Se consideran elementos comunes privativos del presente condominio:

I) los citados en el art. 396 del Código Civil

II) las paredes interiores y elementos de cualquier clase del interior del local, destinadas al uso común y general

III) las servidumbres establecidas y que se constituyan en el título de constitución

Artículo 3.-. Corresponde a cada uno de los titulares de las distintas plazas y/o trasteros:

I) el derecho exclusivo de uso y disfrute en pleno dominio o en arrendamiento del espacio delimitado y numerado, susceptible de aprovechamiento independiente, bien sea como plaza o como trastero

II) el uso y en su caso el dominio, en copropiedad con el resto de titulares, de las rampas y espacios de circulación, entrada y salida y maniobra, con todos los elementos comunes de disfrute y aprovechamiento general dentro del local subdividido.

Artículo 4.- En caso de cotitularidad de una parcela o garaje, se designará un representante por cada una de las plazas o trasteros para el ejercicio de sus derechos y todos los propietarios responderán solidariamente de sus obligaciones para con la comunidad. En caso de usufructo, la asistencia y voto en Junta corresponderá al nudo propietario.

Artículo 5.- Los titulares, por el título que sea, podrán hacer uso de los elementos comunes privativos del local subdividido, conforme al destino de los mismos, y siempre que no perjudiquen los derechos de otros titulares.

Artículo 6.- Serán responsables de los daños causados en las cosas comunes o en la propiedad de otros titulares, cuando estos se hubieran causado por negligencia, dolo, omisión, o bien las que provengan de actos realizados por los usuarios de sus plazas, empleados o familiares.

Artículo 7.- La duración de la comunidad será indefinida, y sólo podrá ser disuelta en los casos previstos en la vigente legislación sobre propiedad horizontal.

TÍTULO II.- RÉGIMEN DE OBLIGACIONES DE LOS PROPIETARIOS

Artículo 8.- Aparcar los vehículos dentro de los límites señalados de cada plaza, quedando terminantemente prohibido el aparcamiento en pasillos, vías de acceso, rampas o espacios no destinados especialmente al aparcamiento.

1º- Dedicar la plaza de garaje única y exclusivamente a aparcamiento de vehículos automóviles, prohibiéndose destinarla a cualquier otro fin.

2º- No realizar ni en las plazas de garaje ni en las zonas comunes, obras de cualquier clase, ya sean temporales o fijas.

3º- Utilizar las zonas de maniobra, paso y circulación conforme a su destino específico, sin que se pueda estacionar en ellas, ni impedir en cualquier forma, su utilización por cualquier otro titular.

4º- No instalar en las plazas de garaje, en tanto están destinadas a aparcamiento, máquinas, motores, útiles o enseres de cualquier clase, ni utilizarlas como almacén o depósito.

5º- Las plazas de garaje serán abiertas, no pudiendo cerrar, tapiar ni delimitar su respectiva plaza con elemento alguno, fijo o móvil. La única delimitación será la que se presenta en las rayas pintadas en el suelo.

Los titulares vienen obligados a cumplir las normas y disposiciones, que además de las previstas en el presente reglamento se acuerden en Junta General.

Artículo 9.- La comunidad no será en ningún caso responsable de los objetos depositados en el interior de los vehículos aparcados.

TÍTULO III.- CARGAS Y GASTOS. DISTRIBUCION DE LOS MISMOS

Artículo 10.- Los titulares de plazas de garaje o cuartos trasteros, vendrán obligados a contribuir a los gastos del condominio. Para la distribución de dichos gastos se atenderá a las cuotas de participación atribuidas a cada plaza o trastero.

Artículo 11.- Los gastos existentes serán los siguientes:

I- Los derivados de la participación atribuida a la totalidad del local subdividido en la Comunidad de vecinos del Inmueble, en la proporción conjunta establecida. Los gastos de conservación, utilización y reparación de la rampa de garaje, serán satisfechos por los propietarios de las plazas en la proporción que corresponda.

II- Los ordinarios que deriven de elementos comunes específicamente atribuidos a este condominio y causados por los servicios de mantenimiento del uso general y utilidad común.

III- Los extraordinarios que se produzcan por obras o reparaciones de carácter general y que hayan sido acordados por la Junta General.

Artículo 12.- Para el pago que corresponda a cada titular se establecerá una cuota anual en Junta General, la cual será pagadera por trimestres adelantados y quedará a resultas de la liquidación definitiva que se establecerá también anualmente. La efectividad de los pagos a efectuar por los titulares, quedará sujeto a la vigente Ley de Propiedad Horizontal.

TÍTULO IV.- GOBIERNO Y ADMINISTRACIÓN

Artículo 13.- La Comunidad estará regida:

- Por la Junta General

- Por la Comisión Permanente

- Por el Administrador-Secretario

Artículo 14.- La Junta General estará formada por los titulares de las plazas y trasteros, y se reunirá una vez al año para decidir la distribución y cuenta de gastos y su liquidación, así como para la resolución de cuantos asuntos de su competencia afecten a los intereses generales de la comunidad, y aparezcan fijados en el Orden del día correspondiente.

Artículo 15.- El cargo de Presidente tendrá vigencia anual, y será elegido de entre los titulares que constituyen la Junta General, pudiendo resultar reelegido. El Presidente representará a la Comunidad y tendrá voto de calidad parad decidir en las votaciones.

Artículo 16.- La Comisión Permanente, constituida por el Presidente, un vocal elegido por la junta, y el Administrador - Secretario, se reunirá cuantas veces se estime necesario y decidirá acerca de los asuntos ordinarios y de trámite de la Comunidad.

Artículo 17.- El Administrador - Secretario será el encargado de ejecutar los acuerdos de la Junta General y de la Comisión Permanente, y resolverá de acuerdo con los presentes estatutos o el Reglamento, los asuntos de trámite.

Las posibles quejas que tenga cualquier titular contra la comunidad o contra cualquier otro titular o usuario, por infracciones al presente reglamento, habrán de presentarse por escrito a la Administración, que queda facultada para resolver dichas quejas o para someter las mismas a la consideración de la junta general para su resolución. En caso de no alcanzarse un acuerdo se dirimirán ante los Tribunales competentes o mediante arbitraje

En todo lo no previsto en los presentes estatutos será de aplicación el artículo 396 del Código Civil y la vigente Ley de Propiedad Horizontal.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

========================================================================
