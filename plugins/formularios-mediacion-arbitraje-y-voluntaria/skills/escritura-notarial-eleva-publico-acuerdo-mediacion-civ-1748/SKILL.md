---
name: escritura-notarial-eleva-publico-acuerdo-mediacion-civ-1748
description: "Escritura notarial que eleva a público un acuerdo de mediación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura notarial que eleva a público un acuerdo de mediación

> Formulario **CIV-1748** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura notarial que eleva a público un acuerdo de mediación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura notarial que eleva a público un acuerdo de mediación” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:escritura-notarial-eleva-publico-acuerdo-mediacion-civ-1748`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NÚMERO (4 veces)
- [ ] CALLE (3 veces)
- [ ] ESTADO CIVIL (3 veces)
- [ ] PROFESIÓN (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DÍA
- [ ] FINCA
- [ ] MES

## Normas que cita el formulario

- art. 25.1 Ley 5/2012
- art. 25 Ley 5/2012
- art. 11 Ley 5/2012
- art. 9 Ley 5/2012

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

Comparecencias

ELEVACIÓN A ESCRITURA PÚBLICA DE ACUERDO DE MEDIACIÓN

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO]

Ante mí, D. [NOMBRE Y APELLIDOS], Notario del Ilustre Colegio de [COLEGIO]

COMPARECEN:

Partes mediadas:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], de profesión [PROFESIÓN], domiciliado en [DOMICILIO], calle [CALLE], con D.N.I. número [NÚMERO]

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], de profesión [PROFESIÓN], domiciliado en [DOMICILIO], calle [CALLE], con D.N.I. número [NÚMERO]

Parte mediadora:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], de profesión [PROFESIÓN], con domicilio profesional en [LOCALIDAD], calle [CALLE], con D.N.I. número [NÚMERO], inscrita en el Registro de Mediadores de [LOCALIDAD] con número [NÚMERO] (si está presente puesto que, conforme al artículo 25.1 de la Ley 5/2012, no es preceptiva su intervención).

INTERVENCIÓN:

Todos ellos en su propio nombre y derecho. La parte mediadora a los únicos efectos de reconocer su intervención como tal en el proceso de mediación del que derivan los acuerdos que ahora se elevan a escritura pública y la autenticidad de su firma, que se legitimará, en los documentos que se protocolizan.

IDENTIFICO a los comparecientes a través de sus reseñados documentos de identidad, que me exhiben y compruebo, y tienen, a mi juicio, según intervienen, capacidad legal necesaria para otorgar la presente escritura de ELEVACIÓN A PÚBLICO DE ACUERDO ADOPTADO EN PROCESO DE MEDIACIÓN CIVIL, a cuyo fin

EXPONEN:

Primero.- Que las partes mediadas manifestaron su voluntad de someter a mediación el conflicto entre ellas existente por razón del contrato de compraventa de fecha [FECHA] concertado entre ambas partes, según consta en copia del acta de la sesión constitutiva que, a requerimiento de los mediados, se protocoliza con esta matriz, estando sometido el citado proceso de mediación a la Ley 5/2012, de 6 de julio, de mediación en asuntos civiles y mercantiles.

Segundo.- Que el objeto sometido a mediación fue la resolución del citado contrato de compraventa y posibles consecuencias indemnizatorias derivadas de que el solar vendido por D. a D. no obtuvo licencia de edificación por haberse modificado el planeamiento urbanístico del municipio en fecha

Tercero.- Que las partes mediadas sometieron la mediación a la Ley 5/2012, de 6 de julio, resultando designado mediador, por la Cámara de Comercio, Industria y Navegación de [LOCALIDAD] D. [NOMBRE Y APELLIDOS]

Cuarto.- Que tras celebrarse diferentes sesiones, los mediados llegaron a un acuerdo que consta en el Acta final del proceso de mediación, copia de la cual se protocoliza en esta matriz, y que se transcribe a continuación:

1) Ambas partes acuerdan la resolución del contrato de compraventa de fecha [FECHA] sobre la finca [FINCA], restituyéndose mutuamente sus respectivas prestaciones, quedando desde este momento el vendedor D. [NOMBRE Y APELLIDOS] en la plena propiedad y posesión de este contrato, y recibiendo el comprador D. la cantidad de [IMPORTE] euros satisfecha en concepto de precio de la compraventa.

2) Respecto de las obras realizada en la finca que fue objeto de compraventa, el vendedor D. indemnizará a D. [NOMBRE Y APELLIDOS] en la cantidad de [IMPORTE] euros, quedando totalmente satisfechas sus pretensiones y reservando en todo caso al vendedor D. el ejercicio de las acciones que pueda dirigir contra el Ayuntamiento de [LOCALIDAD] como consecuencia de los daños y perjuicios derivados del cambio de planeamiento.

3) Los gastos del proceso de mediación, así como cualquier otro derivado de la ejecución del presente acuerdo, serán de cargo exclusivamente del vendedor D. [NOMBRE Y APELLIDOS], comprometiéndose la otra parte a realizar cuantas actuaciones sean necesarias para la íntegra ejecución del presente acuerdo.

Quinto.- Conforme con lo dispuesto en los artículos 25 y siguientes de la Ley 5/2012, de 6 de julio, de mediación en asuntos civiles y mercantiles, las partes mediadas han decidido elevar a escritura pública el acuerdo objeto de mediación, lo cual llevan a efecto, con arreglo a las siguientes:

ESTIPULACIONES:

Primera.- D. y D. [NOMBRE Y APELLIDOS], conforme a lo previsto en el artículo 25 de la Ley 5/2012, de 6 de julio, acuerdan la elevación a escritura pública del acuerdo objeto de mediación transcrito en el expositivo cuarto, ratificándose en el mismo, dotándolo así de fuerza ejecutiva, de conformidad con lo dispuesto en la Ley.

Segunda.- Los gastos derivados de la presente escritura serán satisfechos por el vendedor D. [NOMBRE Y APELLIDOS]

TESTIMONIO DE LEGITIMACIÓN DE FIRMAS:

Los comparecientes reconocen como suyas las firmas que obran en los documentos protocolizados, por lo que yo, el Notario, las legitimo, fundado en el reconocimiento que antecede como medio apto para dicho fin.

REQUERIMIENTO AL MEDIADOR:

Requerido por el autorizante, manifiesta que reúne las condiciones para ejercer como mediador previstas en el artículo 11 de la Ley 5/2012, de 6 de julio, sin que, tal y como exige el artículo 13 de la misma Ley, existan circunstancias que hayan podido afectar a su imparcialidad o generar un conflicto de intereses con las personas mediadas.

ADVERTENCIAS:

Advierto a las partes mediadora y mediadas del deber de confidencialidad que pesa sobre ellas con sus excepciones, conforme al artículo 9 de la Ley 5/2012, de 6 de julio, y de la caducidad de la acción ejecutiva prevista en el Artículo 518 de la Ley de Enjuiciamiento Civil.

CONTROL DE LEGALIDAD:

Conforme a lo previsto en el artículo 25 de la Ley 5/2012, de 6 de julio, yo, el Notario, declaro cumplidos los requisitos exigidos por la citada Ley y que el contenido del acuerdo mediado no es contrario a Derecho.

DOCUMENTOS PROTOCOLIZADOS:

- Acta de iniciación del procedimiento.

- Acta de conclusión del procedimiento.

Yo, el Notario, doy fe de que el consentimiento de los otorgantes-mediados ha sido libremente prestado, de que el otorgamiento se adecua a la legalidad y a la voluntad debidamente informada de los comparecientes.

Hechas las reservas y advertencias legales, especialmente las de carácter fiscal, así lo otorgan los comparecientes mediados a quienes, a su elección, he leído y explicado esta escritura, advertidos antes de su derecho a leerla por si mismos, al que renuncian.

Yo, el Notario, de la identificación de los comparecientes por los medios supletorios indicados, de que firman a continuación y de todo lo demás consignado en este instrumento público, extendido en dos folios de papel timbrado de uso exclusivo notarial, el presente y el siguiente en orden consecutivo, doy fe.

De todo lo cual, extendido en [Nº] folios de papel timbrado del Estado, exclusivo para documentos notariales de la serie y números [Nº], yo el Notario, DOY FE.

========================================================================
