---
name: notificacion-traslado-demanda-juicio-ordinario-segun-civ-1009
description: "Notificación y traslado de demanda de juicio ordinario según el Convenio de La Haya de 1965. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Notificación y traslado de demanda de juicio ordinario según el Convenio de La Haya de 1965

> Formulario **CIV-1009** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Modelo de notificación y traslado de demanda de juicio ordinario conforme al Protocolo del Convenio de La Haya de 15 de noviembre de 1965, con tres formularios, petición, que en su dorso lleva certificación.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Notificación y traslado de demanda de juicio ordinario según el Convenio de La Haya de 1965» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Notificación y traslado de demanda de juicio ordinario según el Convenio de La Haya de 1965” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:notificacion-traslado-demanda-juicio-ordinario-segun-civ-1009`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DOCUMENTO NOTIFICADO (3 veces)
- [ ] Nº (3 veces)
- [ ] DATOS DE LA NOTIFICACIÓN (2 veces)
- [ ] CALLE
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LOCALIDAD Y PAÍS
- [ ] LUGAR
- [ ] NOMBRE DE LA CALLE (STR.)
- [ ] NOMBRE Y APELLIDOS
- [ ] NÚMERO DE LA CALLE
- [ ] SEDE

## Normas que cita el formulario

- art. 161 LEC

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

- Junto a «… SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LOS DE [LOCALIDAD]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

PETICION

A FIN DE TRASLADO O NOTIFICACION AL EXTRANJERO DE DOCUMENTO JUDICIAL O EXTRAJUDICIAL

REQUEST

FOR SERVICE ABROAD OF JUDICIAL OR EXTRAJUDICIAL DOCUMENTS

DEMANDE

AUX FINS DE SIGNIFICATION OU DE NOTIFICATION A L`ETRANGER D`UN ACTE JUDICIAIRE OU EXTRAJUDICIAIRE

Convenio relativo a la notificación o traslado en el extranjero de documentos judiciales o extrajudiciales en materia civil o comercial, firmado en La Haya el 15 de noviembre de 1965.

Convention on the service abroad of judicial and extrajudicial documents in civil or commercial matters, signed at The Hague, on the 15th of November, 1965.

Convention relative à la signification et à la notification à l`étranger des actes judiciaires ou extrajudiciaires en matière civile ou commerciale, signée à La Haya, le 15 novembre 1965.

Identidad y dirección del requirente:

Identity and address of the applicant:

Identité et adresse du requérant:

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LOS DE [LOCALIDAD]

C/, nº [Nº], (ESPAÑA).

Dirección de la autoridad destinataria:

Address of receiving authority:

Adresse de l`autoritè destinataire:

MINISTERIO DE JUSTICIA DE DINAMARCA.

El requirente infrascrito tiene el honor de remitir -en doble ejemplar- a la autoridad destinataria los documentos abajo enumerados, rogándole, conforme al artículo 5º del Convenio precitado, haga remitir sin demora un ejemplar al destinatario, a saber:

The undersigned applicant has the honour to transmit -in duplicate- the documents listed below and, in conformity with article 5 of the above mentioned Convention, requests prompt service of one copy thereof on the addresse, i. e.,

Le requérant soussigné a l`honneur de faire parvenir -en double exemplaire- à l`autorité destinataire les documents ci-dessous énumérés, en le priant, conformément à l`article 5 de la Convention précitée, d`en faire remettre sans retard un exemplaire au destinataire, à savoir:

(Identidad y dirección)

(Identity and address)

(Identité et adresse)

[NOMBRE Y APELLIDOS], CALLE [CALLE] STR. [NOMBRE DE LA CALLE (STR.)], [LOCALIDAD Y PAÍS].

Según la forma particular siguiente (artículo 5º, párrafo primero, letra b):

In accordance with the following particular method (sub-paragraph b) of the first paragraph of article 5):

Selon la forme particulière suivante (article 5, alinéa premier, lettre b):

ENTREGA DE LA CÉDULA DE EMPLAZAMIENTO Y COPIAS DE DEMANDA Y DOCUMENTOS

Se ruega a esa autoridad envíe o haga enviar al requirente un ejemplar del documento [DOCUMENTO NOTIFICADO] con la certificación que figura al dorso.

The authority is requested to return or to have returned to the applicant a copy of the documents [DOCUMENTO NOTIFICADO] with a certificate as provided on the reverse side.

Cette autorité est priée de renvoyer ou de faire renvoyer au requérant un exemplaire de l`acte [DOCUMENTO NOTIFICADO] avec l`attestation figurant au verso.

Enumeración de los documentos:

List of documents:

Enumération des pièces:

1.- CÉDULA DE EMPLAZAMIENTO.
2.- DEMANDA.
3.- DOCUMENTOS ACOMPAÑADOS ().

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Juez/a

La modalidad de entrega de documentos en el caso es de entrega de cédula de emplazamiento, conforme art. 161 LEC, aunque el Tratado de La Haya contempla, además, literalmente: Según las formas legales (artículo 5º, párrafo primero, letra a), en general, y la simple entrega al interesado, si acepta voluntariamente (artículo 5º, párrafo segundo).

B) CERTIFICACIÓN

CERTIFICATE

ATTESTATION

La autoridad infrascrita tiene el honor de certificar, conforme al artículo 6º de dicho Convenio,

The undersigned authority has the honour to certify, in conformity with article 6 of the Convention,

L`autorité soussignée a l`honneur d`attester conformément à l`article 6 de ladite Convention.

Que la petición ha sido ejecutada

(That the document has been served [DATOS DE LA NOTIFICACIÓN])

(Que la demande a été exécutée [DATOS DE LA NOTIFICACIÓN])

- El (fecha) ...

The (date)

Le (date)

- En (localidad, calle, número) ...

at (place, street, number)

à (localité, rue, numéro)

- En una de las formas siguientes previstas en el artículo quinto:

In one of the following methods authorised by article 5:

Dans une des formes suivantes prévues à l`article 5:

