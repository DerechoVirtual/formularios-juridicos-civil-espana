---
name: oposicion-coejecutados-deudor-solidario-suceda-como-civ-1028
description: "Oposición de los coejecutados a que el deudor solidario suceda como ejecutante en el proceso. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición de los coejecutados a que el deudor solidario suceda como ejecutante en el proceso

> Formulario **CIV-1028** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito de las partes coejecutadas oponiéndose a la sucesión procesal del ejecutado en posición de parte ejecutante.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición de los coejecutados a que el deudor solidario suceda como ejecutante en el proceso» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición de los coejecutados a que el deudor solidario suceda como ejecutante en el proceso” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:oposicion-coejecutados-deudor-solidario-suceda-como-civ-1028`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] FECHA
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 1.844 CC
- art. 1.839 CC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, que representa a y [NOMBRE Y APELLIDOS], a virtud de sendas certificaciones del Registro Electrónico de Apoderamientos Judiciales que se acompañan como documentos números [Nº DE DOCUMENTO], en su carácter de partes ejecutadas en el presente proceso, que se sigue en el Tribunal como Ejecución de Título Extrajudicial n.º [Nº]/[AÑO], ante el Tribunal comparezco y en la forma que en Derecho mejor proceda, DIGO:

PRIMERO

[NOMBRE Y APELLIDOS], que resultaba avalista solidario de la deuda por préstamo que se concertó en póliza de operaciones mercantiles con el [ENTIDAD BANCARIA], para el giro del negocio de la empresa de [ACTIVIDAD], por razón de resultar aquél y mis mandantes socios de la misma, miembros de consejo de administración, al parecer, ha pagado al Banco las cantidades que éste exigiera en el presente proceso, mas ello no significa la viabilidad de que, a su vez, utilice contra mis mandantes el proceso ejecutivo en el estado en que se halla, sin que quepa admitir una sucesión procesal frente a tales.

SEGUNDO

El régimen jurídico aplicable a la fianza solidaria es controvertido doctrinalmente, ya que existen opiniones diversas respecto del grado de sujeción al régimen de las obligaciones solidarias en detrimento del de la fianza general o viceversa, y haciéndolo depender de si se aplica a las relaciones internas fiador-deudor principal o también externas, o de los tipos de fianzas solidarias, las que han tenido reflejo en la jurisprudencia.

En cualquier caso, existiendo una confianza en la que los ejecutados [NOMBRE Y APELLIDOS], [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS] se vincularon solidariamente como cofiadores con el deudor principal y entre sí (estipulación 11.ª de la póliza de préstamo), deriva que los cofiadores que hayan pagado la deuda puedan reclamar de cada uno de los demás la parte que proporcionalmente les corresponda satisfacer conforme al art. 1.844 CCiv, en coincidencia con el régimen del art. 1.145, más ello no equivale a que se subrogue en el crédito el deudor solidario.

TERCERO

Una cosa es el crédito del Banco frente a deudores solidarios, y otra el crédito del cofiador solidario que paga al acreedor frente al resto de cofiadores, que no está en el art. 1.839 CCiv, ni dimana de la naturaleza de la fianza como negocio de garantía, y ni siquiera es el mismo, ya que hay que descontar la proporción de la deuda que corresponde al codeudor que pagó.

Téngase en cuenta el requisito de subsidiariedad como la limitación de la subrogatoria ex art. 1.844, párrafo 3.º CCiv, para los supuestos de pago extrajudicial del cogarante, al margen de los codeudores.

CUARTO

Pero es que el título ejecutivo es un acto documentado que tiene la virtualidad de hacer llevar a la realidad física la conducta sustitutiva de la prestación debida por imperio estatal, privilegio procesal que detentaba el [ENTIDAD BANCARIA], y que desaparece con la satisfacción de su objeto, como ha sido caso. El derecho del cofiador no tiene título ejecutivo, y no puede suceder a quien lo tiene en el proceso de ejecución.

Por otro lado, traspasado el plazo legal para oponerse esta parte al despacho de ejecución con relación a una persona, la sucesión procesal impediría oponerse ya a la ejecución que beneficia a otra distinta con la que tienen cuentas que saldar mis representados, lo que se enfrenta con la garantía del art. 17.2, párrafo 2.º LEC.

Por todo ello,

AL TRIBUNAL SUPLICO

que, teniendo por presentado este escrito, con justificante de haberse trasladado a los Procuradores de las demás partes personadas, se sirva admitirlo, y por efectuadas las alegaciones antecedentes, se me tenga por personada y parte en la representación que ostento de los ejecutados [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS], y por opuestos a que se admita la sucesión procesal del ejecutado [NOMBRE Y APELLIDOS] en posición de parte ejecutante, salvo contra la deudora principal [DENOMINACIÓN SOCIAL], debiéndose sobreseer el proceso de ejecución respecto de mis patrocinados, sin perjuicio de los derechos de [NOMBRE Y APELLIDOS] que pueda ejercer donde y como corresponda.

Es justicia debe hacerse en [LUGAR], a [FECHA].

Firma del Abogado/	Firma del Procurador/a

========================================================================
