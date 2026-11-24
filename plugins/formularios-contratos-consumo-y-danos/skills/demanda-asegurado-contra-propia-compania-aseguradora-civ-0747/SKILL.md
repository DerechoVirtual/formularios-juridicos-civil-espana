---
name: demanda-asegurado-contra-propia-compania-aseguradora-civ-0747
description: "Demanda del asegurado contra su propia compañía aseguradora. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda del asegurado contra su propia compañía aseguradora

> Formulario **CIV-0747** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda del asegurado contra su propia compañía aseguradora» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda del asegurado contra su propia compañía aseguradora” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-asegurado-contra-propia-compania-aseguradora-civ-0747`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] MES (5 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] ASEGURADORA (3 veces)
- [ ] DESCRIBIR (2 veces)
- [ ] FECHA (2 veces)
- [ ] Nº (2 veces)
- [ ] CALLE
- [ ] DIRECCIÓN
- [ ] LUGAR
- [ ] MARCA/MODELO
- [ ] MATRÍCULA
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] Nº DE CLÁUSULA
- [ ] OTROS DATOS
- [ ] SEDE
- [ ] TIPO DE INTERÉS

## Normas que cita el formulario

- art. 21 LOPJ
- art. 85.1 LOPJ
- art. 24 Ley 50/1980
- art. 249.2 LEC
- art. 10 LEC
- art. 1 Ley 50/1980
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1254 CC
- art. 3 LCS
- art. 20 LCS
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

D./Dña [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], y como mejor proceda en derecho

DIGO:

Que mediante el presente escrito formulo demanda a tramitar por el cauce del juicio declarativo ordinario contra la Compañía de seguros [ASEGURADORA], con sede en esta ciudad en la C/ [CALLE], número [NÚMERO] en reclamación de indemnización por daños y perjuicios sufridos en el vehículo modelo [MARCA/MODELO], matrícula [MATRÍCULA] de titularidad de mi representado en la cuantía de [IMPORTE] euros más los interes de demora. Baso nuestra pretensión en los siguientes

HECHOS

Primero.- Mi mandante tiene contratada póliza de seguros en vigor con la Aseguradora demandada para cubrir los daños ocasionados en el propio vehículo. La póliza es la nº [NÚMERO], en vigor desde [FECHA] y en cuyo apartado [Nº] de las condiciones particulares expresamente se hace constar que están cubiertos los daños sufridos en el propio vehículo asegurado hasta un importe de [IMPORTE] euros.

Acompaño como documento nº [Nº DE DOCUMENTO] copia de la póliza con sus condiciones generales y particulares y como documento nº [Nº DE DOCUMENTO] copia de justificante de pago de la prima anual que asegura los meses de [MES] a

Segundo.- El día [DÍA] de [MES] de [AÑO], cuando circulaba por [DIRECCIÓN] a las [Nº] horas, sufrí un accidente consistente en [DESCRIBIR]

[ELEGIR UNA OPCIÓN: Colisión vallas / Colisión con otro vehículo / Otro]

Tercero.-

[ELEGIR UNA OPCIÓN: Asegurado / Agentes de la Autoridad]

Cuarto.- Como consecuencia de la colisión el vehículo asegurado sufrió una serie de daños consistentes en [DESCRIBIR], según hizo constar el perito de la Compañía de Seguros demandada, y constan en el informe que emitió

Quinto.- Una vez llevado al taller que indicaron a mi representado la Compañía de Seguros [ASEGURADORA] comunica por teléfono a mi representado el día [DÍA] de [MES] de [AÑO] y posteriormente por escrito el día (doc. nº [NÚMERO]) que no se hacen cargo de la reparación porque [OTROS DATOS] no está incluido en la cobertura contratada.

Sexto.- Como mi representado necesitaba el vehículo para trabajar encarga la reparación (doc. nº [NÚMERO]) y abona el importe de la factura que ascendió a [IMPORTE] euros según se acredita con el documento nº [Nº DE DOCUMENTO].

En fecha [DÍA] de [MES] de [AÑO] nuevamente se reclama a la Aseguradora la cantidad arriba indicada, según acredito con justificante de burofax que acompaño como documento nº [Nº DE DOCUMENTO] por considerar esta parte que el supuesto entraba dentro de la cobertura, pero hasta la fecha no se ha tenido contestación de la ahora demandada, motivo por el que nos vemos obligados a acudir a la vía judicial.

Séptimo.- A la cantidad reclamada se le deberán añadir los intereses de demora desde la fecha en que se puso en conocimiento de la demandada el acaecimiento el siniestro, puesto que se ha negado a asumir sus responsabilidades.

Octavo.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I. Jurisdicción y Competencia.—Los artículos 21 y 22 de la LOPJ y 36 de la LEC atribuyen a la jurisdicción española y al orden civil el conocimiento de estos hechos. Los artículos 85.1º de la LOPJ y 45 de la LEC designan a los Tribunales de Instancia como los órganos que específicamente resolverán estos pleitos. El artículo 24 de la Ley 50/1980, de contrato de seguro fija la competencia territorial de manera inequívoca, atribuyendo el conocimiento al Tribunal del domicilio del asegurado, siendo nulo cualquier pacto en contrario.

II. Tramitación.—Por la cuantía de la reclamación, que se cifra en [IMPORTE] euros el trámite a seguir será el del juicio ordinario en aplicación del artículo 249.2 de la LEC.

III. Legitimación y Postulación.—El artículo 10 de la LEC legitima para comparecer a los titulares de la relación jurídica u objeto litigioso.

El artículo 1 de la Ley 50/1980, de 8 de octubre, de Contrato de Seguro, obliga al asegurador a indemnizar, dentro de límites pactados, el daño producido al asegurado o a dar la prestación convenida.

En materia de postulación son de aplicación los artículos 23 y 31 de la LEC.

IV. Cumplimiento de los requisitos de procedibilidad.— La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V. Fondo del asunto.

Primero.— El artículo 1 de la Ley de contrato de seguro obliga a la Aseguradora a cumplir las obligaciones pactadas, en la línea de lo establecido también en los artículos 1254 y 1255 del CC. Sobre la obligación de cumplir lo pactado.

Segundo.— La Aseguradora esgrime, en la carta que remite a mi representado, la cláusula [Nº DE CLÁUSULA] de las condiciones generales para negar la cobertura, pero lo cierto es que en las condiciones particulares el riesgo está cubierto sin las limitaciones que ellos intentan aplicar y que éstas son las únicas condiciones que asumió el demandante, puesto que no consta que haya firmado ni asumido expresamente esas condiciones generales que ahora le intentan aplicar.

Será de aplicación lo establecido en el artículo 3 de la LCS. No nos encontramos ante una cláusula delimitadora del riesgo cubierto, sino ante una cláusula limitativa que requiere una expresa aceptación que aquí no se ha producido.

Tercero.— Será de aplicación el artículo 20 de la LCS de imposición de intereses.

VI. Costas.—En aplicación del artículo 394 de la LEC se impondrán al demandado.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por presentada esta demanda con los documentos que acompaño y copia de todo ello, la admita a trámite y previos los trámites legales oportunos, dicte en su día sentencia por la que se condene a la Compañía Aseguradora [ASEGURADORA], a indemnizar a D./Dña. [NOMBRE Y APELLIDOS] en la cuantía de [IMPORTE] euros y al pago de los intereses de [TIPO DE INTERÉS] desde [FECHA], así como a las costas de este juicio.

Es justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

========================================================================
