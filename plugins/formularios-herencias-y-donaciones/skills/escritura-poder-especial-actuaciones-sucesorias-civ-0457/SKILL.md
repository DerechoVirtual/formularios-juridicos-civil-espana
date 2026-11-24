---
name: escritura-poder-especial-actuaciones-sucesorias-civ-0457
description: "Escritura de poder especial para actuaciones sucesorias. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de poder especial para actuaciones sucesorias

> Formulario **CIV-0457** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Escritura notarial de poder especial en materia sucesoria, con dos modalidades de facultades (muy amplias o reducidas a una herencia concreta), por la que una persona autoriza a otra a aceptar o repudiar herencias, hacer particiones, cobrar y vender bienes hereditarios. Contiene la previsión de que el poder siga vigente aunque la poderdante precise medidas de apoyo.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de poder especial para actuaciones sucesorias» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de poder especial para actuaciones sucesorias” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:escritura-poder-especial-actuaciones-sucesorias-civ-0457`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (4 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] CLASE
- [ ] COLEGIO NOTARIAL
- [ ] DÍA
- [ ] ESTADO CIVIL
- [ ] FECHA
- [ ] MES
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL CAUSANTE
- [ ] Nº DE PROTOCOLO
- [ ] NÚMERO
- [ ] NÚMEROS
- [ ] PARENTESCO
- [ ] PARENTESCO O AFINIDAD
- [ ] SERIE

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

- Junto a «…tamiento, de su seguridad y confidencialidad el Notario titular de esta notaría.»: el original citaba la Orden del Ministerio de Justicia 484/2003 y la LO 15/1999 (derogada); sustituido por RGPD y LOPDGDD; comprobar la cláusula de protección de datos vigente que utilice la notaría.

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

PODER ESPECIAL EN MATERIA SUCESORIA

NÚMERO [Nº DE PROTOCOLO]

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO]

Ante mí, [NOMBRE DEL NOTARIO], Notario del Ilustre Colegio Notarial de [COLEGIO NOTARIAL],

COMPARECE

Doña [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], de profesión [PROFESIÓN], vecina de [LOCALIDAD], con domicilio en calle [DOMICILIO], y con D.N.I. número [DNI/NIE].

La identifico por su D.N.I., que tengo a la vista.

Interviene en su propio nombre y derecho.

Tiene, a mi juicio, la compareciente la capacidad legal necesaria para otorgar la presente escritura de APODERAMIENTO, y

DICE Y OTORGA

Que confiere poder especial tan amplio y bastante como en Derecho se requiera a favor de [PARENTESCO O AFINIDAD], Doña [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], vecina de [LOCALIDAD], domiciliada en [DOMICILIO], calle [CALLE], titular del D.N.I. número [DNI/NIE], para que en nombre y representación de la compareciente (y aunque al hacerlo incurra en la figura jurídica de la autocontratación u oposición de intereses, o tenga intereses contrapuestos o ejercite una múltiple representación), pueda realizar los actos siguientes con plenitud de competencias, atribuciones y facultades, y con libertad para fijar pactos, cláusulas, disposiciones, determinaciones y declaraciones, de suerte que la apoderada ostente la plena representación de la poderdante sin traba, limitación ni excepción alguna.

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— FACULTADES MUY AMPLIAS

I.- Aceptar, con o sin beneficio de inventario, las herencias testadas o intestadas en que tenga interés la poderdante. Repudiar y manifestar herencias; hacer, aprobar o impugnar particiones de herencias y liquidaciones de sociedad conyugal, incluso de comunicaciones forales; entregar y recibir legados; aceptar, liquidar y extinguir fideicomisos; pagar, cobrar, fijar, garantizar y depositar legítimas y cancelar o renunciar a sus garantías legales; hacer y aceptar donaciones. Dividir bienes comunes.

— FACULTADES REDUCIDAS

I.- Aceptar, con o sin beneficio de inventario, las herencias testadas o intestadas en que tenga interés la poderdante y, de un modo especial, la de [PARENTESCO] Doña [NOMBRE Y APELLIDOS DEL CAUSANTE], fallecida en [LOCALIDAD] el día [FECHA]; solicitar, en su caso, declaraciones de herederos, copias de testamentos, aprobar inventario y avalúo, liquidación, división y adjudicación de bienes hereditarios, practicar cuanto proceda hasta la terminación de las operaciones particionales e inscripción de las mismas en el Registro de la Propiedad correspondiente.

Cobrar cuantas cantidades resulten a percibir con respecto de dicha herencia, de cualquier persona, ya sea física o jurídica.

Vender lo adjudicado a la persona o personas con quien a bien tenga concertar la operación, por el precio, pactos y condiciones que libremente estipule, pudiendo cobrar dicho precio al contado, a plazos o anticipadamente y, en caso de aplazamiento, aceptar las garantías oportunas, incluso hipotecaria, condición resolutoria que cancelará en su día, previo cobro de la cantidad aplazada.

Y a tales efectos otorgar y firmar las escrituras públicas o documentos privados que fueren necesarios o convenientes.

II.- Solicitar y obtener copias del presente apoderamiento.

Manifiesta expresamente la poderdante que desea que este apoderamiento conserve su vigencia hasta su fallecimiento (salvo que expresamente hubiere sido revocado por ella), y desea expresamente que conserve dicha vigencia aunque, por razón de discapacidad, se establecieran judicialmente medidas de apoyo para el ejercicio de su capacidad jurídica, se le nombrara curador, defensor judicial o cualquier otro tipo de apoyo para su persona y bienes (Ley 8/2021, de 2 de junio).

AUTORIZACIÓN

Reservas y advertencias legales

Así lo dice y otorga, según interviene, a quien hago las reservas y advertencias legales pertinentes y, a efectos fiscales, las relativas a las obligaciones y responsabilidades que le incumben en su aspecto material, formal y sancionador, y a las consecuencias que se derivarían de la inexactitud de sus declaraciones.

Se informa a la compareciente de que sus datos personales serán tratados por el Notario conforme al Reglamento (UE) 2016/679 (RGPD) y a la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, con la finalidad de facilitar la tramitación y seguimiento de esta escritura, conservándose con carácter confidencial y reservado y sin perjuicio de las comunicaciones autorizadas por la ley. Es responsable del tratamiento, de su seguridad y confidencialidad el Notario titular de esta notaría.

Lectura

Permito a la compareciente la lectura de esta escritura, porque así lo solicita después de advertida de la opción del artículo 193 del Reglamento Notarial.

Consentimiento

Enterada, según dice, por la lectura que ha practicado y por mis explicaciones verbales, la compareciente hace constar libremente su consentimiento al contenido de la escritura.

Firma

Y la firma.

Autorización

Yo, el Notario, compruebo que este otorgamiento se adecua a la legalidad y a la voluntad debidamente informada y expresada ante mí; y con el contenido de esta escritura, extiendo en [NÚMERO] folios de papel timbrado notarial de la clase [CLASE], serie [SERIE], números [NÚMEROS]. DOY FE.
