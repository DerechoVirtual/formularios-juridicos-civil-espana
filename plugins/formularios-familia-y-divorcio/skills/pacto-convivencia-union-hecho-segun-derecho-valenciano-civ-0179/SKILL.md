---
name: pacto-convivencia-union-hecho-segun-derecho-valenciano-civ-0179
description: "Pacto de convivencia de una unión de hecho según el Derecho valenciano. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Pacto de convivencia de una unión de hecho según el Derecho valenciano

> Formulario **CIV-0179** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Pacto de convivencia de una unión de hecho según el Derecho valenciano» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Pacto de convivencia de una unión de hecho según el Derecho valenciano” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:pacto-convivencia-union-hecho-segun-derecho-valenciano-civ-0179`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NÚMERO (4 veces)
- [ ] MES (3 veces)
- [ ] PISO (3 veces)
- [ ] PUERTA (3 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] ESCALERA (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] DÍA
- [ ] NOMBRE DEL MENOR
- [ ] Nº
- [ ] PÁGINA
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

En la ciudad de [LOCALIDAD] a día [FECHA] de [MES] de 20 [AÑO]

REUNIDOS

De una parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, soltero, con domicilio en [LOCALIDAD], calle [CALLE], número [NÚMERO], escalera [ESCALERA], piso [PISO], puerta [PUERTA], y D.N.I. núm. [DNI/NIE]

Y de otra, D./Dª [NOMBRE Y APELLIDOS], mayor de edad, soltero, con domicilio en [LOCALIDAD], calle [CALLE], número [NÚMERO], escalera [ESCALERA], piso [PISO], puerta [PUERTA], y D.N.I. núm. [DNI/NIE]

Ambos se encuentran vinculados entre sí por relación de pareja de hecho inscrita en el Registro administrativo de uniones de hecho de la Comunidad Valenciana en fecha [FECHA] de [MES] de

INTERVIENEN

Ambas partes concurren en su propio nombre y derecho, reconociéndose mutuamente la capacidad legal necesaria para acordar el presente PACTO DE CONVIVENCIA FAMILIAR, de conformidad con la Ley 5/2011, de 1 de abril, de la Generalitat, de Relaciones Familiares de los hijos e hijas cuyos progenitores no conviven. A tal efecto,

EXPONEN:

Unión de hecho e hijos

D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS] han convivido como pareja estable de hecho durante [Nº] años, encontrándose inscrita su unión en el Registro administrativo de uniones de hecho de la Comunidad Valenciana

De dicha unión ha nacido y vive un hijo/a, llamado/a [NOMBRE DEL MENOR], nacido en [LOCALIDAD] el día [DÍA] de [MES] de [AÑO], según consta igualmente inscrito en el Registro Civil de [LOCALIDAD], al Tomo [TOMO], Página [PÁGINA] Dicho hijo/a tiene vecindad civil valenciana por haber nacido de padres con dicha vecindad civil (cfr. art. 14.2 del Código civil).

Domicilio familiar

La vivienda que ha constituido el domicilio familiar se encuentra en Valencia, número [NÚMERO], piso [PISO], puerta [PUERTA]

Ruptura de la unión

Los convivientes han decidido poner fin a su unión y con el fin de regular los efectos de su ruptura, acuerdan el presente PACTO DE CONVIVENCIA FAMILIAR, conforme a las siguientes

ESTIPULACIONES

[ELEGIR UNA OPCIÓN: Patria potestad, guarda y custodia / Guarda y custodia individual / Guarda y custodia compartida]

Régimen mínimo de relación del hijo/a menor con los abuelos

En la actualidad, el/la menor sólo cuenta con su abuela paterna y su abuela materna [NOMBRE Y APELLIDOS], por haber fallecido ya sus abuelos paterno y materno.

Si el menor no asiste al comedor escolar, podrá ser recogido a mediodía por su abuela paterna [NOMBRE Y APELLIDOS], como ha venido siendo habitual hasta la fecha, y comerá en su domicilio y compañía. Su abuela paterna [NOMBRE Y APELLIDOS], se encargará de devolverlo al Colegio para las clases de la tarde. Si su abuela paterna [NOMBRE Y APELLIDOS] se encontrara impedida para recoger al menor y comer con él, se encargará de hacerlo el progenitor custodio.

En cualquier caso cada una/o de las abuelas/os del /de la menor, tendrán derecho a relacionarse con el mismo, pudiendo pasar, al menos, una tarde cada quince días en su compañía -que será disfrutada de modo conjunto por el abuelo y abuela paternos, por un lado, y por el abuelo y abuelo materno por otro, de ser ello posible y no interferir en el régimen de convivencia existente entre los propios abuelos (este último inciso no procede si no están vivos los dos miembros de cada una de las parejas -paterna y materna- de abuelos)-. Dicha tarde comprenderá, al menos, un periodo de tres horas ininterrumpidas.

[ELEGIR UNA OPCIÓN: Régimen mínimo de relación de los hijos menores con los hermanos / Régimen mínimo de relación del hijo/a menor con los hermanos / Caso de que no tenga hermanos / Caso de hermanos mayores de edad de vida independiente / Caso de hermanos de vínculo sencillo -modalidad 1ª- / Caso de hermanos de vínculo sencillo -modalidad 2ª- / — y además elegir: Régimen mínimo de relación de los hijos menores con otros parientes o allegados / Régimen mínimo de relación del hijo/a menor con otros parientes o allegados / Caso de custodia compartida / Caso de custodia individual]

Atribución del uso de la vivienda familiar y del ajuar doméstico

Además de la vivienda familiar, los convivientes no han hecho uso de otra vivienda en el ámbito familiar con regularidad (si hubieran hecho uso de otra vivienda en el ámbito familiar, por ejemplo, por razones laborales, habrían de pactar, igualmente, el régimen de atribución de su uso, con independencia de su titularidad; quedan excluidas de esta necesidad las viviendas de temporada que se disfruten como segundas o ulteriores residencias).

Se atribuye el uso de la vivienda que ha sido familiar, y de la que ambos convivientes son copropietarios, a D./Dª [NOMBRE Y APELLIDOS], progenitor custodio, y al/a la hijo/a hasta que éste alcance la mayoría de edad, por aconsejarlo así el interés de éste. Aquél se hará cargo de los gastos de comunidad, luz, agua, gas y otros similares. Se atribuye igualmente a D./Dª [NOMBRE Y APELLIDOS] el uso del ajuar doméstico mientras tenga el de la vivienda habitual, sin perjuicio de que el otro conviviente, D./Dª [NOMBRE Y APELLIDOS], pueda retirar de ésta sus objetos de uso personal.

De acuerdo con el art. 6.1 de la Ley valenciana 5/2011, de 1 de abril, D./Dª [NOMBRE Y APELLIDOS], cotitular de la vivienda familiar, a quien no se le ha atribuido su uso, tiene derecho a una compensación económica, que se fija en [IMPORTE] euros ( €). La misma se computará como contribución de dicho cónyuge a los gastos de mantenimiento del hijo/a.

[ELEGIR UNA OPCIÓN: Contribución a los gastos del/de los menor/menores / Contribución a los gastos del/de los menor/es / Caso de guarda y custodia individual / Caso de guarda y custodia compartida]

Pensión de alimentos en favor de hijos mayores de edad (para el caso de que los hubiera)

Los convivientes establecen como pensión de alimentos a favor de su hijo/a mayor de edad, la suma de [IMPORTE] EUROS ( euros) mensuales, pagaderos por mensualidades anticipadas dentro de los cinco primeros días de cada mes en la cuenta bancaria nº [NÚMERO], de la que es titular el hijo/a, cuya cantidad será actualizada anualmente conforme a la variación que experimente el Índice General Nacional del Sistema de Índices de Precios al Consumo. Dicha pensión se establece por no contar el/la hijo/a con ingresos propios y encontrarse todavía en periodo de formación, viviendo en casa de su madre (o padre) y será satisfecha mientras el/la hijo/a no finalice su formación por causa que no le sea imputable y carezca de medios de vida propios, conforme a lo establecido en los arts. 142 y ss. del Código civil.

Aprobación judicial

La presente propuesta de Pacto de Convivencia Familiar, se someterá a la preceptiva aprobación judicial, obligándose cada uno de los convivientes a ratificarlo en presencia judicial.

Y en prueba de conformidad con todo lo acordado firman los comparecientes en el lugar y fecha arriba indicados.

Firmas de las partes:

========================================================================
