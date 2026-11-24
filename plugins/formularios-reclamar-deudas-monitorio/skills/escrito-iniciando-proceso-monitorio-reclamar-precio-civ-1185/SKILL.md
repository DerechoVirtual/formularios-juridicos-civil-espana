---
name: escrito-iniciando-proceso-monitorio-reclamar-precio-civ-1185
description: "Escrito iniciando proceso monitorio para reclamar el precio de la reparación de un automóvil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito iniciando proceso monitorio para reclamar el precio de la reparación de un automóvil

> Formulario **CIV-1185** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Escrito promoviendo proceso monitorio reclamando una cantidad debida como consecuencia de la reparación de un automóvil (contrato de arrendamiento de obra).

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito iniciando proceso monitorio para reclamar el precio de la reparación de un automóvil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito iniciando proceso monitorio para reclamar el precio de la reparación de un automóvil” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:escrito-iniciando-proceso-monitorio-reclamar-precio-civ-1185`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NÚMERO (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] CALLE (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] DOMICILIO
- [ ] ENTIDAD BANCARIA
- [ ] FECHAS
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MARCA/MODELO
- [ ] MATRÍCULA
- [ ] NIF
- [ ] NOMBRE COMERCIAL

## Normas que cita el formulario

- art. 812.1.1.ª LEC
- art. 813 LEC
- art. 85.1 LOPJ
- art. 812 LEC
- art. 5 Ley Orgánica 1/2025
- art. 812.1 LEC
- art. 576 LEC

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

Notas al pie del formulario original:
(1) Está previsto en el art. 814.1, párrafo segundo LEC, que estén a disposición de las partes impresos o formularios para hacer la solicitud inicial.

========================================================================


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

D./Dña. [NOMBRE Y APELLIDOS] con D.N.I [DNI/NIE] mayor de edad, de estado [ESTADO CIVIL], de profesión [PROFESIÓN] y domiciliado en [DOMICILIO], ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que insto proceso monitorio contra D./Dña. [NOMBRE Y APELLIDOS], con D.N.I [DNI/NIE] mayor de edad, de estado [ESTADO CIVIL], de profesión [PROFESIÓN] y con domicilio en [LOCALIDAD] calle [CALLE], en reclamación de la cantidad de [IMPORTE] euros, y al amparo de lo prevenido en el art. 812.1.1.ª LEC.

Se basa esta pretensión en lo siguiente:

HECHOS

Que soy titular del negocio de reparación de automóviles sito en esta ciudad, calle [CALLE] que gira con el nombre comercial [NOMBRE COMERCIAL], con N.I.F [NIF]; en dicho negocio se efectuó la reparación de un automóvil marca [MARCA/MODELO] matrícula [MATRÍCULA] que había traído su propietario, el demandado; aquél presentaba diversos desperfectos en chapa y parte delantera con afectación de diversos elementos de su mecánica; todo ello fue evaluado en el oportuno presupuesto, que aceptó y firmó el demandado según se acredita con el DOC. N.º [NÚMERO], de fecha

En la fecha prevista se culminó la reparación del vehículo, devengando una factura total por mano de obra, accesorios, repuestos etc, según se detalló, por importe total de [IMPORTE] euros, que fue entregada al propietario demandado al recoger el vehículo en el taller. Para su pago hizo entrega de un talón contra su cuenta en el Banco [ENTIDAD BANCARIA], que fue ingresado para su abono, resultando impagado, por lo que el Banco lo devolvió. Se acompañan: DOC. N.º [NÚMERO], copia de la factura final, DOC. N.º [NÚMERO], talón impagado firmado por el deudor, y DOC. N.º [NÚMERO], carta de devolución bancaria.

La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA:

Corresponde al Tribunal de Instancia al que tengo el honor de dirigirme, por ser el del domicilio del deudor (art. 813 LEC, en relación con lo dispuesto en el art. 85.1º LOPJ)

II.- PROCEDIMIENTO:

Corresponde el regulado en los arts. 812 y siguientes LEC.

III.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD:

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IV.- MATERIALES O DE FONDO:

Se trata de cantidad determinada, vencida y exigible (art. 812.1 LEC), ya que debió ser abonada en el momento de la recogida del vehículo ya reparado; se apoya la pretensión en el cumplimiento de los requisitos formales (art. 812.1.1.ª LEC) consistentes en el presupuesto y factura de la reparación, el primero firmado por el deudor; y en el talón firmado por el mismo e impagado, que implícitamente reconoce la existencia de la deuda.

Por lo expuesto,

SUPLICO AL TRIBUNAL:

Que teniendo por presentado este escrito, lo admita y tenga por promovido proceso monitorio, acordando dar traslado con requerimiento de pago al deudor, y en caso de desatención del mismo y previa petición de parte, se dicte Auto por el que se despache ejecución, por la cantidad de [IMPORTE] euros, si el demandado no se opusiere o no consignare la deuda; y continuándose luego el trámite señalado para la ejecución de las sentencias, haciéndose el completo y cumplido pago al que suscribe de la cantidad reclamada por principal, más los intereses del art. 576 LEC, con las costas a que, en su caso, se diere lugar.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma del peticionario/a
