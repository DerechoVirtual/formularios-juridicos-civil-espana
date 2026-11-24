---
name: acta-vista-sobre-medidas-proteccion-alimentos-civ-2151
description: "Acta de la vista sobre medidas de protección y alimentos provisionales en reclamación de filiación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de la vista sobre medidas de protección y alimentos provisionales en reclamación de filiación

> Formulario **CIV-2151** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Acta de la vista para decidir sobre las medidas de protección y alimentos provisionales en reclamación de filiación.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de la vista sobre medidas de protección y alimentos provisionales en reclamación de filiación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de la vista sobre medidas de protección y alimentos provisionales en reclamación de filiación” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:acta-vista-sobre-medidas-proteccion-alimentos-civ-2151`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] DNI/NIE
- [ ] LUGAR
- [ ] NOMBRE DEL COLEGIO
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 767.1 LEC

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

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [NÚMERO]

PROCEDIMIENTO: Juicio de Filiación nº [Nº DE PROCEDIMIENTO]/[AÑO]

PARTES:

Número de Identificación Informático:

ACTA DE VISTA

En [LUGAR], a [FECHA].

Siendo el día señalado, y a las [Nº] horas, ante S.Sª Ilma., Magistrado-Juez de este Tribunal, D./Dña. [NOMBRE Y APELLIDOS], con mi asistencia, el LAJ, comparece la demandante Doña [NOMBRE Y APELLIDOS], asistido del Letrado/a. D./Dña. [NOMBRE Y APELLIDOS] y representado por su Procurador Sr/a.

Asimismo, comparece el demandado Don [NOMBRE Y APELLIDOS], provisto de DNI n.º [DNI/NIE], que otorga poder para pleitos ‘apud acta’ al Procurador Sr./a. [NOMBRE Y APELLIDOS], y concurriendo el/la Abogado/a D./Dña. [NOMBRE Y APELLIDOS].

Concedida la palabra a la parte actora, esta se ratifica en su escrito de demanda en lo referente a la solicitud de alimentos y de adopción de la medida cautelar de formación de inventario de los bienes del que afirma es el progenitor de su hijo, y en caso de disconformidad, solicita el recibimiento del incidente a prueba.

Concedida la palabra al demandado, se hace constar su oposición a la adopción de medidas cautelares, al no existir apariencia de buen derecho, habida cuenta que el principio de prueba que es requisito de procedibilidad se ha salvado con el anuncio de una determinada prueba testifical para el momento procesal oportuno, sin la constancia de cartas, fotografías, etc., elementos por escrito habituales de acreditación indiciaria, por lo que no hay en este momento demostración presuntiva de ningún tipo de que demandado sea el padre biológico del hijo de Doña [NOMBRE Y APELLIDOS], demandante, y así se alega la falta de legitimación pasiva ‘ad causam’ en la pretensión de este juicio. De esta manera, no sólo se sujeta a un proceso infamante sin ningún indicio a mi representado, sino que, improsperable la acción, se postula la fijación abusiva de medidas de garantía económica.

En segundo lugar, está perfectamente ausente el ‘periculum in mora’, presupuesto fundamental para la adopción de cualquier medida cautelar, y ello porque en ningún momento el demandado ha procedido a despatrimonializarse desde el conocimiento de la absurda reclamación, y además no existe dato que abone peligro justificado de que vaya a hacerlo durante la pendencia del proceso. Además, no puede asumirse una prestación de alimentos inmediata para el hijo de Doña [NOMBRE Y APELLIDOS], cuando no ha procedido a reclamar durante [Nº] años desde el nacimiento, momento durante el cual sí parece ser lo más necesario, de existir la carencia de recursos de que se habla.

Por S.S.ª se puntualiza que una falta de legitimación pasiva se refiere a la negativa a estar colocado el demandado en el polo pasivo de la relación obligatoria por parentesco alegada y, por ende, es una oposición al fondo del asunto principal, y no una excepción procesal para este incidente, haciendo saber en todo caso, que la exigencia del art. 767.1 LEC se ha llenado en el trámite de admisión de la demanda, por haberse presentado un principio de prueba determinante de la posible paternidad del demandado respecto del menor [NOMBRE DEL MENOR], mediante anuncio de medios no documentales para su momento, conforme a la doctrina de SSTS de 22 de marzo de 1999, rec. 3027/1994 y 4 de mayo de 1999, rec. 1642/1995 o ATS 18 de julio de 2000, rec. 762/1998, y estando así atribuida procesalmente el carácter de parte pasiva en el proceso principal, es dicha parte sujeto pasivo de este incidente.

Por la parte demandante se proponen los siguientes medios de prueba:

A) Documental pública:

A.1) Certificación del Ayuntamiento de [LOCALIDAD], que hace constar la inexistencia de contribuciones de ningún tipo satisfechas por Doña [NOMBRE Y APELLIDOS]

A.2) Certificación de la Agencia Tributaria de [LOCALIDAD], que hace constar la ausencia de declaración sobre impuesto de patrimonio y sobre la renta de las personas físicas por Doña [NOMBRE Y APELLIDOS]

A.3) Certificación del Instituto de Bienestar Social [LOCALIDAD], que acredita el percibo por Doña [NOMBRE Y APELLIDOS] del salario de inserción, de [IMPORTE] euros anuales, durante el ejercicio

A.4) Certificación negativa de la Tesorería General de la Seguridad Social de [LOCALIDAD], sobre falta de pensión a nombre de Doña [NOMBRE Y APELLIDOS], contributiva o no contributiva.

A.5) Certificación del Registro de la Propiedad nº [NÚMERO] de [LOCALIDAD], donde consta que el demandado ha transmitido el [FECHA] dos inmuebles de su propiedad.
B) Documental privada: Certificado del Colegio [NOMBRE DEL COLEGIO], a los efectos de constatar que el menor [NOMBRE DEL MENOR], está escolarizado, y carece de cualquier ayuda o beca.

Por la parte demandante se proponen los siguientes medios de prueba:

1) Documental pública: consistente en la aportación de certificación del Registro de la Propiedad nº [NÚMERO] de [LOCALIDAD], donde constan los bienes inmuebles, propiedad del demandado, y sobre los que pesan cargas, notoriamente muy inferiores a su valor de mercado.
2) Documental privada: consistente en el contrato de compraventa, de fecha muy anterior a la interposición de la demanda de reclamación de la filiación, por el cual se concierta la compraventa de los dos inmuebles de las fincas cuyas escrituras se otorgaron el [FECHA].

Respecto a la caución, la parte demandada solicita que en caso de adoptarse la prestación alimenticia y la medida cautelar solicitada, se condicione a la exigencia a la demandante de una caución en un importe por lo menos que ascienda a [IMPORTE] euros, a fin de prever el resarcimiento por las eventuales responsabilidades.

La parte actora reitera su solicitud de no imposición de la caución al amparo de lo establecido en el art. 768.3.pfo.3º LEC.

Se da por finalizada la vista, extendiéndose la presente acta, que es leída y hallada conforme, firmando los asistentes a la vista, después de S.S.ª, conmigo el LAJ, de lo que doy fe.

Firma del/de la Letrado/a de la Administración de Justicia

========================================================================
