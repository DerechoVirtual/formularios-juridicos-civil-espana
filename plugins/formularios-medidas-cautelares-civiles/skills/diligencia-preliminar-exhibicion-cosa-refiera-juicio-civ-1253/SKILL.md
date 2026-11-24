---
name: diligencia-preliminar-exhibicion-cosa-refiera-juicio-civ-1253
description: "Diligencia preliminar de exhibición de la cosa a que se refiera el juicio (art. 256.1.2 LEC). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Diligencia preliminar de exhibición de la cosa a que se refiera el juicio (art. 256.1.2 LEC)

> Formulario **CIV-1253** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito solicitando la diligencia preliminar de juicio al amparo del art. 256.1.2º LEC, pidiendo la exhibición de una cosa a una persona que el solicitante pretende demandar inmediatamente en juicio.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Diligencia preliminar de exhibición de la cosa a que se refiera el juicio (art. 256.1.2 LEC)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Diligencia preliminar de exhibición de la cosa a que se refiera el juicio (art. 256.1.2 LEC)” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:diligencia-preliminar-exhibicion-cosa-refiera-juicio-civ-1253`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (19 veces)
- [ ] Nº DE DOCUMENTO (7 veces)
- [ ] FECHA (5 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DESCRIPCIÓN DEL BIEN (2 veces)
- [ ] SEDE (2 veces)
- [ ] ASEGURADORA
- [ ] CALLE
- [ ] DATOS DE LA DENUNCIA
- [ ] DOMICILIO
- [ ] LUGAR
- [ ] Nº
- [ ] NÚMERO

## Normas que cita el formulario

- art. 256.1.2 LEC
- art. 258 LEC
- art. 261.3 LEC
- art. 727.3 LEC

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
- Junto a «…te la Sección de Instrucción del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

D./Dña. [NOMBRE Y APELLIDOS], que actúa en su propio nombre y Derecho [DOMICILIO]; ante el Tribunal comparezco y como mejor procede en derecho, DIGO:

Que mediante el presente escrito deduzco solicitud de DILIGENCIA PRELIMINAR DE JUICIO al amparo del art. 256.1.2º LEC, pidiendo la exhibición de la cosa que se indicará, a D./Dña. [NOMBRE Y APELLIDOS] al proponerse mi representado demandar inmediatamente en juicio a la citada; todo ello en base a los siguientes

HECHOS

PRIMERO.- Mi representado es sobrino y heredero de D./Dña. [NOMBRE Y APELLIDOS], que ha fallecido hace quince días a la edad de noventa y cinco años, titular de un pingüe patrimonio.

Se acredita ello mediante certificado de defunción (documento nº. [Nº DE DOCUMENTO]), certificado de actos de última voluntad (documento nº [Nº DE DOCUMENTO]), y copia auténtica del testamento otorgado el fecha [FECHA], último que se conoce (documento nº [Nº DE DOCUMENTO]).

SEGUNDO.- D./Dña. [NOMBRE Y APELLIDOS], por causa de su avanzada edad, carecía de una vida autónoma en su residencia habitual de [LOCALIDAD], y pasó, por motivos complejos, hace unos cuatro meses a vivir con D./Dña. [NOMBRE Y APELLIDOS], en la vivienda de esta última en [LOCALIDAD], calle [CALLE], abonándole al parecer una renta que acordaron entre ambas, y llevando a tal vivienda algunos muebles y efectos personales entre los que se contaba una arqueta de marfil con incrustaciones de piedra de rubí de motivos religiosos, con gran antigüedad y valor, perteneciente a la familia por generaciones.

Se acompaña declaración de objeto de especial valor ante la Compañía de Seguros [ASEGURADORA], efectuada el [FECHA], para la póliza ‘multirriesgo hogar’, donde se hace constar la preexistencia de la joya (documento nº [Nº DE DOCUMENTO]).

TERCERO.- Mi mandante intentó en este tiempo entrar en contacto con [NOMBRE Y APELLIDOS], como era lo habitual hasta entonces, siéndole impedido, produciéndose un numeroso cúmulo de circunstancias, que no son del caso, y que le llevaron a sospechar que su provecta tía estaba siendo objeto de maquinaciones para que se desprendiera en favor de D./Dña. [NOMBRE Y APELLIDOS] Juana y la familia de ésta de la mayoría de sus bienes.

Adjunto copia de la denuncia presentada por mi patrocinado contra D./Dña. [NOMBRE Y APELLIDOS] y su yerno/nuera D./Dña. [NOMBRE Y APELLIDOS], ante la Sección de Instrucción del Tribunal de Instancia de [SEDE], plaza n.º [Nº] [DATOS DE LA DENUNCIA], que ha dado origen a las diligencias previas nº [NÚMERO] (documento nº [Nº DE DOCUMENTO]).

CUARTO.- El día [FECHA] padeció un accidente doméstico, siendo evacuada de urgencia al Hospital de [LOCALIDAD], donde pudo ser visitada por mi mandante, y recobrar la relación, que entonces se interrumpió con D./Dña. [NOMBRE Y APELLIDOS], habiéndose intervenido quirúrgicamente a la anciana, que se recuperó, y sin embargo, recayó al de pocas semanas, falleciendo.

QUINTO.- Desde el mismo Hospital [NOMBRE Y APELLIDOS] encomendó a mi representado reclamar la devolución de sus cosas que se hallaban en la vivienda de D./Dña. [NOMBRE Y APELLIDOS], y especialmente el camafeo antedicho, lo que éste hizo por conducto telefónico y envío de misiva formal a la dicha, sin ningún resultado.

Se aporta documento con lista manuscrita de la finada en la que constan los objetos que tenía en la casa de D./Dña. [NOMBRE Y APELLIDOS] (documento nº [Nº DE DOCUMENTO]), y el burofax enviado por mi mandante con fecha [FECHA] como documento nº [Nº DE DOCUMENTO].

FUNDAMENTOS DE DERECHO

I.- La competencia territorial ha de corresponder al órgano judicial de la instancia civil del lugar del domicilio de la interpelada D./Dña. [NOMBRE Y APELLIDOS] (art. 257.1.pfo.1º LEC)

II.- El procedimiento de admisión de la diligencia pedida es el del los arts. 258 y 259 LEC (art. 260 para la eventual oposición de la requerida), que se califica urgente, por haberse producido el fenómeno de desafeccción de D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], y la muerte de la primera, en espacio de pocas semanas, y no poderse dejar en poder de la segunda, quien se ha negado a la devolución por la tácita, ni un instante más, la cosa que se solicita de exhibición, al ser fácilmente transmisible, y evidente el riesgo de burlarse la identificación una vez descompuesta su factura en sus valiosos componentes -lo que de suyo supone un atentado al patrimonio artístico por la rareza y antigüedad-, peligrará la reivindicación, que se complicará por la presencia de terceros, receptadores o de buena fe.

III.- Conforme a la previsión del art. 261.3ª LEC, conociéndose el lugar donde se encuentra la cosa que se reivindica, si D./Dña. [NOMBRE Y APELLIDOS], citada y requerida, no atendiera al requerimiento de exhibición ni formulare oposición, el Tribunal proveerá la entrada y registro en el domicilio de la interpelada, para ocupar la arqueta en cuestión.

IV.- Tanto para el supuesto anterior como en el que se produzca la exhibición de la cosa, con fundamento en la medida cautelar del art. 727.3ª LEC, como quiera que se reivindicará, se solicita el depósito en poder de mi representado, y se ofrece caución para atender a los gastos de las diligencias y posibles daños y perjuicios irrogables, que fijará el Tribunal a la luz del fundamento de esta solicitud, de conformidad con arts. 256.3 y 258.1 LEC.

Por lo expuesto:

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito con los documentos que le acompañan, se sirva admitirlo y, teniéndome por comparecido y parte, se acuerde la práctica de diligencia preliminar de juicio para exhibición de cosa mueble; requiriéndose a D./Dña. [NOMBRE Y APELLIDOS], para que, en la fecha que se acuerde, se proceda a la exhibición de la arqueta [DESCRIPCIÓN DEL BIEN] etc [DESCRIPCIÓN DEL BIEN] en. la sede del Tribunal, a fin de que el suscrito la pueda identificar como propia, del caudal relicto de D./Dña. [NOMBRE Y APELLIDOS], con apercibimiento de acordarse la entrada y registro domiciliario si no se atendiera al requerimiento; procediendo en todo caso al depósito de la cosa, exhibida u ocupada, conforme a los trámites procesales oportunos, y por cuenta y riesgo de esta parte, que se concretará en la caución que se estime pertinente y que se ofrece prestar.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
