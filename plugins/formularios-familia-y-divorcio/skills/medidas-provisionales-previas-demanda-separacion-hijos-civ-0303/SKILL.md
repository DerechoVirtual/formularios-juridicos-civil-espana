---
name: medidas-provisionales-previas-demanda-separacion-hijos-civ-0303
description: "Medidas provisionales previas a la demanda de separación con hijos menores y salida del otro cónyuge. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Medidas provisionales previas a la demanda de separación con hijos menores y salida del otro cónyuge

> Formulario **CIV-0303** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito inicial, con representación de procurador, para solicitar medidas provisionales previas a la demanda de separación (arts. 771 LEC y 102 y 103 CC) cuando existen hijos menores y el otro cónyuge ha abandonado el domicilio familiar: guarda y custodia, visitas, uso de la vivienda y contribución a las cargas.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Medidas provisionales previas a la demanda de separación con hijos menores y salida del otro cónyuge» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Medidas provisionales previas a la demanda de separación con hijos menores y salida del otro cónyuge” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:medidas-provisionales-previas-demanda-separacion-hijos-civ-0303`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (5 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] NÚMERO (4 veces)
- [ ] DOMICILIO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE (3 veces)
- [ ] FIRMA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] Nº DE COLEGIADO (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] CENTRO DE TRABAJO
- [ ] DENOMINACIÓN DE LA ENTIDAD
- [ ] DOMICILIO DE LA VIVIENDA FAMILIAR
- [ ] DOMICILIO PROFESIONAL
- [ ] DÍAS Y HORARIO PROPUESTO
- [ ] EDADES
- [ ] EMPRESA
- [ ] JUSTIFICACIÓN DE LA CUANTÍA
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL SOLICITANTE
- [ ] NOMBRES
- [ ] SEDE

## Normas que cita el formulario

- art. 771.1 LEC
- art. 771 LEC
- art. 81 CC
- art. 10 LEC
- art. 4.1 LO 1/2025
- art. 102 CC
- art. 103 CC
- art. 81.2.º CC
- art. 66 CC
- art. 104 CC
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

- Junto a «…disposición de las partes), según el art. 4.1, párrafo segundo, de la LO 1/2025.»: comprobar el artículo exacto de la LO 1/2025 que regula las materias excluidas del requisito de procedibilidad (art. 5.2, según la numeración vigente).
- Junto a «… que afecten a derechos y obligaciones que no estén a disposición de las partes.»: comprobar el artículo equivalente de la LO 1/2025 (art. 5.2).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Nota previa: aunque la cuestión es discutida por la doctrina, el modelo contempla la no sujeción al previo intento de resolución de controversias en vía no jurisdiccional, por tratarse de materias excluidas del requisito de procedibilidad (entre ellas, los conflictos que afecten a derechos y obligaciones que no estén a disposición de las partes), según el art. 4.1, párrafo segundo, de la LO 1/2025.


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

AL TRIBUNAL DE INSTANCIA
SECCIÓN CIVIL – SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales con número de colegiado [Nº DE COLEGIADO], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL SOLICITANTE], con domicilio en [DOMICILIO], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº DE DOCUMENTO], con la asistencia del Letrado/a suscrito/a D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [LOCALIDAD], con despacho abierto en [DOMICILIO PROFESIONAL], ante el Tribunal comparezco y, como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito vengo a formular solicitud de MEDIDAS PROVISIONALES PREVIAS frente a D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], con domicilio en [DOMICILIO], en base a los siguientes datos y argumentos:

HECHOS

PRIMERO.– Mi mandante contrajo matrimonio [ELEGIR: canónico / civil] con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], en [LOCALIDAD], el día [DÍA] de [MES] de [AÑO], a cuya acreditación se acompaña certificación expedida por el Registro Civil de [LOCALIDAD], como DOCUMENTO N.º [Nº DE DOCUMENTO].

SEGUNDO.– De dicho matrimonio nacieron [NÚMERO] hijos, conforme se acredita mediante la aportación, como DOCUMENTOS NÚMEROS [Nº DE DOCUMENTO], de las certificaciones de las respectivas inscripciones de nacimiento, que en la actualidad cuentan con [EDADES] años, respectivamente.

TERCERO.– Desde el pasado día [DÍA] de [MES] de [AÑO], el sujeto pasivo de las medidas, cónyuge de mi mandante, ha decidido pernoctar fuera del domicilio conyugal, pasando a [LUGAR DONDE RESIDE ACTUALMENTE, por ejemplo, la casa de sus padres], en [LOCALIDAD], calle [DOMICILIO], sin aportar nada de sus ingresos al sostenimiento de la familia.

CUARTO.– El régimen económico del matrimonio es el legal supletorio, por no haberse otorgado nunca capitulaciones, siendo que el/la solicitante tiene empleo como [PROFESIÓN] [ELEGIR: a tiempo completo / a tiempo parcial (media jornada)] en [EMPRESA], mientras que el demandado es [PROFESIÓN], en [CENTRO DE TRABAJO], gozando de ingresos con los que es dable mantener el nivel de gastos fijos de la atención de la casa y que genera la manutención y educación de los hijos comunes.

Se adjuntan copias de las autoliquidaciones del I.R.P.F. de los ejercicios [AÑO] y [AÑO], del actor y del demandado, como DOCUMENTOS NÚMS. [Nº DE DOCUMENTO], así como certificaciones de movimientos y saldos de cuenta bancaria emitidas por la entidad [DENOMINACIÓN DE LA ENTIDAD], como DOCUMENTOS NÚMS. [Nº DE DOCUMENTO].

QUINTO.– Es voluntad de mi mandante, sin optar por el momento por la disolución de su matrimonio, solicitar la separación de su cónyuge.

FUNDAMENTOS DE DERECHO

I.– Es competente el Tribunal de Instancia del lugar del domicilio del solicitante, conforme al art. 771.1, párrafo primero, LEC.

II.– El proceso adecuado es el del art. 771 LEC para conocer de la solicitud de medidas provisionales previas.

III.– Tiene el demandante legitimación activa ordinaria por hallarse en la situación jurídica de relación conyugal, como detenta la pasiva su cónyuge (art. 81 CC y art. 10, párrafo primero, LEC), siendo el objeto del proceso la tutela judicial cautelar de la pretensión de separación conyugal anunciada.

IV.– La presente solicitud no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional, por tratarse de materias excluidas del requisito de procedibilidad de acuerdo con el art. 4.1, párrafo segundo, de la LO 1/2025, entre las cuales se encuentran los conflictos que afecten a derechos y obligaciones que no estén a disposición de las partes.

V.– El fondo de la pretensión consiste en la adopción de los efectos del art. 102 CC y las medidas del art. 103 CC, de cognición judicial, derivados de la admisión futura de la demanda de separación matrimonial, la cual se fundará en la mera petición de esta parte, una vez transcurridos tres meses desde la celebración del matrimonio, conforme al art. 81.2.º CC.

Aunque ninguna causa debe anunciarse, debe alegarse que el otro cónyuge no respeta los deberes contenidos en los arts. 66, 67 y 68 CC.

El art. 104 CC presume la urgencia para la tutela sumaria cautelar y el peligro de infructuosidad de no adoptarse los anteriores efectos y medidas.

Los [NÚMERO] hijos menores comunes del matrimonio han estado siempre en compañía del progenitor solicitante, mi mandante, y es lo conveniente que continúen con él/ella, habida cuenta de [CIRCUNSTANCIAS: conducta del otro progenitor, salida del hogar, etc.], pareciendo suficiente la comunicación, sin estancia de pernocta, del otro progenitor [DÍAS Y HORARIO PROPUESTO] de todas las semanas, por lo menos hasta la resolución definitiva.

En cuanto a la vivienda familiar, procede que se atribuya a mi mandante su uso, así como la utilización del ajuar familiar, sin perjuicio de los inventarios que se estimen necesarios, toda vez que, por lo expuesto, queda claro que resulta ser el interés familiar más necesitado de protección.

Dada la situación económica de D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE] y de mi mandante, aquel/aquella deberá abonar como contribución a las cargas del matrimonio y alimentos la cantidad de [IMPORTE] euros. Esta cantidad se justifica por [JUSTIFICACIÓN DE LA CUANTÍA].

VI.– Las costas procesales deben ser impuestas a la parte demandada, por criterio del íntegro vencimiento, en atención al art. 394 LEC.

Y demás normas y jurisprudencia de general y pertinente aplicación.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL:

que, teniendo por presentado este escrito con sus copias y documentos adjuntados, se digne admitir uno y otros, tener al/a la firmante por comparecido/a y parte, entendiéndose conmigo las sucesivas diligencias, y por deducida solicitud de adopción de medidas provisionales previas, seguido que sea su pertinente trámite, se dicte Auto por el que se aprueben las siguientes:

a) Separación provisional de los cónyuges, con cese de la presunción de convivencia.

b) Revocación de los consentimientos y poderes que cualquiera de los cónyuges hubiera otorgado a favor del otro, cesando la posibilidad de vincular los bienes privativos del otro cónyuge en el ejercicio de la potestad doméstica.

c) Asignación al progenitor solicitante de la guarda y custodia de los [NÚMERO] hijos menores, [NOMBRES], quedando en potestad compartida de ambos progenitores.

d) Fijación de un derecho provisional de comunicación y visita del demandado a sus hijos [DÍAS Y HORARIO, por ejemplo, todos los sábados de cada semana de diez a veinte horas].

e) Atribución del uso exclusivo de la vivienda familiar sita en [DOMICILIO DE LA VIVIENDA FAMILIAR], al/a la solicitante y a los [NÚMERO] hijos, así como del ajuar doméstico en ella existente.

f) Fijación de la cantidad de [IMPORTE] euros mensuales en concepto de contribución al levantamiento de las cargas familiares, que será ingresada, en cumplimiento de oficio del Tribunal, por meses anticipados, dentro de los cinco primeros días de cada mes, en la cuenta bancaria que el/la solicitante designe.

Dicha cantidad se actualizará anualmente, con efectos de primero de enero de cada año, en proporción a las variaciones que experimenten los índices de precios al consumo, según el Instituto Nacional de Estadística u organismo que le sustituya.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
