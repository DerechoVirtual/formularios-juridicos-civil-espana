---
name: contestacion-demandado-como-padre-demanda-filiacion-no-civ-0370
description: "Contestación del demandado como padre a la demanda de filiación no matrimonial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación del demandado como padre a la demanda de filiación no matrimonial

> Formulario **CIV-0370** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito de contestación a la demanda sobre reclamación de filiación no matrimonial, por parte del demandado en condición del padre del menor.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación del demandado como padre a la demanda de filiación no matrimonial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación del demandado como padre a la demanda de filiación no matrimonial” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-demandado-como-padre-demanda-filiacion-no-civ-0370`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] FECHA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 23 LEC
- art. 767 LEC

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

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…2666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], con D.N.I. n.º [NÚMERO], como demuestro mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], habiendo sido demandado en el juicio de filiación seguido en ese Tribunal bajo número [NÚMERO]/[AÑO], a instancias de D./Dña. [NOMBRE Y APELLIDOS], en representación legal de su hijo menor [NOMBRE Y APELLIDOS], comparezco y como mejor en Derecho proceda, DIGO:

Por Decreto/Auto de fecha [FECHA] de los corrientes se le dio traslado del escrito de demanda y emplazó a mi mandante para personación dentro del emplazamiento notificado, por lo que en tiempo y forma se viene a evacuar CONTESTACIÓN a la demanda, con base en los siguientes datos y razonamientos:

HECHOS

PRIMERO.- En lo que refiere la demanda, en sus ordinales segundo, tercero y cuarto, a las circunstancias objetivas del empleo y matrimonio de mi patrocinado, y a la calidad de hijo de la demandante, no cabe más que prestar conformidad, y también a que ha existido un rotundo rechazo, como se documenta, en asumir por esta parte la paternidad que se le pide (si bien, lejos de lo que se asevera en la demanda, las pretensiones económicas no han sido ni mucho menos desdeñadas en este asunto).

SEGUNDO.- Por lo que toca a la convivencia entre mi patrocinado y D./Dña. [NOMBRE Y APELLIDOS], tanto por su origen, contenido y finalización, es menester discrepar en el siguiente sentido:

Mi patrocinado, al acceder a su primer destino profesional, en [LOCALIDAD], por razón de la carencia de familia y la necesidad de ahorro del gasto, como es tan habitual entre funcionarios jóvenes desplazados de su lugar de origen o siquiera del destino que prevén más duradero, compartió arrendamiento de un piso céntrico y grande con otras personas, ciñéndose la comunidad al pago de la renta, siendo una de tales personas la demandante.

Con el tiempo, fueron marchando los demás co-arrendatarios, y quedaron solos mi patrocinado y D./Dña. [NOMBRE Y APELLIDOS], habiéndose trabado entre ellos una íntima amistad, según se ha de reconocer, pero no hubo ninguna relación de las que naturalmente son hábiles para procrear un hijo en tiempo compatible con la concepción del hijo de la actora.

El dato de que se abriera una cuenta mancomunda en entidad de crédito para el pago de la renta y consumos normales de la vivienda, o que se solicitara un préstamo de consuno para adquirir cierto mobiliario, nada tuvo qué ver con que entre D./Dña. [NOMBRE Y APELLIDOS] y mi patrocinado haya existido convivencia ‘more uxorio’.

FUNDAMENTOS DE DERECHO

I.- De conformidad con la competencia del Tribunal, procedimiento, capacidad y legitimaciones puramente procesales de los litigantes.

Comparece esta parte cumpliendo los requisitos de postulación de representación técnica y asistencia letrada, de los arts. 23, 31 y 750 LEC.

II.- En cuanto al fondo del asunto, puesto que la verdad material de la procreación no tiene valladar en el actual régimen para que se investigue por la Jurisdicción, se trata de que, sin que concurran datos indiciarios de que presumir la filiación reclamada, y por supuesto que la prueba del hecho negativo es imposible para esta parte, se intente la demostración del normal hecho constitutivo, por la comunidad de mensaje genético del cuerpo de mi mandante y del hijo de la actora, a través de la prueba pericial biológica de que habla el art. 767 LEC.

No siendo factible encontrar tal comunidad genética, y estando fijada en grado elevadísimo la fiabilidad de dicha prueba científica, ningún obstáculo se interpondrá a su práctica.

Por esta parte no puede más que negarse la procreación, y aseverar el alejamiento físico de quienes coincidieron durante un tiempo y mantuvieron amistad y confianza, ahora sorprendida, que se produjo sin el más mínimo problema, pero también sin la más mínima noticia de que D./Dña. [NOMBRE Y APELLIDOS], la demandante, pudiera haber quedado embarazada. Nunca ha habido, por otro lado, ulterior contacto, hasta la noticia de esta pretendida paternidad.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, se digne admitirlo y tenerme por personado y parte en la representación que ostento, entendiéndose conmigo todas las sucesivas diligencias del proceso, y por contestada en términos de total oposición la demanda, y siguiéndose el proceso por todos sus trámites, se venga a dictar sentencia que desestime cuantos pedimentos se deducen en el escrito de demanda, absolviendo libremente a esta parte, con condena en costas a la actora.

Es de Justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
