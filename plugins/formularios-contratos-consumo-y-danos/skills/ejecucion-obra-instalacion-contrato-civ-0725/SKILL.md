---
name: ejecucion-obra-instalacion-contrato-civ-0725
description: "Ejecución de obra o instalación (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Ejecución de obra o instalación (contrato)

> Formulario **CIV-0725** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Ejecución de obra o instalación (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Ejecución de obra o instalación (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:ejecucion-obra-instalacion-contrato-civ-0725`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE DE LA PARTE (14 veces)
- [ ] DENOMINACIÓN SOCIAL (11 veces)
- [ ] NÚMERO (8 veces)
- [ ] CALLE (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] OTROS DATOS (4 veces)
- [ ] PISO (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº (3 veces)
- [ ] CARGO (2 veces)
- [ ] DESCRIBIR (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] ACTIVIDAD
- [ ] LUGAR
- [ ] Nº DE CUENTA (IBAN)

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS:

De una parte, D [NOMBRE Y APELLIDOS], mayor de edad, provisto de D.N.I. y N. I. F. número [NÚMERO], domiciliado en Calle [CALLE], número [NÚMERO], piso [PISO], de [LOCALIDAD], que interviene en nombre y representación de la sociedad [DENOMINACIÓN SOCIAL], como [CARGO] de dicha sociedad, provista de C.I.F. número [NÚMERO] y domiciliada en Calle [CALLE], número [NÚMERO], piso [PISO] de

y de otra parte, D [NOMBRE Y APELLIDOS], mayor de edad, provisto de D.N.I. y N. I. F. número [NÚMERO], domiciliado en Calle [CALLE], número [NÚMERO], piso [PISO], de [LOCALIDAD], que interviene en nombre y representación de la sociedad [DENOMINACIÓN SOCIAL] como [CARGO] de dicha sociedad, provista de C.I.F. número [NÚMERO] y domiciliada en Calle [CALLE], número [NÚMERO], piso [PISO], de

Ambas partes se reconocen capacidad suficiente, que prometen no impugnar, para contratar y para obligarse mediante la firma de este documento y, de común acuerdo,

EXPONEN

La empresa [DENOMINACIÓN SOCIAL] dedicada a [ACTIVIDAD], está interesada en la ejecución de una obra/realización de una instalación consistente en [DESCRIBIR]

La empresa [DENOMINACIÓN SOCIAL] dispone de los medios personales y técnicos necesarios para llevar a cabo la obra/instalación mencionada en el ordinal anterior.

Estando la sociedad [DENOMINACIÓN SOCIAL] interesada en que se realice en su establecimiento la obra/instalación expresada y la empresa [DENOMINACIÓN SOCIAL] en hacerse cargo de su ejecución material, suscriben el presente contrato, que se regirá por la legislación general aplicable y por las siguientes

ESTIPULACIONES

La sociedad [DENOMINACIÓN SOCIAL] se compromete a ejecutar la obra/realizar la instalación consistente en [DESCRIBIR] Se adjunta al presente contrato, firmado por las partes, Anexo señalado con nº I, en el que se detallan los pormenores de la obra/instalación, y las calidades de los materiales que han de de aplicarse a la ejecución.

El plazo para la ejecución de la obra/instalación será de [Nº] meses, a partir de la firma de este contrato, en que la empresa [DENOMINACIÓN SOCIAL] pone a disposición de [DENOMINACIÓN SOCIAL] el local donde debe realizarse la intervención, manifestando esta última encontrarse en disposición de dar inmediato comienzo a las obras. En consecuencia, la obra/instalación deberá quedar íntegramente finalizada el día [DÍA] de [MES] de [AÑO], debiendo poner [NOMBRE DE LA PARTE] en dicha fecha, el local/la instalación a disposición de [NOMBRE DE LA PARTE] en condiciones de perfecto e inmediato uso para el ejercicio de la actividad a que se destina.

El precio convenido por la ejecución de la obra/instalación es de [IMPORTE] euros, que se pagarán de la siguiente manera:

-A la firma de este contrato, la firma [NOMBRE DE LA PARTE] entrega a [NOMBRE DE LA PARTE] la suma de [IMPORTE] euros en concepto de anticipo y a cuenta del precio total, sirviendo la firma de este contrato como la más eficaz carta de pago [OTROS DATOS].

-Con fecha [DÍA] de [MES] de [AÑO], [NOMBRE DE LA PARTE] realizará una transferencia bancaria a la cuenta corriente [Nº DE CUENTA (IBAN)] de la titularidad de [NOMBRE DE LA PARTE] por importe de [IMPORTE] euros.

La empresa [NOMBRE DE LA PARTE] se obliga a realizar por sí misma el contenido total del objeto de su prestación [OTROS DATOS]

El incumplimiento de las condiciones de este contrato dará lugar al siguiente cuadro de responsabilidades:

Si la mercantil [DENOMINACIÓN SOCIAL] no cumple su compromiso de tener finalizada la obra/instalación en el plazo previsto, [NOMBRE DE LA PARTE] podrá optar por solicitar la resolución del contrato o por exigir a [NOMBRE DE LA PARTE] una penalización por retraso de [IMPORTE] euros por cada día en que se demore la entrega de la obra/instalación, en perfecto estado de uso/funcionamiento, viniendo [NOMBRE DE LA PARTE] obligada al pago de tal indemnización

Si [NOMBRE DE LA PARTE] no cumple la obligación de realizar los pagos previstos, [NOMBRE DE LA PARTE] podrá optar entre la resolución del contrato, en cuyo caso quedarán en su favor las sumas entregadas hasta la fecha y podrá exigir el precio de la parte de obra/instalación ejecutada más los perjuicios ocasionados, o exigir el íntegro cumplimiento del mismo.

Si cualesquiera de las partes incumplen las restantes obligaciones que para cada una de ellas se derivan de la firma de este contrato, la parte que haya cumplido sus obligaciones podrá optar por exigir el íntegro complimiento o solicitar su resolución, en ambos casos con reclamación de los daños y perjuicios generados

A todos los efectos de aplicación de intereses moratorios se aplicará lo dispuesto en la estipulación séptima.

Se establece un plazo de garantía de [Nº] años para la obra/instalación que ha de ejecutarse, durante el cual [NOMBRE DE LA PARTE] garantizará el correcto acabado de la obra/funcionamiento de la instalación [OTROS DATOS] Si la obra/instalación presentase defectos imputables a su ejecución que [OTROS DATOS], [NOMBRE DE LA PARTE] podrá optar entre

Las partes manifiestan, y mutuamente reconocen, su condición de comerciantes, y que la contratación guarda relación con la actividad mercantil de ambos contratantes. En consecuencia, resultarán de aplicación a la interpretación y aplicación de este concreto las normas que regulan la contratación mercantil, y en particular, las del Código de Comercio y la Ley 3/2004 por la que se establecen medidas de lucha contra la morosidad en las operaciones comerciales.

Controversias y arbitraje

Para dirimir cualquier cuestión sobre interpretación o aplicación de este contrato las partes se someten, con renuncia a cualquier fuero especial que pudiera corresponderles, a los juzgados y tribunales de la ciudad de

Y en prueba de conformidad con cuantas manifestaciones y estipulaciones se contienen en el presente documento que consta de [Nº] hojas por una sola cara, las partes lo firman en todas dichas hojas, por duplicado ejemplar y a un solo efecto, en el lugar y fecha de su encabezamiento.

Fdº: Por Fdº: Por [DENOMINACIÓN SOCIAL]
Administrador Único	Administrador Único

ANEXO I:

Características de la obra y calidades de materiales:

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fdº: Por Fdº: D [NOMBRE Y APELLIDOS]
Administrador Único	Agente comercial
