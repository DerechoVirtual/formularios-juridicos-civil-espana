---
name: escrito-contestacion-demanda-divorcio-civ-0321
description: "Escrito de contestación a la demanda de divorcio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de contestación a la demanda de divorcio

> Formulario **CIV-0321** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito de escrito de contestación a la demanda de divorcio.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de contestación a la demanda de divorcio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de contestación a la demanda de divorcio” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:escrito-contestacion-demanda-divorcio-civ-0321`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] ENFERMEDAD
- [ ] FECHA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] Nº DE CUENTA (IBAN)
- [ ] RÉGIMEN DE VISITAS

## Normas que cita el formulario

- art. 81.2.º CC
- art. 86 CC
- art. 92 CC
- art. 96 CC
- art. 145 CC
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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

AL TRIBUNAL

D/Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de Dña. [NOMBRE Y APELLIDOS], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo la dirección del/de la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], colegiado/a n.º [NÚMERO] del Iltre. Colegio de [LOCALIDAD], con despacho abierto en [LOCALIDAD], calle [CALLE], en autos de Juicio de divorcio n.º [NÚMERO]/[AÑO] promovido por D. [NOMBRE Y APELLIDOS], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que, en la representación que ostento y dentro del plazo legal, vengo a CONTESTAR a la demanda formulada de adverso, con base en los siguientes hechos y fundamentos:

HECHOS

PRIMERO.- De acuerdo con el correlativo de la demanda, sobre los datos del matrimonio celebrado, separación conyugal de hecho y régimen económico de los cónyuges, negando el resto de los hechos alegados en la misma, en los que justifica la solicitud de las medidas relativas al hijo menor y la determinación de la contribución económica para su manutención y educación.

SEGUNDO.- El hijo menor no sólo padece la enfermedad genética señalada, sino que sufre la dolencia crónica de [ENFERMEDAD], que precisa del cuidado constante de quien, como su madre que es doctora en medicina, y que dispone de autonomía profesional para tenerle permanentemente en compañía, es capaz de proporcionar. El padre, según la demanda reconoce, está viajando continuamente, y su actual residencia está alejada del domicilio familiar y de la consulta de mi patrocinada en la localidad de [LOCALIDAD] Se acompañan informes médicos relativos al padecimiento del hijo como documentos n.os y [Nº DE DOCUMENTO].

TERCERO.- En cuanto a la obligación de mantenimiento del hijo menor, ha de tenerse en cuenta, por su proporcionalidad a los recursos económicos de los padres, no sólo que la madre custodia goza de unas rentas suficientes, sino que el demandante, que dice en la demanda ser agente comercial, en realidad tiene título de ingeniero y desempeña un importante cargo en la empresa [DENOMINACIÓN SOCIAL], S.L., adjuntándose a esta exposición, como documentos n.os y [Nº DE DOCUMENTO], copia de la última declaración de IRPF de D. [NOMBRE Y APELLIDOS] que ha tenido en su poder mi mandante, y certificado del plan de pensiones con la entidad [DENOMINACIÓN SOCIAL], en que consta el capital acumulado al

FUNDAMENTOS DE DERECHO

I.- Conformes con la competencia objetiva y territorial del Tribunal, la legitimación de los cónyuges, y el procedimiento adecuado escogido, compareciendo esta parte con la debida representación técnica y asistencia letrada.

II.- El fondo de la pretensión actora consiste en la declaración de divorcio, a fin de la disolución del matrimonio, a instancia del marido, de conformidad con el art. 81.2.º CC, por remisión del art. 86 CC, sin necesidad de que se produzca causa legal alguna, sino por la pura voluntad del casado, siendo suficiente que uno de los cónyuges no desee la continuación del matrimonio para que pueda pretender el divorcio, y sin que mi representada pueda oponer motivos materiales a la consideración judicial, al fundarse en la voluntad de no permanecer casado, como corolario legal del derecho del art. 32 CE a contraer matrimonio.

III.- El artículo 92 CC en lo que se refiere a la custodia de los hijos, por cuanto exige adoptar las medidas más beneficiosas para ellos, y el art. 96 CC sobre la atribución del uso de la vivienda conyugal para el hijo menor de edad y su madre, así como del ajuar y mobiliario que en la misma se encuentra.

IV.- Los arts. 91, 93 y 142 y ss. CC en lo relativo a la contribución económica a favor de los hijos y, en especial, el artículo 145 CC sobre la fijación de la aportación de cada cónyuge; y el artículo 146, en cuanto a la proporción necesaria entre el caudal de quien da la pensión y las necesidades de quien los recibe.

V.- Las costas deben imponerse a la actora, de conformidad con lo dispuesto en el artículo 394 LEC.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito, con sus documentos, y copias de todo ello, se sirva admitirlo, y tenga por formulada CONTESTACIÓN A LA DEMANDA DE DIVORCIO y, tras los trámites que sean de rigor con intervención del Ministerio Fiscal, dicte Sentencia en la que se acuerde la disolución del matrimonio por divorcio de los cónyuges y la adopción de las siguientes medidas definitivas:

1.- La atribución de la guarda y custodia del hijo menor a la madre, así como el uso y disfrute del domicilio conyugal, fijándose el siguiente régimen de visitas a favor del padre [RÉGIMEN DE VISITAS] (se especificará)
2.- La fijación para el hijo menor a cargo del padre de una pensión de alimentos en cuantía de [IMPORTE] euros mensuales, pagadera por meses anticipados, mediante ingreso en la cuenta corriente [Nº DE CUENTA (IBAN)], y actualizable anualmente conforme a las variaciones que experimente el Índice de Precios al Consumo que publique el Instituto Nacional de Estadística, u organismo oficial que lo sustituya.
3.- Se proceda a liquidar la sociedad de gananciales previamente disuelta por capitulaciones matrimoniales, de forma que, con independencia de la atribución que se determine de la propiedad de los bienes se respete el uso y disfrute exclusivo de los citados al hijo y al cónyuge con el cual convive.

Todo ello con expresa imposición de costas a la parte actora.

Es de Justicia que pido en [LUGAR], a [FECHA].

========================================================================
