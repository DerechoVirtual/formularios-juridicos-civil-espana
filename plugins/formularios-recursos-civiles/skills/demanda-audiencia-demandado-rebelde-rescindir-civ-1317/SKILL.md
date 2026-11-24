---
name: demanda-audiencia-demandado-rebelde-rescindir-civ-1317
description: "Demanda de audiencia al demandado rebelde para rescindir la sentencia firme. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de audiencia al demandado rebelde para rescindir la sentencia firme

> Formulario **CIV-1317** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de audiencia al demandado rebelde para rescindir la sentencia firme» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de audiencia al demandado rebelde para rescindir la sentencia firme” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:demanda-audiencia-demandado-rebelde-rescindir-civ-1317`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] PROVINCIA (3 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] NOMBRE DE LA PARTE
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 501.3 LEC
- art. 501 LEC
- art. 507 LEC
- art. 4.1 LO 1/2025
- art. 504.2 LEC
- art. 506.2 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], actuando en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

- Que mediante el presente escrito, al amparo de lo dispuesto en el art. 501 y ss. de la LEC formulo demanda de audiencia al demandado rebelde en solicitud de la rescisión de la sentencia de fecha [FECHA] dictada por la Sección Civil del Tribunal de Instancia nº [NÚMERO] al que me dirijo en autos de juicio verbal [Nº DE PROCEDIMIENTO] seguidos a instancias de [NOMBRE DE LA PARTE] contra mi representado, que fue notificada mediante publicación en el BO de [PROVINCIA] el pasado día [FECHA], en base a los siguientes

HECHOS

PRIMERO.- (antecedentes del proceso de instancia y cumplimiento de presupuestos) Se solicita la audiencia en relación a los autos seguidos ante el Tribunal al que me dirijo a instancia de D. [NOMBRE Y APELLIDOS] contra mi representado, en los que se dictó sentencia en fecha [FECHA] que fue publicada en el BO de [PROVINCIA] el día [FECHA]

El juicio se siguió sin oír a mi representado, quien desconocía la existencia de la demanda y del pleito, puesto que fue citado a juicio por edictos que fueron publicados en el tablón de anuncios de este Tribunal, sin que esta parte demandada tuviera oportunidad alguna de conocer dicha citación edictal, no sólo por el carácter ficticio de la misma, sino también porque el domicilio de mi representado se halla en la localidad de [LOCALIDAD] y no en la de [LOCALIDAD], según facilitó incorrectamente el demandante en el proceso.

La audiencia se solicita en el plazo de cuatro meses desde la notificación de la sentencia en el BO de [PROVINCIA], sin que esta parte haya podido interponer recurso de apelación contra la misma, puesto que sólo tuvo conocimiento de la sentencia el pasado día [FECHA] cuando se notificó el auto despachando ejecución por el Tribunal en el verdadero domicilio de mi representado, como posteriormente indicaremos.

SEGUNDO.- (motivos de impugnación y circunstancias fácticas) La audiencia se solicita al amparo del art. 501.3º de la LEC al desconocerse por el demandado la demanda y el pleito y no estar en el lugar en que se siguió el proceso y se publicaron los edictos para citación, como ya se ha anticipado.

En efecto, mi representado tiene su domicilio en la localidad de [LOCALIDAD], domicilio en el que fue finalmente notificado de las actuaciones de ejecución. En la demanda del proceso de instancia consta como domicilio de mi representado el de la localidad de [LOCALIDAD], que fue el que facilitó el actor y donde se intentó la citación con resultado negativo, tal como es de ver en los autos. En dicho domicilio mi representado tenía hace unos años una sucursal que fue cerrada exactamente hace dos años, por lo que en modo alguno era un domicilio válido para efectuar la citación al tiempo de deducirse la demanda.

Por tanto, es indudable que mi representado ha estado ausente de la localidad en que se siguió el proceso y donde se publicaron los edictos, puesto que su único domicilio radica en la localidad de [LOCALIDAD], perteneciente a la Comunidad Autónoma de [LOCALIDAD], por lo que ninguna oportunidad tuvo de conocer la citación.

Debemos subrayar que esta circunstancia debía ser conocida por el actor, quien, ya en fase de ejecución, facilita el domicilio correcto, por lo que entendemos que debe acordarse la imposición de costas al citado, pues con su conducta ha ocasionado graves perjuicios a esta parte.

TERCERO.- (Consecuencias jurídicas pretendidas) Por tanto, concurre el motivo de rescisión prevenido en el apartado tercero del art. 501 de la LEC, acudiendo a esta vía impugnatoria para que se rescinda la sentencia dictada por ese mismo Tribunal, decretando que se retrotraigan las actuaciones para sustanciar el procedimiento en la forma que prescribe el art. 507 de la LEC, con imposición de las costas de este juicio al actor por su temeridad y mala fe.

A los anteriores hechos son de aplicación los siguientes,

FUNDAMENTOS DE DERECHO

I. En cuanto a la jurisdicción y competencia, es competente la Sala a la que me dirijo conforme a lo dispuesto en el art. 501 de la LEC.

II. Está legitimado activamente mi representado al haberse seguido el proceso sin que haya comparecido, conforme al citado art. 501 y 504.1 de la LEC.

III. En cuanto al cumplimiento de los requisitos de procedibilidad, la presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional por tratarse de materia excluidas del requisito de procedibilidad, de acuerdo con el art. 4.1 II LO 1/2025, en cuanto la demanda de audiencia al demandado rebelde es un mecanismo procesal extraordinario, quedando el proceso fuera del principio de disponibilidad, y, por tanto, no exige el intento previo de Medios Adecuados de Solución de Controversias (MASC) como requisito de procedibilidad.

IV. En cuanto al procedimiento, deben seguirse los trámites del proceso ordinario, tal como dispone el art. 504.2 LEC.

V. En cuanto al fondo, es de aplicación el art. 501.3 de la LEC al haberse seguido el juicio sin conocimiento de mi representado que fue citado mediante edictos y que estaba ausente del lugar del juicio por tener su domicilio en la localidad de

VI. En cuanto a las costas, es de aplicación lo dispuesto en el art. 506.2 de la LEC, debiendo imponerse al demandante en el proceso cuya rescisión se pretende por su temeridad y mala fe, puesto que existen motivos para afirmar que ha ocultado el domicilio de mi representado durante todo el curso del proceso, como lo prueba el hecho que lo haya facilitado una vez ha obtenido sentencia a su favor y cuando ya se ha iniciado la fase de ejecución.

Por lo expuesto es de justicia y

AL TRIBUNAL SUPLICO que tenga por presentada esta demanda de petición de audiencia a mi representado D. [NOMBRE Y APELLIDOS], demandado en los autos seguidos ante la Sección Civil del Tribunal de Instancia número [NÚMERO], y, previos los trámites legales, dicte sentencia por la que rescinda la dictada por el Tribunal en fecha [FECHA], acordando que el proceso se siga con audiencia de mi representado, sustanciándose el procedimiento conforme dispone el art. 507 de la LEC, y con imposición de costas al actor en el proceso cuya rescisión se pretende.

OTROSÍ PRIMERO que teniendo intención esta parte de solicitar la suspensión de la ejecución en curso, es necesario a su derecho de defensa obtener testimonio de la resolución de admisión de esta demanda (en su caso, también se puede formalizar la solicitud en este mismo otrosí conforme al formulario siguiente).

SUPLICO AL TRIBUNAL acuerde expedir testimonio de la resolución de admisión de esta demanda tan pronto la misma sea dictada.

OTROSÍ DIGO que, de conformidad con lo dispuesto en los apartados 3.d) y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 50 euros.

Por lo que, SUPLICO A LA SALA que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

En L. y F.

(Firma Procurador y Abogado)

========================================================================
