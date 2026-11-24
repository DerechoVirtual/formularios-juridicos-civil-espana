---
name: demanda-medidas-paterno-filiales-tras-sentencia-civ-0121
description: "Demanda de medidas paterno-filiales tras la sentencia que declara la filiación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de medidas paterno-filiales tras la sentencia que declara la filiación

> Formulario **CIV-0121** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de medidas paterno-filiales tras la sentencia que declara la filiación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de medidas paterno-filiales tras la sentencia que declara la filiación” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-medidas-paterno-filiales-tras-sentencia-civ-0121`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] NOMBRE DEL MENOR (3 veces)
- [ ] FECHA (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] COLEGIO
- [ ] DNI/NIE
- [ ] DÍA
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 85.1 LOPJ
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales en nombre y representación de Dña. [NOMBRE Y APELLIDOS], mayor de edad, soltera, con DNI [DNI/NIE] y domicilio a efectos de notificaciones en la calle [CALLE], sita en [LOCALIDAD], cuya representación procesal acreditaré el día que se determine mediante comparecencia apud acta ante el Letrado/a de la Administración de Justicia competente para conocer de este proceso, bajo la dirección técnica de D./Dña. [NOMBRE Y APELLIDOS], Abogado/a del Ilustre Colegio de Abogados de [COLEGIO], Colegiado núm. [Nº], ante este Tribunal comparezco y, como mejor proceda en Derecho y

DIGO

Que mediante el presente escrito y siguiendo instrucciones de mi mandante formulo demanda en solicitud de medidas paterno-filiales acordes con lo dispuesto en el fallo de la sentencia de fecha [FECHA], en la que se reconoce la filiación extramatrimonial del demandado [NOMBRE Y APELLIDOS], respecto de la menor [NOMBRE DEL MENOR], con arreglo a lo que a su derecho conviene de conformidad con lo dispuesto en el artículo 730 de la Ley de Enjuiciamiento Civil, lo que baso en los siguientes

HECHOS

Mi mandante mantuvo relaciones afectivas y de convivencia con D. [NOMBRE Y APELLIDOS], durante tres años, según consta en la certificación de empadronamiento que se aporta para su debida acreditación como documento núm.1.

Fruto de esa relación nació la menor de 6 años en la actualidad [NOMBRE DEL MENOR], que D. se negó a reconocer en su día como suya por los motivos que se acreditan en las cartas remitidas por él a mi representada y que se aportan como prueba como documentos núms. 2, 3 y 4.

Ante la injustificada negativa de mi representada decidió formular demanda de reclamación de filiación no matrimonial, que finalizó con sentencia firme de fecha [FECHA], que falló a su favor reconociendo la paternidad del demandado respecto de la menor, que se aporta como documento núm. 5.

Desde dicho fallo no se ha procedido a satisfacer por el demandado pensión de alimentos alguna a favor de la menor, a pesar de tener un trabajo estable como comercial bien remunerado, siendo ésta una medida necesaria, atendidos los escasos recursos con que mi representada cuenta en la actualidad, para garantizar el debido bienestar de la menor, razón por la cual se presenta este escrito.

A los anteriores hechos son de aplicación los siguientes

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

COMPETENCIA JURISDICCIONAL: La competencia objetiva: Es de aplicación el párrafo 3º del artículo 117 de la Constitución española, que asigna exclusivamente a los Juzgados y Tribunales determinados por las Leyes, el ejercicio de la potestad jurisdiccional en todo tipo de procesos, juzgando y haciendo ejecutar lo juzgado. Para la competencia territorial con carácter general hay que atenerse a lo dispuesto en el artículo 769.3 de la Ley de Enjuiciamiento Civil, en relación con lo dispuesto en el art. 85.1º LOPJ, que hace referencia al Tribunal de Instancia del lugar del último domicilio común de los progenitores.

CAPACIDAD Y LEGITIMACIÓN DE LAS PARTES: Tanto mi representada como el demandado se encuentran en pleno ejercicio de sus derechos civiles y no están incursos en causa de incapacitación alguna, por lo que tienen la capacidad procesal establecida en los arts. 6.1 y 7.1 de la Ley de Enjuiciamiento Civil. Estando legitimado mi mandante para llevar a cabo dicha acción, por tener interés legítimo de conformidad con lo establecido en el art. 768.2 de la Ley de Enjuiciamiento Civil en tanto determina que "reclamada judicialmente la filiación, el tribunal podrá acordar alimentos provisionales a cargo del demandado y, en su caso, adoptar las medidas de protección a que se refiere el apartado anterior".

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

DERECHO SUSTANTIVO: Se atenderá a lo establecido en el art. 108 y siguientes de la Ley de Enjuiciamiento Civil que alude a los efectos de la filiación matrimonial y no matrimonial, como es el caso, que ha venido determinada legalmente por sentencia firme. En este sentido, tal como determina el art. 110 "el padre y la madre, aunque no ostenten la patria potestad, están obligados a velar por los hijos menores y a prestarles alimentos".

PROCEDIMIENTO: El procedimiento aplicable seguirá lo dispuesto en los arts. 753 y siguientes de la Ley de Enjuiciamiento Civil, que determina que se sustanciarán por los trámites del juicio verbal.

Por todo lo cual,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito de solicitud de medidas de orden patrimonial así como los documentos que lo acompañan y copias de todo ello y se sirva admitirlos, teniéndome por personado y parte en la representación acreditada, y previos los trámites legales oportunos, se digne admitirla y dicte auto por el que se acuerde la medida de otorgar alimentos a favor de la menor [NOMBRE DEL MENOR], por parte de D. [NOMBRE Y APELLIDOS], en la cuantía de [IMPORTE] euros pagaderos los primeros días de cada mes y actualizables conforme al índice de precios al consumo publicado, y una vez firme disponga el desglose de los documentos presentados.

Es justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo. Procurador/a

D./Dña. [NOMBRE Y APELLIDOS]

Fdo. Letrado/a

D./Dña. [NOMBRE Y APELLIDOS]

========================================================================
