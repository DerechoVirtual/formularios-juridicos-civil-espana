---
name: demanda-juicio-verbal-reclamacion-cantidad-contrato-civ-0846
description: "Demanda de juicio verbal por reclamación de cantidad por contrato de obra de hasta 2.000 euros. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal por reclamación de cantidad por contrato de obra de hasta 2.000 euros

> Formulario **CIV-0846** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda sucinta de juicio verbal para reclamar una cantidad que no excede de 2.000 euros por trabajos realizados en virtud de un contrato de obra. No precisa de abogado ni procurador por razón de la cuantía; demandante y demandado son personas físicas.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal por reclamación de cantidad por contrato de obra de hasta 2.000 euros» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal por reclamación de cantidad por contrato de obra de hasta 2.000 euros” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-verbal-reclamacion-cantidad-contrato-civ-0846`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] IMPORTE EN LETRA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] CÓDIGO POSTAL (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] AÑO
- [ ] CORREO ELECTRÓNICO
- [ ] DESCRIPCIÓN DE LA OBRA
- [ ] DESCRIPCIÓN DE LOS TRABAJOS REALIZADOS
- [ ] DNI/NIE
- [ ] DÍA
- [ ] ESTADO CIVIL
- [ ] FECHA
- [ ] FECHAS
- [ ] FIRMA
- [ ] MES
- [ ] Nº DE TELÉFONO
- [ ] SEDE

## Normas que cita el formulario

- art. 437.1 LEC
- art. 437.2 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, [ESTADO CIVIL], provisto/a de DNI [DNI/NIE], de profesión [PROFESIÓN], y domiciliado/a en [LOCALIDAD] ([CÓDIGO POSTAL]), calle [DOMICILIO], n.º [Nº], ante el Tribunal comparezco y, como mejor en Derecho proceda (1) (2) (3), DIGO:

Que por medio del presente escrito vengo a formular DEMANDA DE JUICIO VERBAL sobre reclamación de cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €), contra D./Dña. [NOMBRE Y APELLIDOS], de profesión [PROFESIÓN], y domiciliado/a en [LOCALIDAD] ([CÓDIGO POSTAL]), calle [DOMICILIO], n.º [Nº].

Que el demandado adeuda al que suscribe la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €), por no haber pagado el importe de los trabajos de [DESCRIPCIÓN DE LOS TRABAJOS REALIZADOS] realizados en su indicado domicilio, concretamente [DESCRIPCIÓN DE LA OBRA], según el presupuesto aceptado y firmado por el mismo y según la factura final extendida y presentada al cobro.

Que el demandado se ha negado a satisfacer su deuda, a pesar de los repetidos requerimientos que le han sido efectuados, forzando a la presente reclamación.

En este sentido, la parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria, incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, esta parte envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, [ELEGIR: directamente / a través del abogado que firma este escrito], el cual fue contestado por el demandado por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento n.º [Nº] el requerimiento efectuado y como documento n.º [Nº] la contestación del demandado.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, con su copia, lo admita, y teniendo por formulada demanda sucinta de juicio verbal, en nombre y derecho propio, acuerde dar traslado al demandado para que comparezca y la conteste, y, seguido el juicio por sus trámites, se dicte sentencia condenando al demandado al pago de la cantidad reclamada de [IMPORTE EN LETRA] euros ([IMPORTE] €), más sus intereses [ELEGIR: desde el requerimiento, si se ha hecho y existe constancia / desde la interpelación judicial], y las costas procesales que hubiere.

OTROSÍ DIGO:

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en términos del art. 399.1, párrafo segundo, en relación con el art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y n.º de teléfono: [CORREO ELECTRÓNICO] / [Nº DE TELÉFONO].

Por lo expuesto,

AL TRIBUNAL NUEVAMENTE SUPLICO que, teniendo por hecha la anterior manifestación, se admita y provea en consecuencia.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del demandante: [FIRMA]

(1) Se indicarán todos los domicilios del deudor que se conozcan, y si no, el del lugar donde pueda ser hallado a efectos del requerimiento.

(2) Está previsto en el art. 437.2 LEC que estén a disposición de las partes impresos normalizados.

(3) En este supuesto, podrá la parte optar por el juicio verbal o el "monitorio".
