---
name: reglamento-regimen-interior-comunidad-propietarios-civ-0636
description: "Reglamento de régimen interior de una comunidad de propietarios. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Reglamento de régimen interior de una comunidad de propietarios

> Formulario **CIV-0636** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Reglamento de régimen interior de una comunidad de propietarios» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Reglamento de régimen interior de una comunidad de propietarios” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:reglamento-regimen-interior-comunidad-propietarios-civ-0636`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (5 veces)
- [ ] HORA (2 veces)
- [ ] LOCALIDAD
- [ ] NOMBRE DE LA CALLE
- [ ] NOMBRE DE LA COMUNIDAD

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

Capítulo I. DISPOSICIONES GENERALES
Capítulo II. DE LAS SANCIONES A IMPONER
Capítulo III. DE LAS NORMAS DE CONVIVENCIA
Capítulo IV. DEL USO DE ASCENSORES
Capítulo V. DEL SERVICIO DE PORTERÍA
Capítulo VI. DE LAS BASURAS
Capítulo VII. DE LAS VIVIENDAS Y LOCALES ARRENDADOS O CEDIDOS
REGLAMENTO DE RÉGIMEN INTERIOR DE LA COMUNIDAD [NOMBRE DE LA COMUNIDAD] SITA EN EL NÚMERO [Nº] DE LA CALLE [NOMBRE DE LA CALLE] DE [LOCALIDAD]

Capítulo I. DISPOSICIONES GENERALES

Artículo 1: Carácter obligatorio del Reglamento

El presente reglamento es de obligado cumplimiento. Los derechos y obligaciones de los Estatutos y de este Reglamento afectan de idéntica forma a los ocupantes de las viviendas y locales, sean propietarios, usufructuarios, arrendatarios o usuarios por cualquier título de ocupación, o bien por simple cesión oneroso o gratuita del propietario.

El Presidente, a través del Secretario Administrador, dará cuenta por escrito al propietario del piso de la decisión tomada en relación con la falta cometida por él, sus familiares, invitados y personas dependientes. Cuando el piso o local lo ocupen terceras personas, de las que tenga constancia la Comunidad, las comunicaciones se harán también igualmente a los usuarios.

Capítulo II. DE LAS SANCIONES A IMPONER

Artículo 2: Primera falta

La comisión de la primera falta a las normas de la Comunidad dará lugar a una amonestación simple.

Artículo 3: Segunda falta

La comisión de una segunda falta supondrá una segunda amonestación con la advertencia de que podrá ser privado, en la forma y tiempo que se establezca, de la utilización de servicios o elementos comunes.

Artículo 4: Tercera falta

La comisión de una tercera falta podrá dar lugar a la privación del derecho a utilizar elementos y servicios comunes, sin perjuicio de la decisión que al respecto pueda adoptarse en la Junta General e independientemente de la reparación económica de los daños ocasionados y de las acciones previstas en el artículo 19 de la Ley de Propiedad Horizontal.

Capítulo III. DE LAS NORMAS DE CONVIVENCIA

Artículo 5: Utilización incorrecta de servicios y elementos comunes

La utilización de los servicios y elementos comunes de forma contraria a su destino está completamente prohibida.

Además de las sanciones previstas en los artículos 2, 3 y 4, la rotura o deterioro de un elemento común, por uso indebido o contrario a su destino dará lugar a la exigencia económica del importe de la factura de reparación de dicho elemento común.

Artículo 6: Tendido de ropa

Queda prohibido el tendido de ropa en las terrazas principales de las viviendas, debiendo hacerse exclusivamente en los sitios destinados al efecto de cada piso y de forma tal que no produzca molestias a las viviendas inferiores.

Artículo 7: Toldos

Para la instalación de toldos en las terrazas exteriores, se deberá guardar una homogeneidad con el resto de los ya instalados, debiendo ser al menos, del mismo color, y en caso de que no hubiese instalado ninguno, deberá consultarse previamente a la Junta de Propietarios.

Artículo 8: Placas y distintivos profesionales

Los particulares que deseen colocar una placa identificativa de su actividad y domicilio, deberán adecuarse a las características de los ya existentes, a fin de lograr una unidad.

Artículo 9: Períodos de ausencia prolongados

Los vecinos que se ausentaren durante largo tiempo, dejarán las llaves de su vivienda a familiar o conocido de confianza, o al portero de la finca, para que, en caso de emergencia o fuerza mayor de carácter intempestivo, no sea preciso entrar a la misma por la fuerza.

Artículo 10: Actividades ruidosas y molestas

Queda prohibido desarrollar actividades que produzcan ruidos y molestias a los vecinos desde las 12 de la noche hasta las 10 de la mañana y de las [HORA] hasta las [Nº] horas (horario de siesta).

Capítulo IV. DEL USO DE ASCENSORES

Artículo 11: Condiciones técnicas

Cada bloque tiene unos elevadores, tanto de subida como de bajada, que deberán reunir en cada momento los requisitos que establezcan las normas legales correspondientes, además de las siguientes cuando no sean contradictorias con las primeras.

Artículo 12: Condiciones de uso

1. En ningún caso se podrá sobrepasar la capacidad indicada en cada uno de ellos, ni en peso total ni en número de personas, exigiéndose las responsabilidades correspondientes a que hubiera lugar en caso de uso abusivo de estos ascensores.

2. No podrán utilizar estos ascensores los menores de 14 años sin ir acompañados de personas mayores.

3. No se podrán transportar en ellos objetos, paquetes o bultos cuyo peso sobrepase el límite de capacidad o que por su tamaño y características sean susceptibles de causar daños o deterioros.

4. No podrá utilizarse los elevadores para transportes de materiales de obras y tampoco para hacer traslados de muebles. En ningún caso se podrá ocupar el ascensor de forma permanente o continuada, dejando sin servicio al resto de los vecinos.

Artículo 13: Cuidado y vigilancia de los ascensores

Del cuidado y vigilancia de los ascensores se encargará el Conserje, a los efectos de avisar a la Empresa de conservación, dando cuenta la Presidente y Administrador de la Comunidad de los problemas que puedan existir para la adopción de las medidas oportunas. Ningún propietario o inquilino podrá manipular en su mecanismo en caso de mal funcionamiento, debiendo avisar a dichos empleados y, en su caso, a la Empresa de mantenimiento.

Artículo 14: Conservación y mantenimiento de los ascensores

Para el buen cuidado de los ascensores y los debidos engrases periódicos se concertará el correspondiente contrato con una casa especializada en tal cometido.

Capítulo V. DEL SERVICIO DE PORTERÍA

Artículo 15: Dirección y control de los empleados

El poder de dirección y control de los empleados será ejercido por el Presidente. Queda prohibido todo tipo de discusión o queja directamente a los empleados, siendo el sistema el de dar cuenta al Presidente o Administrador del bloque.

Artículo 16: Horario de apertura del portal

El portal se abrirá a las [Nº] horas de la mañana y se cerrará a las [Nº] horas de la noche, permaneciendo durante este lapso de tiempo cerrado con llave a fin de evitar la entrada de personas ajenas a la finca. A estos efectos, cada vecino dispondrá de un juego de llaves del portal, así como una llave del cuarto de contadores.

Capítulo VI. DE LAS BASURAS

Artículo 17: Horarios de recogida

El horario de bajada de basuras individuales a los cubos existentes será de [HORA] a [Nº] horas. La basura se depositará en los contenedores comunes que se encuentran en el exterior del edificio, quedando prohibido su depósito en el patio interior del edificio.

Artículo 18: Condiciones de depósito de la basura

Las basuras individuales deberán ser bajadas siempre en bolsas de plástico cerradas u otro sistema similar, quedando prohibido utilizar otros recipientes que no reúnan las características de seguridad y cerramiento, depositándolas únicamente dentro de los cubos colectivos.

Capítulo VII. DE LAS VIVIENDAS Y LOCALES ARRENDADOS O CEDIDOS

Artículo 19: Comunicación de datos

Reiterando en su totalidad las obligaciones de los propietarios que vienen reflejadas en los Estatutos de la Comunidad, cada propietario estará obligado a dar cuenta al Presidente o Administrador de su bloque de la persona y demás datos del arrendamiento o cesionario del piso o local.

En esta comunicación, que el Presidente o Administrador del bloque trasladará a la Junta Directiva, el arrendatario o cesionario hará constar que conoce y acepta los Estatutos de la Comunidad, y este Reglamento de Régimen Interior, comprometiéndose a su cumplimiento, sin perjuicio de las acciones que, en su caso, deriven contra el propietario por la Comunidad.

Artículo 20: Responsabilidad

La Comunidad, a través de sus órganos representativos, podrá exigir a los ocupantes los daños y perjuicios ocasionados e imponer las sanciones previstas en este Reglamento, sin perjuicios de la responsabilidad directa del propietario conforme a lo previsto en los Estatutos y naturalmente ejercitar las acciones previstas en la Ley de Propiedad Horizontal, Código Civil y demás normas legales.

========================================================================
