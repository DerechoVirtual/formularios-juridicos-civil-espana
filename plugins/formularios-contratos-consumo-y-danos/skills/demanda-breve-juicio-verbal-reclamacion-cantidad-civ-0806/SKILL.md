---
name: demanda-breve-juicio-verbal-reclamacion-cantidad-civ-0806
description: "Demanda breve de juicio verbal de reclamación de cantidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda breve de juicio verbal de reclamación de cantidad

> Formulario **CIV-0806** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda sucinta de juicio verbal en reclamación de cantidad de cuantía no superior a 2.000 euros (art. 437.2 LEC), que el propio interesado puede presentar sin abogado ni procurador, sin necesidad de fundamentos jurídicos extensos. El modelo toma como ejemplo el impago de una venta mediante recibo domiciliado devuelto. Conviene exponer también la actividad extrajudicial de reclamación previa y numerar los documentos que se acompañan.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda breve de juicio verbal de reclamación de cantidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda breve de juicio verbal de reclamación de cantidad” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-breve-juicio-verbal-reclamacion-cantidad-civ-0806`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] CALLE (3 veces)
- [ ] Nº (3 veces)
- [ ] AÑO
- [ ] DIRECCIÓN DE CORREO ELECTRÓNICO
- [ ] DOMICILIO DEL ESTABLECIMIENTO
- [ ] DÍA
- [ ] ENTIDAD
- [ ] FECHA
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] Nº DE CUENTA
- [ ] OBJETO DE LA VENTA: DESCRIPCIÓN, MARCA Y MODELO
- [ ] PROFESIÓN
- [ ] PROVINCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 437.2 LEC
- art. 155 LEC
- art. 162 LEC
- art. 252.2 LEC

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
- Junto a «….2 de la LEC. En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]. Firma del interesado/a.»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2.

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

Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDANTE], mayor de edad, de profesión [PROFESIÓN], con domicilio en la calle [CALLE], s/n, de la localidad de [LOCALIDAD], provincia de [PROVINCIA], y con establecimiento abierto al público en [DOMICILIO DEL ESTABLECIMIENTO], comparezco ante este Tribunal y DIGO:

Que formulo demanda de juicio verbal en reclamación de cantidad de [IMPORTE] euros, la cual deduzco de forma sucinta conforme a lo prevenido en el art. 437.2 LEC, al tratarse de un juicio verbal por razón de cuantía no superior a 2.000 euros, contra Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDADO], mayor de edad, con domicilio en la calle [CALLE], s/n, de [LOCALIDAD], la cual fundo en los siguientes

HECHOS

PRIMERO.- La reclamación de la cantidad que formulo se basa en que en fecha [FECHA] el demandado adquirió en mi establecimiento [OBJETO DE LA VENTA: DESCRIPCIÓN, MARCA Y MODELO], por los que debía satisfacer el precio de [IMPORTE] euros, el cual debía abonarse mediante recibo pasado al cobro dentro de los diez días siguientes a la entrega, en la cuenta corriente nº [Nº DE CUENTA] del Banco [ENTIDAD], de la que es titular el demandado, tal como se hizo constar en la hoja de pedido que se acompaña como documento nº 1.

SEGUNDO.- Pasado el recibo al cobro en los términos convenidos, resultó impagado por la entidad bancaria, tal como acredita el documento nº [Nº]. [OPCIONAL — si procede: exponer la actividad llevada a cabo por el acreedor para reclamar extrajudicialmente el pago de la cantidad adeudada.]

TERCERO.- En prueba de la reclamación acompaño los siguientes documentos: a) hoja de pedido firmada por el demandado (doc. nº 1); b) albarán de entrega (doc. nº 2); y c) recibo en cuyo dorso consta que, pasado al cobro en la fecha indicada, la entidad bancaria procedió a su devolución por haber recibido instrucciones de su cliente (doc. nº 3).

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito y demás documentos junto con las copias que se acompañan, lo admita, me tenga por personado/a en mi propio nombre y derecho y tenga por formulada demanda de juicio verbal civil en reclamación de la cantidad de [IMPORTE] euros contra el demandado Don/Doña [NOMBRE Y APELLIDOS], cuyas demás circunstancias personales constan en el encabezamiento de este escrito, y tras los trámites correspondientes dicte sentencia por la que se condene al demandado a abonar al actor la cantidad de [IMPORTE] euros más los intereses legales de demora, que al tiempo de presentar la demanda ascienden a [IMPORTE] euros, y las costas del proceso.

OTROSÍ PRIMERO DIGO: Que al amparo del art. 155 de la LEC designo como domicilio para las notificaciones el de mi establecimiento mercantil, sito en la calle [CALLE], nº [Nº], de [LOCALIDAD].

OTROSÍ SEGUNDO DIGO: Asimismo, y al amparo del art. 162 de la LEC, comunico que dispongo de [ELEGIR: correo electrónico [DIRECCIÓN DE CORREO ELECTRÓNICO] / FAX nº [Nº] / otro medio técnico] para la realización de los actos de comunicación que procedan con arreglo a la ley.

OTROSÍ TERCERO DIGO: Que fijo la cuantía del proceso en [IMPORTE] euros por aplicación del artículo 252.2 de la LEC.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del interesado/a.
