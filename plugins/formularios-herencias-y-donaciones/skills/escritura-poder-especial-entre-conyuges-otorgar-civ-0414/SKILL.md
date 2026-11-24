---
name: escritura-poder-especial-entre-conyuges-otorgar-civ-0414
description: "Escritura de poder especial entre cónyuges para otorgar la partición de herencia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de poder especial entre cónyuges para otorgar la partición de herencia

> Formulario **CIV-0414** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Escritura notarial por la que una persona (el poderdante, por ejemplo un cónyuge) apodera a otra para que, en su nombre, acepte o repudie una herencia, realice las operaciones de partición y otorgue las escrituras correspondientes, con facultad expresa de venta de una finca concreta.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de poder especial entre cónyuges para otorgar la partición de herencia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de poder especial entre cónyuges para otorgar la partición de herencia” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:escritura-poder-especial-entre-conyuges-otorgar-civ-0414`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] AÑO (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE FOLIOS (2 veces)
- [ ] NÚMEROS (2 veces)
- [ ] COLEGIO NOTARIAL
- [ ] FOLIO
- [ ] LIBRO
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL APODERADO
- [ ] NOMBRE Y APELLIDOS DEL CAUSANTE
- [ ] Nº DE FINCA
- [ ] Nº DE PROTOCOLO
- [ ] NÚMEROS DE ARANCEL APLICABLES
- [ ] SECCIÓN
- [ ] SERIE
- [ ] TOMO

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

NÚMERO [Nº DE PROTOCOLO]

ESCRITURA DE PODER ESPECIAL

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO].

Ante mí, [NOMBRE DEL NOTARIO], Notario del Ilustre Colegio Notarial de [COLEGIO NOTARIAL],

COMPARECE

D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en [DOMICILIO], con DNI/NIE [DNI/NIE].

INTERVIENE

En su propio nombre y derecho.

Me aseguro de su identidad por su reseñado documento nacional de identidad que me exhibe y le juzgo con capacidad legal suficiente para el otorgamiento de esta escritura.

DISPOSICIÓN

El señor compareciente otorga el poder que se deduce de los apartados siguientes:

-A- APODERADO.- D./Dª [NOMBRE Y APELLIDOS DEL APODERADO], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en [DOMICILIO], con DNI/NIE [DNI/NIE].

-B- HERENCIA A LA QUE SE REFIERE.- La de D./Dª [NOMBRE Y APELLIDOS DEL CAUSANTE], fallecido/a el [DÍA] de [MES] de [AÑO].

-C- CONTENIDO DEL PODER.-

1. ACEPTACIÓN, REPUDIACIÓN, PARTICIÓN.- Aceptar o repudiar, liquidar la sociedad conyugal y realizar todas las operaciones particionales, incluso con adjudicación de todos o alguno de los bienes a uno a calidad de abonar a los otros el exceso en dinero; nombrar peritos, tasadores y contadores-partidores; pedir el nombramiento de contador-partidor dativo y confirmar la partición que éste realizara; otorgar las correspondientes escrituras, inclusive de adición, subsanación y/o aclaración. Y, como actos preparatorios o complementarios, describir los bienes y rectificar cabidas y linderos, hacer las segregaciones, divisiones, agrupaciones, declaraciones de obra nueva y constitución o modificación del régimen de propiedad horizontal que fuesen precisas.

2. LEGADOS, USUFRUCTOS, CRÉDITOS.- Entregar y recibir legados; capitalizar usufructos, reconocer créditos en favor o en contra de la herencia, adjudicar bienes en pago o para pago de deudas y gastos.

3. TÍTULO SUCESORIO.- Instar declaraciones de herederos y obtener copias de testamentos.

4. REINTEGROS A LA MASA.- Retirar sumas y valores o efectos de la masa hereditaria que existan en bancos, incluso el de España u otros oficiales, sociedades, cajas de ahorro o de particulares; cobrar seguros.

5. IMPUESTOS.- Pedir prórrogas y liquidaciones provisionales de impuestos, reclamar contra las valoraciones y liquidaciones y percibir las cantidades cuya devolución se obtenga.

[OPCIONAL — incluir si procede]

6. VENTA.- ÚNICA Y EXCLUSIVAMENTE en relación a la de la finca registral número [Nº DE FINCA], obrante en el Registro de la Propiedad de [LOCALIDAD] al folio [FOLIO], tomo [TOMO], libro [LIBRO] de la Sección [SECCIÓN], que es [DESCRIPCIÓN DE LA FINCA: tipo de inmueble, edificio, calle y número].

Venderla, cederla, en general enajenar, fijando libremente el precio y condiciones, a las personas físicas o jurídicas que tenga por conveniente, por el plazo y condiciones que libremente podrá determinar; en caso de aplazamiento, aceptar las garantías que juzgue pertinentes, incluso la de condición resolutoria que podrá cancelar y, en su día, cobrar el precio y cancelar las garantías. Todo ello de la forma más amplia y sin ninguna limitación, firmando cuantos documentos públicos y privados fueren menester, y facultándole asimismo para solicitar y retirar copias de esta escritura.

-D- AUTOCONTRATACIÓN.- Se otorga este poder aunque el apoderado tenga o represente intereses iguales u opuestos en la herencia.

PROTECCIÓN DE DATOS

Respecto a los datos personales recogidos en el presente documento, debe tenerse en cuenta que el tratamiento de los mismos se ajustará a la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, en desarrollo y aplicación del Reglamento (UE) 2016/679, de 27 de abril, y que el interesado podrá ejercitar sus derechos de acceso, rectificación, supresión (derecho al olvido), portabilidad, oposición y limitación del tratamiento de los datos en los términos establecidos en los artículos 12 a 23 del citado Reglamento y en los artículos 12 a 18 de la citada Ley Orgánica, respectivamente.

OTORGAMIENTO Y AUTORIZACIÓN

Así lo dice y otorga a mi presencia.

Leo la presente escritura al compareciente, por su elección, tras advertirle del derecho que le asiste a leerla por sí. Enterado y habiendo quedado debidamente informado del contenido de este instrumento público, por la lectura y mis explicaciones verbales, se ratifica en su contenido y lo firma conmigo, el Notario.

Y yo, el Notario, DOY FE:

a) De haber identificado al compareciente por medio de su documento identificativo, reseñado en la comparecencia, que me ha sido exhibido.

b) De que el compareciente, a mi juicio, tiene capacidad y está legitimado para el presente otorgamiento.

c) De que el consentimiento de los otorgantes ha sido libremente prestado.

d) De que el otorgamiento se adecua a la legalidad y a la voluntad libre y debidamente informada de los comparecientes.

e) Y de todo cuanto antecede en este instrumento público, extendido en [Nº DE FOLIOS] folios de papel timbrado notarial de serie [SERIE], números [NÚMEROS] y los [Nº] siguientes.

SIGUE LA FIRMA DEL COMPARECIENTE.- SIGNADO, RUBRICADO Y FIRMADO POR MÍ. ESTÁ EL SELLO DE MI NOTARÍA.

APLICACIÓN ARANCEL, DISPOSICIÓN ADICIONAL 3.ª LEY 8/1989

BASES DE CÁLCULO: Sin cuantía.

ARANCEL APLICABLE: [NÚMEROS DE ARANCEL APLICABLES]

DERECHOS ARANCELARIOS sin IVA: [IMPORTE] euros. Cuota IVA: [IMPORTE] euros. Total factura: [IMPORTE] euros.

ES PRIMERA COPIA LITERAL de su matriz con la que concuerda fielmente y donde queda anotada. La expido a instancias del PODERDANTE en [Nº DE FOLIOS] folios de papel exclusivo para documentos notariales, números [NÚMEROS] y los [Nº] siguientes, el mismo día de su autorización. DOY FE.
