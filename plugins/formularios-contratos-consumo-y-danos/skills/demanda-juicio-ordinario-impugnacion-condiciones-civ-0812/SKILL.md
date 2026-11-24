---
name: demanda-juicio-ordinario-impugnacion-condiciones-civ-0812
description: "Demanda de juicio ordinario de impugnación de condiciones generales de la contratación (Ley 7 1998). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario de impugnación de condiciones generales de la contratación (Ley 7 1998)

> Formulario **CIV-0812** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario de impugnación de condiciones generales de la contratación (Ley 7 1998)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario de impugnación de condiciones generales de la contratación (Ley 7 1998)” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-impugnacion-condiciones-civ-0812`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DÍA
- [ ] IMPORTE
- [ ] MES
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE Y APELLIDOS
- [ ] NÚMERO

## Normas que cita el formulario

- art. 8 Ley 7/1998
- art. 52.1 LEC
- art. 85.1 LOPJ
- art. 16.1 Ley 7/1998
- art. 12 Ley 7/1998
- art. 5 Ley Orgánica 1/2025
- art. 9.2 Ley 7/1998
- art. 1261 Código Civil
- art. 394 LEC
- art. 7.2 Ley 10/2012

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…curador ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de la Asociación de Consumidores [DENOMINACIÓN SOCIAL], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], por medio de la presente formulo demanda de impugnación de condiciones generales de contratación frente a la mercantil [DENOMINACIÓN SOCIAL] SA con domicilio en [LOCALIDAD] en base a los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- La Asociación que represento agrupa a los profesionales de [ACTIVIDAD] y tiene encomendada la defensa de intereses de sus miembros, tal como consta en sus estatutos que se acompañan como documento número

Un amplio número de asociados han suscrito con la mercantil demandada [DENOMINACIÓN SOCIAL] contratos de suministro con el siguiente objeto

Tales contratos se han formalizado por medio de contratos de adhesión, tratándose de formularios prerredactado que utiliza la mercantil demandada para sus clientes (acompaño como documentos número [Nº DE DOCUMENTO] diferentes contratos suscritos con asociados).

SEGUNDO.- Como se ha indicado, la mercantil [DENOMINACIÓN SOCIAL] de cara a realizar sus suministros utiliza el contrato tipo adjuntado.

Entre las cláusulas de los mismos se incluye con el número sexto, la cláusula que se impugna en esta demanda que tiene el siguiente tenor literal:

Dicha cláusula se estima abusiva ya que en la misma se indica que la entrega de los suministros se hará dentro de un margen de fechas que se dice solamente opera a título orientativo eximiéndose la suministradora de toda responsabilidad en el incumplimiento de tales plazos.

TERCERO.- La citada cláusula debe calificarse como condición general de la contratación, puesto que reúne las notas exigidas jurisprudencialmente, pudiendo citarse la STS 9 de mayo de 2013, rec. 485/2012, entre otras, como son: 1) contractualidad, puesto que evidentemente la inserción en el contrato no deriva del acatamiento de una norma imperativa; 2) predisposición, pues se trata de una cláusula prerredactada, que se incluye en un contrato de adhesión; 3) imposición, puesto que cualquiera que quiera contratar con la demandada sólo puede hacerlo mediante el acatamiento a la inclusión en el mismo de la cláusula; y 4) generalidad, ya que las cláusulas están incorporadas a todos los contratos celebrados por la entidad demandada.

Tratándose de una condición general, es obvio que la referida cláusula es abusiva por cuanto que reserva a la entidad demandada un plazo indeterminado para satisfacer la prestación, eximiéndose de cualquier responsabilidad derivada por su incumplimiento, lo cual supone una vinculación del contrato a la voluntad del la empresa suministradora en perjuicio del adherente, afectando al objeto principal del contrato y a la justa reciprocidad de las prestaciones, lo que determina la nulidad de la condición general impugnada según lo dispuesto en el art. 8 de la Ley 7/1998, sobre condiciones generales de la contratación.

CUARTO.- Mi representado, previamente a la interposición de la demanda, ha requerido a la entidad solicitando la eliminación de las cláusulas.

Se acompaña como documentos núms. y [Nº DE DOCUMENTO] la solicitud de eliminación de las cláusulas y la respuesta de la entidad demandada.

FUNDAMENTOS DE DERECHO

PRIMERO.- Competencia.-Corresponde a los Tribunales de [LOCALIDAD] conforme a lo dispuesto en el apartado 14º del art. 52.1 de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

SEGUNDO.- Procedimiento y cuantía.-Es el juicio ordinario con fundamento en el art. 249.1.5.ºLEC al ejercitarse una acción relativa a condiciones generales de contratación, no incluida en el ámbito del art. 250.1.12ºLEC, fijando la cuantía como indeterminada.

TERCERO.- Legitimación.-Le corresponde a esta parte la activa conforme al art. 16.1 de la Ley 7/1998, de 13 de abril, sobre condiciones generales de la contratación, y la pasiva a la mercantil demandada, según lo dispuesto en el art. 17 de la citada Ley.

CUARTO.- Acción ejercitada.-La de cesación en el uso de una condición general de contratación nula del art. 12 de la Ley 7/1998, de 13 de abril, sobre condiciones generales de la contratación, el cual dispone que la acción de cesación se dirige a obtener una sentencia que condene al demandado a eliminar de sus condiciones generales las que se reputen nulas y a abstenerse de utilizarlas en lo sucesivo, determinando o aclarando, cuando sea necesario, el contenido del contrato que ha de considerarse válido y eficaz.

QUINTO.- Requerimientos previos.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

SEXTO.- Fondo de la reclamación.- El art. 8 de la Ley 7/1998, de 13 de abril, sobre condiciones generales de la contratación, declara que son nulas de pleno derecho las condiciones generales que contradigan en perjuicio del adherente lo dispuesto en esta Ley o en cualquier otra norma imperativa o prohibitiva, salvo que en ellas se establezca un efecto distinto para el caso de contravención.

En este caso, la cláusula impugnada afecta al objeto principal del contrato y rompe la equivalencia de prestaciones, imponiéndose unilateralmente a los adherentes y en su perjuicio, por lo que incurre en vicio de nulidad.

SÉPTIMO.- Efectos.- El art. 9.2 de la citada Ley 7/1998 establece que la sentencia estimatoria, obtenida en un proceso incoado mediante el ejercicio de la acción individual de nulidad o de declaración de no incorporación, decretará la nulidad o no incorporación al contrato de las cláusulas generales afectadas y aclarará la eficacia del contrato de acuerdo con el artículo 10,o declarará la nulidad del propio contrato cuando la nulidad de aquellas o su no incorporación afectara a uno de los elementos esenciales del mismo en los términos del artículo 1261del Código Civil.

OCTAVO.- En materia de costas el art. 394 LEC señala que las de primera instancia se imponen a la parte que vea en primera instancia rechazadas sus pretensiones.

En base a lo anterior,

SUPLICO AL TRIBUNAL: Que tenga por presentada la presente demanda con los documentos a ella adjuntos y por parte en la representación que ostento se tenga por formulada demanda de acción de cesación en el uso de condición general de la contratación y en virtud de ella se condene a [NOMBRE DE LA PARTE] a eliminar de sus condiciones generales empleadas en sus contratos de suministro adjuntos como doc. la n.º [NÚMERO] que se reputa nula dejando constancia de ello en el Registro pertinente, todo ello con condena en costas a la demandada.

OTROSÍ DIGO: Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 300 euros correspondiente a la cuota fija, más la cantidad de [IMPORTE] euros por la aplicación a la base imponible de la escala prevista en el artículo 7.2 de la Ley 10/2012

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

a [DÍA] de [MES] de [AÑO]

Firma Abogado	Firma Procurador

========================================================================
