---
name: demanda-modificacion-medidas-modificacion-provisional-civ-0172
description: "Demanda de modificación de medidas con modificación provisional y supresión de alimentos (Cataluña). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de modificación de medidas con modificación provisional y supresión de alimentos (Cataluña)

> Formulario **CIV-0172** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Antecedentes: Tribunal y procedimiento Al Tribunal Procurador, representación Asistencia letrada, acción que se ejercita HECHOS FUNDAMENTOS DE DERECHO Suplico Otrosí solicitando suspensión provisional de la obligación de prestar alimentos Segundo Otrosí solicitando prueba anticipada Firmas

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de modificación de medidas con modificación provisional y supresión de alimentos (Cataluña)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de modificación de medidas con modificación provisional y supresión de alimentos (Cataluña)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-modificacion-medidas-modificacion-provisional-civ-0172`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] CALLE (3 veces)
- [ ] AÑO (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] COLEGIO
- [ ] DNI/NIE
- [ ] DÍA
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] NOMBRE DEL HIJO
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO DE LA CALLE
- [ ] SEDE

## Normas que cita el formulario

- art. 775.1 LEC
- art. 775 LEC
- art. 770 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 394 LEC

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

- Junto a «…Antecedentes: Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…CIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

Antecedentes:

Tribunal de Instancia de [SEDE], plaza n.º [Nº]

Procedimiento de divorcio/separación de mutuo acuerdo/contencioso: /

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], comparezco en este TRIBUNAL y como mejor proceda en Derecho DIGO:

Que mediante el presente escrito, y con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], formulo demanda de modificación de medidas definitivas contra D./Dª [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., en base al artículo 237.7, apartado 1, del Código civil de Cataluña, en relación con el artículo 775.1 de la LEC y ello en base a los siguientes:

HECHOS

Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS] formularon demanda de divorcio de mutuo acuerdo que correspondió al Tribunal al que me dirijo y que se siguió como procedimiento núm. [Nº DE PROCEDIMIENTO]/[AÑO]

El mencionado procedimiento finalizó por sentencia en la que se decretó la disolución por divorcio del matrimonio y se homologaron las medidas propuestas en el convenio regulador aportado por los solicitantes.

Adjunto aportamos como DOCUMENTO NÚM. UNO copia testimoniada de la citada sentencia.

En concreto se acordó (y se homologó judicialmente) que el padre, como progenitor no custodio, tendría que abonar en concepto de pensión de alimentos a favor del hijo del matrimonio, la suma de 600 € mensuales, incrementándose con arreglo a las variaciones del IPC, y los gastos extraordinarios por mitad, tal y como consta en el convenio que obra en el documento acompañado bajo el numero uno.

El hijo del matrimonio [NOMBRE DEL HIJO], que actualmente cuenta con 24 años de edad, ha sido contratado por tiempo indefinido por la entidad BBVA, trabajando como cajero en la sucursal de dicha entidad sita en [LOCALIDAD], en la calle [CALLE], nº [NÚMERO DE LA CALLE]

Asimismo, el hijo ha trasladado su domicilio, junto con su novia a un piso de alquiler en la calle [CALLE], nº [NÚMERO], de [LOCALIDAD]

A los anteriores hechos les son de aplicación los siguientes:

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

Competencia

Es competente el Tribunal al que me dirijo al solicitarse la modificación de una de las medidas adoptadas en el procedimiento de divorcio seguido ante el mismo, al amparo del art. 775 de la LEC.

Procedimiento

Deberá seguirse la demanda, al amparo del artículo 775 de la LEC, por los cauces del juicio verbal, con las especialidades previstas en el artículo 770 de la LEC.

Legitimación

Está legitimado activamente mi mandante, y pasivamente la demandada.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Fondo del asunto

El artículo 237.13.1. d) del Código civil de Cataluña prevé que la obligación de prestar alimentos se extingue por la mejora de las condiciones de vida del alimentado, de modo que haga innecesaria la prestación.

Es evidente, y se acreditará en juicio, que el alimentista ha devenido a mejor fortuna, habiendo quedado sin efecto la causa que determinó la prestación por alimentos.

Costas

Deberán imponerse a la demandada si se opone a la demanda al amparo del art. 394 de la LEC.

Por lo expuesto:

SUPLICO AL TRIBUNAL tenga por presentado este escrito, junto con los documentos que se acompañan, lo admita, me tenga por parte en la representación que otorgada por D./Dª [NOMBRE Y APELLIDOS], asumo, entendiéndose conmigo las sucesivas actuaciones, y previo traslado de la demanda a la demandada y celebración de juicio verbal, se dicte sentencia por la que se modifique la medida relativas a la prestación de alimentos acordando la extinción de la obligación de prestarlos.

PRIMER OTROSÍ DIGO que al amparo del artículo 775 de la LEC, y previa la comparecencia prevista en el artículo 773 en relación con el 771 del mismo cuerpo legal, SUPLICO AL TRIBUNAL dicte auto por el que deje sin efecto provisionalmente, hasta que se dicte sentencia, la obligación de abonar la prestación alimenticia acordada.

SEGUNDO OTROSÍ DIGO que con el carácter de prueba anticipada SUPLICO AL TRIBUNAL que por el Letrado de la Administración de Justicia se libre atento oficio a la TESORERÍA GENERAL DE LA SEGURIDAD SOCIAL para que se informe de la vida laboral de [NOMBRE Y APELLIDOS], con DNI nº [DNI/NIE], sin perjuicio de volver a solicitar la práctica de la prueba en el momento procesal oportuno o de ampliar los medios ya solicitados.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