Según la forma particular siguiente:

In accordance with the following particular method:

Selon la forme particulière suivante:

ENTREGA DE LA CÉDULA DE EMPLAZAMIENTO Y COPIAS DE DEMANDA Y DOCUMENTOS

Los documentos mencionados en la petición han sido entregados a:

The documents referred to in the request have been delivered to:

Les documents mentionnés dans la demande ont été remis à:

(Identidad y calidad de la persona) ...

(Identity and description of person)

(Identité et qualité de la personne)

- Vínculos de parentesco, subordinación y otros, con el destinatario del documento:

Relationship to the addressee (family, business or other):

Liens de parenté, de subordination ou autres, avec le destinataire de l`acte:

Conforme al artículo 12, párrafo segundo, de dicho Convenio, se ruega al requirente el pago o reembolso de los gastos cuyo detalle figura en la declaración adjunta.

In conformity with the second paragraph of article 12 of the Convention, the applicant is requested to pay or reimburse the expenses detailed in the attached statement.

Conformément à l`article 12, alinéa 2, de la dite Convention, le requérant est prié de payer ou de rembourser les frais dont le détail figure au mémoire ci-joint.

Anexos:

Annexes:

Annexes:

Documentos reenviados:

Documents returned:

Pièces renvoyées:

En su caso, los documentos justificativos de la ejecución:

In appropriate cases, documents establishing the service:

Le cas échéant, les documents justificatifs de l`exécution:

Hecho en ..., a ... de ... de ...

Firma del Letrado de la Administración de Justicia y sello del Tribunal: ...

Advertencia

Otra de las posibilidades del certificado que expida la Autoridad requerida, obviamente, será que la petición no ha sido ejecutada en razón a los hechos que se consignen.

C) ELEMENTOS ESENCIALES DEL DOCUMENTO

IMPORTANT ELEMENTS OF THE DOCUMENT

ELEMENTS ESSENTIELS DE L`ACTE

Convenio relativo a la notificación o traslado en el extranjero de documentos judiciales o extrajudiciales en materia civil o comercial, firmado en la Haya el 15 de noviembre de 1965.

(Artículo 5º, párrafo cuarto)

Convention on the service abroad of judicial and extrajudicial documents in civil or commercial matters, signed at The Hague, on the 15th of November, 1965.

(Article 5, fourth paragraph)

Convention relative à la signification et à la notification à l`étranger des actes judiciaires ou extrajudiciaires en matière civile ou commerciale, signée à La Haya, le 15 novembre 1965.

(Article 5, alinéa 4)

Nombre y dirección de la autoridad requirente:

Name and address of the requesting authority:

Nom et adresse de l`autorité requérante:

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA Nº [Nº]. DE LOS DE ...

C/ ..., nº [NÚMERO DE LA CALLE], ... (ESPAÑA).

Identidad de las partes:

Particulars of the parties:

Identité des parties:

DEMANDANTE: CAPITAL ..., S.A.

DEMANDADA: INDUSTRIA ..., G.m.b.H.

DOCUMENTO JUDICIAL

JUDICIAL DOCUMENT

ACTE JUDICIAIRE

Naturaleza y objeto del documento:

Nature and purpose of the document:

Nature et objet de l`acte:

CÉDULA DE EMPLAZAMIENTO CON DEMANDA Y DOCUMENTOS ACOMPAÑADOS, A FIN DE QUE LA DEMANDADA INDUSTRIA ...., G.m.b.H., SE PERSONE EN AUTOS Y CONTESTE A LA DEMANDA EN EL TÉRMINO DE 20 DÍAS POR MEDIO DE ABOGADO QUE LA DEFIENDA Y PROCURADOR QUE LA REPRESENTE.

Naturaleza y objeto del procedimiento y, en su caso, cuantía del litigio:

Nature and purpose of the proceedings and, where appropriate, the amount in dispute:

Nature et objet de l`instance, les cas échéant, le montant du litige:

JUICIO ORDINARIO SOLICITANDO LA DECLARACIÓN DE RESPONSABILIDAD DEL DEMANDADO, SU OBLIGACIÓN DE INDEMNIZAR DAÑOS Y PERJUICIOS EN CANTIDAD DE ... €, E INTERESES DEVENGADOS.

Fecha y lugar para verificar la comparecencia:

Date and place for entering appearance:

Date et lieu de la ...

DENTRO DEL PLAZO DE 20 DÍAS, EN LAS ACTUACIONES

Autoridad judicial que ha dictado la resolución:

Court which has given judgment:

Juridiction qui a rendu la décision:

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA Nº [Nº]. DE LOS DE ...

Fecha de resolución:

Date of judgment:

Date de la décision:

Advertencia

Las menciones de los formularios de Petición, Certificación, y Elementos del documento, y que se han rellenado en castellano han de facilitarse traducidas al idioma del Estado requerido, lengua francesa o lengua inglesa.

El documento que se notifica o traslada, si existe reserva del Estado firmante a que se efectúe de la forma especial que establezca el Estado requirente, deberá venir traducido a la lengua o a una de las lenguas oficiales del Estado requerido.

========================================================================
