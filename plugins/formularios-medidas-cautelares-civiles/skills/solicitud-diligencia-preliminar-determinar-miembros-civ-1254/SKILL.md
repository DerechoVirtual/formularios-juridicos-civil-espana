---
name: solicitud-diligencia-preliminar-determinar-miembros-civ-1254
description: "Solicitud de diligencia preliminar para determinar los miembros de un grupo de afectados. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de diligencia preliminar para determinar los miembros de un grupo de afectados

> Formulario **CIV-1254** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito solicitando diligencia preliminar del art. 256.1.6º de la LEC., pidiendo la concreción de los integrantes del grupo de afectados por los cobros de alta, gastos administrativos de contratación y de revisión de las instalaciones interiores previa al servicio, en las pólizas para el suministro de gas natural.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de diligencia preliminar para determinar los miembros de un grupo de afectados» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de diligencia preliminar para determinar los miembros de un grupo de afectados” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-diligencia-preliminar-determinar-miembros-civ-1254`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE O DENOMINACIÓN (3 veces)
- [ ] FECHA (2 veces)
- [ ] LUGAR (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] ACTUACIÓN NO PERMITIDA
- [ ] CALLE
- [ ] COMUNIDAD AUTÓNOMA
- [ ] DENOMINACIÓN SOCIAL
- [ ] SEDE
- [ ] TIPO DE SUMINISTRO

## Normas que cita el formulario

- art. 256.1.6.º LEC
- art. 91.2 Ley 34/1998
- art. 8 Ley 7/1998
- art. 85 LOPJ
- art. 52.1.14 LEC
- art. 258 LEC
- art. 259.2 LEC
- art. 261.5.º LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de la ASOCIACIÓN DE CONSUMIDORES DE SUMINISTROS DE [TIPO DE SUMINISTRO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], dirigida por la Letrada D./Dña. [NOMBRE Y APELLIDOS], abogado ejerciente del Iltre. Colegio de [LOCALIDAD], con despacho abierto en [LOCALIDAD], calle [CALLE]; ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito solicito DILIGENCIA PRELIMINAR del art. 256.1.6.º LEC, pidiendo concreción de integrantes del grupo de afectados por los cobros de alta, gastos administrativos de contratación y de revisión de las instalaciones interiores previa al servicio, en las pólizas para el suministro de gas natural concertadas con ‘[NOMBRE O DENOMINACIÓN]’, al proponerse mi representada demandar a tal mercantil en juicio declarativo; ello en base a los siguientes

HECHOS

PRIMERO.- Mi mandante es asociación de consumidores y usuarios legalmente constituída y que tiene en sus Estatutos encomendada específicamente la defensa de los intereses de tales, y en concreto de los usuarios de suministros en el territorio de

Se aporta copia auténtica de la escritura de constitución y estatutos, con el cajetín del Registro autónomico de [COMUNIDAD AUTÓNOMA] (documento n.º [NÚMERO]).

SEGUNDO.- En sus pólizas para el suministro de gas natural de esta ciudad de [LOCALIDAD], la entidad interesada "." incluye una cláusula de atribución del pago a los particulares que contratan de los gastos administrativos derivados de la contratación, y de la revisión de las instalaciones interiores previa a la conexión del servicio, por cuyos conceptos factura cantidades diversas a los usuarios.

Se acompaña como documento n.º [NÚMERO] una serie de contratos, todos seriados, en que se constata dicha cláusula, haciendo estipulación 11.ª.

TERCERO.- La entidad interesada es la concesionaria administrativa, en virtual régimen de monopolio, del suministro de gas natural en [LUGAR], a través de su red de distribución, y carece de facultad para [ACTUACIÓN NO PERMITIDA], sin previa modificación del modelo de ‘Póliza de Abono’, según Reglamento General del Servicio Público de Combustibles aprobado por Decreto de 26 de octubre de 1973, introducir semejantes cláusulas, además para repercutir gastos referentes a actividad ya específicamente prevista en tal Reglamento, sin embargo no contemplado su cobro al usuario final en el modelo anexo.

El art. 91.2 y 3 de la Ley 34/1998 de 7 de octubre, del Sector de Hidrocarburos confirma la necesidad de la previa aprobación por la Administración para que las empresas distribuidoras del gas natural pueden dar efectividad al derecho de cobrar a los usuarios por las actividades necesarias para suministrar el gas natural.

Es así la conclusión del informe del Consejo de Estado de fecha [FECHA], y pronunciamiento de sentencias de los Tribunales de Instancia nos. de esta capital (se adjunta copia del dictamen indicado, y de tres sentencias firmes, como documentos nos. [Nº DE DOCUMENTO]).

CUARTO.- Las dichas cláusulas son condiciones generales de la contratación, que tienen como requisito de validez la aprobación por la Administración Pública competente, en términos del art. 8 de la Ley 7/1998 de 13 de abril, sobre Condiciones Generales de la Contratación (LCGC), y añadidamente, son abusivas, por no especificarse el concepto preciso que se factura, generando confusión en el adherente (arts. 82 y ss. del Texto Refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias, aprobado por Real Decreto Legislativo 1/2007, de 16 de noviembre).

QUINTO.- Mi patrocinada tiene intención de deducir acción colectiva de cesación (art. 12 LCGC), como hasta el momento ha asistido profesionalmente a los particulares que han demandado en ejercicio de acciones individuales con éxito, a la que acumulará la reclamación de que se devuelvan las cantidades que se hubieran cobrado en virtud de la condición general nula, conforme a las reglas del cobro de lo indebido.

SEXTO.- El grupo de afectados está integrado por quienes han contratado con ‘[NOMBRE O DENOMINACIÓN]’ el suministro de gas natural en el último año, según el contrato de adhesión referido, y han debido abonar lo que se les facturó por los confusos conceptos a que se ha hecho mención, cuyo número, identidad y localización se ignora.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Corresponde al órgano judicial de la instancia civil (arts. 85 LOPJ y 45 LEC) ante el que haya de presentarse la demanda que se ha anunciado, en atención al art. 257.1 párrafo 2.º LEC, que es, por la naturaleza de la acción y conforme al art. 52.1.14º LEC, el del lugar del establecimiento de la futura demandada, que coincide con el domicilio social de ‘.’

II.- PROCEDIMIENTO.-

Respecto de la admisión de la solicitud se deberá seguir el trámite de los arts. 258 y 259 LEC, y en cuanto a la práctica de la diligencia se procederá, como permite el art. 256.1.6.º, mediante requerimiento a la futura demandada para que colabore en determinar quiénes han sido los usuarios que han concertado pólizas de suministro de gas natural en el último año, y las cantidades que se les ha facturado por los conceptos de alta, gastos administrativos, o de revisión previa al servicio, citando a tal efecto ante la sede de la Oficina judicial a su representante legal, en diligencia a la que mi patrocinada acudirá asesorada por un experto en la materia, según autoriza el art. 259.2 LEC.

III.- FONDO.

Interés legítimo. El asunto objeto del pleito proyectado es la reclamación de la cesación, devolución del cobro indebido e indemnización de daños y perjuicios, junto con la publicación e inscripción en el Registro de Bienes Muebles de la condición general nula, en los términos circunstanciados. Así se legitima el interés de mi representada como futura demandante y el de ‘.’ como futura demandada.

Justa causa. Dadas las circunstancias, es notoria la precisión de reunir los datos de los afectados por la condición general de la contratación nula, y de las cifras que deben serles devueltas, así como de las eventuales características de cada quién de cara a una reparación.

Adecuación. Lógicamente, es la futura demandada la única que está en la posición de concretar a mi patrocinada la identidad y percibos de todo el conjunto de afectados, como común contratante de todos los usuarios adheridos a su modelo de contrato, y perceptora del precio que fija para el consumo.

IV.- EFECTOS.

Si la interesada requerida negara la información y no se opusiera válidamente a la diligencia, el Tribunal ordenará la intervención de la mercantil para obtenerla, o recabarla de las personas que puedan facilitarla, incluyendo la entrada y registro en las dependencias de ‘.’ en búsqueda de documentos o datos al respecto, y sin perjuicio de la responsabilidad penal por desobediencia grave a la autoridad de los responsables de la sociedad (art. 261.5.º LEC).

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan, se digne admitir uno y otros, y tenerme por comparecido y parte en la representación que ostento para que, previos los trámites legales oportunos, se acuerde la práctica, como diligencia preliminar de juicio, de la determinación por la mercantil ‘[DENOMINACIÓN SOCIAL]’ de los integrantes del grupo de usuarios afectados por los cobros de alta, gastos administrativos de contratación y de revisión de las instalaciones interiores previa al servicio, en las pólizas para el suministro de gas natural concertadas con dicha sociedad en el último año, así como la especificación de las cantidades cobradas, citándose y requiriéndose a la representación necesaria de ‘[NOMBRE O DENOMINACIÓN]’ ante la sede del Tribunal, bajo apercibimiento de que, si no comparece ni se opone, o comparece y no facilita la información cumplida, podrá incurrir en delito de desobediencia, y ser sujeta la sociedad a intervención, incluso con entrada y registro en su domicilio para obtención de los documentos o datos precisos, con lo demás que sea procedente en Derecho.

OTROSÍ PRIMERO DIGO: Para responder de los gastos, así como de los daños y perjuicios que estas diligencias puedan ocasionar al requerido, ofrezco caución suficiente mediante dinero en efectivo (o aval bancario).

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por hecha la anterior manifestación y la acepte fijando la caución que deba prestar mi representado.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
