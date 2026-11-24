---
name: demanda-resolucion-arrendamiento-vivienda-necesidad-civ-0534
description: "Demanda de resolución de arrendamiento de vivienda por necesidad del arrendador (posterior a 1995). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de resolución de arrendamiento de vivienda por necesidad del arrendador (posterior a 1995)

> Formulario **CIV-0534** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario por la que el arrendador pide que se declare resuelto un contrato de arrendamiento de vivienda (posterior al 1 de enero de 1995) porque necesita la vivienda para destinarla a vivienda permanente propia, de sus familiares en primer grado de consanguinidad o por adopción, o de su cónyuge en los supuestos de sentencia firme de separación, divorcio o nulidad, causa que debió constar expresamente en el contrato (art. 9.3 LAU, en la redacción vigente para contratos anteriores a la Ley 4/2013). Véanse las notas de ayuda finales.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de resolución de arrendamiento de vivienda por necesidad del arrendador (posterior a 1995)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de resolución de arrendamiento de vivienda por necesidad del arrendador (posterior a 1995)” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-resolucion-arrendamiento-vivienda-necesidad-civ-0534`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (7 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] AÑO
- [ ] DOMICILIO DE LA VIVIENDA
- [ ] DÍA
- [ ] FECHAS
- [ ] IMPORTE EN LETRA
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] SEDE

## Normas que cita el formulario

- art. 21.1 LOPJ
- art. 36.1 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 52.1.7.º LEC
- art. 249.1.6.º LEC
- art. 10 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 23 LEC
- art. 399 LEC
- art. 399.3 LEC
- art. 5 Ley Orgánica 1/2025
- art. 9.1 Ley 29/1994
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…los supuestos de sentencia firme de separación, divorcio o nulidad matrimonial».»: la redacción transcrita del art. 9.3 LAU es la anterior a la Ley 4/2013, de 4 de junio, y solo se aplica a los contratos celebrados antes de su entrada en vigor; comprobar la redacción aplicable al contrato concreto y sus disposiciones transitorias.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº], dirigido por el Letrado/a abajo firmante D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], con despacho profesional en [DOMICILIO], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que, mediante el presente escrito y en nombre de mi mandante, formulo demanda de juicio declarativo ordinario sobre resolución de contrato de arrendamiento de la vivienda sita en [DOMICILIO DE LA VIVIENDA] contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], haciendo constar los siguientes

HECHOS

PRIMERO.– Mi mandante es propietario/a de la vivienda sita en [LOCALIDAD], calle [DOMICILIO]. Se acompaña el título correspondiente como documento n.º [Nº].

SEGUNDO.– Entre el demandado D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO] y mi representado se convino un contrato de arrendamiento respecto de la indicada vivienda en fecha [FECHA]. Se adjunta como documento n.º [Nº] el contrato privado de arrendamiento de inmueble urbano con destino a vivienda, siendo la renta inicialmente convenida la de [IMPORTE] euros mensuales.

TERCERO.– Debido a [CAUSA: p. ej., un cambio eventual de puesto de trabajo y traslado de domicilio de mi representado a la localidad de [LOCALIDAD]], en el contrato de arrendamiento celebrado se hizo constar expresamente en la cláusula [Nº] la improcedencia de la prórroga obligatoria si, una vez transcurrido el primer año, el arrendador tuviera necesidad de la vivienda arrendada para destinarla a vivienda permanente, por razón de [SU REGRESO A ESTA CIUDAD / LA NECESIDAD DE SUS FAMILIARES DE PRIMER GRADO / LA NECESIDAD DE SU CÓNYUGE TRAS SENTENCIA FIRME DE SEPARACIÓN, DIVORCIO O NULIDAD].

CUARTO.– En fecha [FECHA] el actor requirió al inquilino, de forma fehaciente, haciéndole saber la necesidad de ocupar la vivienda para sí, así como la causa de dicha necesidad y la no existencia de otra vivienda propiedad del actor en la misma localidad, y, al objeto de dejar constancia fehaciente, por requerimiento notarial notificó al demandado la necesidad de ocupar la vivienda para sí, sin que el inquilino haya abandonado la misma, no dejando más alternativa a esta parte que la vía judicial. Se aporta copia del requerimiento notarial no atendido por el demandado como documento n.º [Nº].

QUINTO.– La parte actora manifiesta que, previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria, incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento n.º [Nº] el requerimiento efectuado y como documento n.º [Nº] la contestación del demandado.

FUNDAMENTOS DE DERECHO

I.– JURISDICCIÓN Y COMPETENCIA.

La jurisdicción ordinaria es la única competente para el conocimiento de los juicios que se susciten en territorio español con arreglo a lo establecido en los tratados y convenios internacionales en los que España sea parte, en las normas de la Unión Europea y en las leyes españolas (art. 21.1 LOPJ y art. 36.1 LEC).

La competencia objetiva corresponde a la Sección Civil del Tribunal de Instancia según lo dispuesto en el art. 85.1 LOPJ y art. 45 LEC, así como la territorial con arreglo al art. 52.1.7.º LEC, puesto que el Tribunal competente es el del lugar en que está sita la finca.

II.– PROCEDIMIENTO.

El art. 249.1.6.º LEC dice que se decidirá en juicio ordinario las demandas que versen sobre cualesquiera asuntos relativos a arrendamientos urbanos, salvo excepciones que no comprenden el presente supuesto.

III.– LEGITIMACIÓN ACTIVA Y PASIVA.

La legitimación corresponde a mi poderdante activamente como propietario de la vivienda y al demandado corresponde pasivamente como arrendatario de la misma (art. 10 LEC).

IV.– CUANTÍA.

Conforme al art. 253.1 LEC cifro la cuantía de la presente demanda en [IMPORTE EN LETRA] euros ([IMPORTE] €), importe de una anualidad de renta, según resulta de la regla 9.ª del art. 251 LEC.

V.– POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23 y 31 LEC se formula esta demanda por medio de Procurador/a con poder para pleitos y con dirección y firma de Letrado/a habilitado/a. Asimismo se cumplen los requisitos formales del art. 399 LEC.

VI.– CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por el art. 264.4.º y el art. 399.3 de la LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.– FUNDAMENTOS DE DERECHO MATERIALES O SOBRE EL FONDO DEL ASUNTO.

El art. 9.1 de la Ley 29/1994, de 24 de noviembre, de Arrendamientos Urbanos, establece para los arrendamientos de vivienda un régimen de prórroga forzosa a voluntad del arrendatario por plazos anuales hasta alcanzar los cinco años, o siete años si el arrendador fuese persona jurídica, disponiendo el art. 9.3 de dicha Ley que «una vez transcurrido el primer año de duración del contrato y siempre que el arrendador sea persona física, no procederá la prórroga obligatoria del contrato cuando, al tiempo de su celebración, se hubiese hecho constar en el mismo, de forma expresa, la necesidad para el arrendador de ocupar la vivienda arrendada antes del transcurso de cinco años para destinarla a vivienda permanente para sí o sus familiares en primer grado de consanguinidad o por adopción o para su cónyuge en los supuestos de sentencia firme de separación, divorcio o nulidad matrimonial».

VIII.– COSTAS.

Conforme al art. 394 LEC, las costas del procedimiento habrán de imponerse al demandado.

Por lo expuesto,

SUPLICO AL TRIBUNAL que, teniendo por presentado este escrito de demanda junto con los documentos que se acompañan y copias de todo ello, se sirva admitirlo a trámite, me tenga por comparecido y parte demandante y por formulada la demanda de juicio ordinario contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], acordando conferir traslado de la misma a dicho demandado, emplazándole para que comparezca y la conteste, y, seguido el juicio por sus trámites, se dicte sentencia por la que, estimando íntegramente la demanda, se declare la resolución del contrato de arrendamiento de la vivienda descrita, condenando al demandado a que desaloje la misma, bajo apercibimiento de ser lanzado, con expresa imposición de costas procesales.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a

NOTAS DE AYUDA

1. Si se pacta un plazo determinado de vigencia del contrato sin que el arrendatario tenga derecho a prórrogas obligatorias hasta los cinco años (en la redacción de la ley vigente antes de la Ley 4/2013), se estaría ejercitando una acción de resolución de contrato por expiración del plazo contractual, que seguiría el cauce del juicio verbal y permitiría, en su caso, acumular la reclamación de rentas atrasadas. Pero si lo que se deniega es una prórroga porque no se pudo concretar el momento en que volvería a necesitar el arrendador la vivienda, no estaríamos ante una resolución por expiración del plazo contractual, sino ante una extinción del contrato por denegación de prórroga y, en rigor, habría que acudir al juicio ordinario. Este modelo recoge ese segundo supuesto (denegación de la prórroga sucesiva, una vez cumplida la duración inicial del contrato pero antes de los cinco años, cuando se cumpla la condición, no determinada en fecha [FECHA], de necesidad de la vivienda).

2. Si, transcurridos tres meses desde la extinción del contrato, el arrendador no hubiera ocupado la vivienda personalmente, deberá, a elección del arrendatario, o reponerle en el uso y disfrute de la misma por un nuevo periodo de hasta cinco años, con indemnización por los gastos que causó el desalojo hasta el momento de la reocupación, o indemnizarle con una cantidad igual al importe de la renta por los años que quedasen hasta completar cinco, salvo que la ocupación no pudiera tener lugar por causa de fuerza mayor.

3. Tras la reforma operada por la Ley 4/2013 ha cambiado sustancialmente esta posibilidad del arrendador de reclamar para sí el uso de la vivienda.
