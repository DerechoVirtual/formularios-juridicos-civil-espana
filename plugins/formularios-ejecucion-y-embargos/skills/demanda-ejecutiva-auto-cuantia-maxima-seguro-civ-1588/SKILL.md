---
name: demanda-ejecutiva-auto-cuantia-maxima-seguro-civ-1588
description: "Demanda ejecutiva de auto de cuantía máxima por seguro obligatorio, con bienes a embargar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva de auto de cuantía máxima por seguro obligatorio, con bienes a embargar

> Formulario **CIV-1588** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda ejecutiva de título judicial (art. 517.2.8.º LEC) contra la aseguradora para reclamar las cantidades fijadas en el auto de cuantía máxima dictado en un proceso penal por hechos de la circulación cubiertos por el seguro obligatorio de responsabilidad civil de vehículos a motor, con otrosí designando bienes a embargar.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva de auto de cuantía máxima por seguro obligatorio, con bienes a embargar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva de auto de cuantía máxima por seguro obligatorio, con bienes a embargar” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-auto-cuantia-maxima-seguro-civ-1588`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (4 veces)
- [ ] SEDE (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] MES (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA ASEGURADORA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL CONDUCTOR (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL EJECUTANTE (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CONCEPTO INDEMNIZATORIO
- [ ] DENOMINACIÓN DE LA ENTIDAD
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] DOMICILIO PROFESIONAL
- [ ] HORA
- [ ] MARCA
- [ ] MATRÍCULA
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] Nº DE CUENTA
- [ ] Nº DE PÓLIZA
- [ ] PROPIETARIO
- [ ] RELACIÓN DE SECUELAS
- [ ] TALLER
- [ ] VÍA

## Normas que cita el formulario

- art. 517.2.8.º LEC
- art. 5 LEC
- art. 76 Ley 50/1980
- art. 576 LEC
- art. 553 LEC

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
- Junto a «…CHO I Arts. 45 y 52.1.9.º LEC, en orden a la competencia objetiva y territorial.»: comprobar la atribución competencial vigente tras la LO 1/2025 (Tribunal de Instancia).

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTANTE], conforme acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº DE DOCUMENTO], ante la Sección Civil del Tribunal de Instancia de [SEDE], a la que en su caso corresponda por turno de reparto, ante la misma comparezco, bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [LOCALIDAD], con despacho abierto en [DOMICILIO PROFESIONAL], y como mejor proceda en Derecho, DIGO:

Que, siguiendo expresas instrucciones de mi mandante, vengo a ejercitar la acción prevista en el art. 517.2.8.º LEC, formulando demanda ejecutiva de título judicial de auto de cuantía máxima contra la mercantil [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], con domicilio en [DOMICILIO], en reclamación de la cantidad que se expresa en el suplico, lo que baso en los siguientes

HECHOS

PRIMERO.– El pasado día [DÍA] de [MES] de [AÑO], sobre las [HORA] horas, circulaba mi poderdante conduciendo [VEHÍCULO DEL EJECUTANTE: clase, marca y modelo], de su propiedad, por [VÍA], en dirección a [DIRECCIÓN].

[DESCRIPCIÓN DEL ACCIDENTE: maniobra realizada por el ejecutante, circunstancias de la colisión y conducta del conductor del vehículo asegurado. Ejemplo del modelo original: al efectuar un cambio de dirección a su derecha, el ejecutante señalizó la maniobra y fue alcanzado por el vehículo asegurado, cuyo conductor, al acceder a la carretera desde un punto muy próximo y a gran velocidad, no se percató de su presencia, colisionando contra él.]

El vehículo causante del siniestro, marca [MARCA], matrícula [MATRÍCULA], propiedad de [PROPIETARIO] y conducido por D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR], se encontraba asegurado en la fecha de ocurrencia de los hechos en la entidad aseguradora demandada, con póliza número [Nº DE PÓLIZA].

SEGUNDO.– Como consecuencia de los hechos relatados, mi poderdante resultó con lesiones de las que tardó en curar [NÚMERO] días, estando impedido [NÚMERO] días y quedándole como secuelas las siguientes: [RELACIÓN DE SECUELAS].

De conformidad con lo establecido en el auto que se ejecuta y en el baremo del texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor, aprobado por Real Decreto Legislativo 8/2004, las citadas lesiones se valoran en los siguientes importes:

Concepto | Importe
[CONCEPTO INDEMNIZATORIO] | [IMPORTE]

Así aparecen reflejadas tanto en el informe de sanidad facilitado por el Médico Forense como en la sentencia dictada en los autos de juicio por delito leve n.º [Nº DE PROCEDIMIENTO] de la Sección de Instrucción del Tribunal de Instancia de [SEDE], autos que acompañamos por testimonio (documentos números [Nº] y [Nº]), designando, si de adverso se impugnaran, los archivos del Tribunal mencionados, para traer en su día los testimonios que fuesen precisos.

Igualmente, el vehículo conducido por mi poderdante sufrió daños por importe de [IMPORTE] euros, según factura de [TALLER], unida a los autos de juicio por delito leve citados, y no impugnada (documento número [Nº DE DOCUMENTO]).

TERCERO.– En los indicados autos de juicio por delito leve n.º [Nº DE PROCEDIMIENTO], de la Sección de Instrucción del Tribunal de Instancia de [SEDE], recayó sentencia absolutoria para D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR], lo que motivó, a su vez, el dictado del título cuya ejecución se solicita (documento número [Nº DE DOCUMENTO]).

FUNDAMENTOS DE DERECHO

I

Arts. 45 y 52.1.9.º LEC, en orden a la competencia objetiva y territorial.

II

Arts. 6 y 7 LEC, en orden a la capacidad para ser parte y la capacidad procesal; arts. 5, 10 y 538 LEC, art. 7 del texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor (RDLeg 8/2004) y art. 76 de la Ley 50/1980, de Contrato de Seguro, en orden a la legitimación de las partes.

III

Arts. 23, 31 y 539.1 LEC, en cuanto a la postulación o necesidad de intervención de Letrado y de Procurador/a.

IV

Arts. 549 y siguientes LEC, en orden al procedimiento ejecutivo.

V

En cuanto al fondo del asunto, los arts. 1 y 7 del texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor, así como el art. 517.2.8.º LEC.

VI

Son de aplicación los intereses de mora especiales del asegurador de los arts. 20 de la Ley de Contrato de Seguro y 9 del texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor, y los legales procesales, en su caso, del art. 576 LEC.

VII

Arts. 539 y 583 LEC, en orden a la imposición de costas a la parte ejecutada.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, con los poderes y documentos que se acompañan y copia de todo ello, se sirva admitir uno y otros, y tener por interpuesta demanda ejecutiva de auto de cuantía máxima en nombre de D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTANTE] contra la mercantil [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], por la cantidad de [IMPORTE] euros de principal, más [IMPORTE] euros que provisionalmente y sin perjuicio de ulterior liquidación se presupuestan para intereses, costas y gastos del procedimiento ejecutivo, se sirva admitirla y dictar auto despachando ejecución por las cantidades reclamadas, cuyo auto servirá de mandamiento al Personal de Auxilio de la Administración de Justicia para que, asistido del/de la Oficial de Justicia habilitado/a del Servicio Común de Actos de Comunicación y Ejecución, y sin necesidad de requerimiento previo de pago a la entidad demandada, proceda al embargo de bienes de la misma, en cantidad bastante para cubrir las cantidades reclamadas, con notificación del auto despachando ejecución a la parte ejecutada, siguiendo el juicio por todos sus trámites y con celebración de vista y, en su día, dictar definitiva resolución por la que se declare procedente la ejecución y se mande seguir adelante por todos sus trámites hasta hacer trance y remate en los bienes embargados a la demandada, y con su producto cumplido pago a mi poderdante de cuanto se reclama por principal, intereses y costas, pues así procede y es de hacer en justicia, que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

OTROSÍ DIGO: Que, de conformidad con lo establecido en los arts. 553, 589 y 590 LEC, señalo como bienes a embargar los saldos en cuentas bancarias titularidad de la ejecutada en la entidad bancaria [DENOMINACIÓN DE LA ENTIDAD], con el número [Nº DE CUENTA].

Y desconociendo si la precitada cuenta dispone de saldo suficiente, intereso se requiera a la ejecutada para que manifieste relacionadamente bienes y derechos de su titularidad suficientes para cubrir la ejecución, bajo los apercibimientos legales.

SUPLICO AL TRIBUNAL que, teniendo por causadas las manifestaciones antecedentes a los efectos oportunos, sirva acordar lo pertinente a su respecto, por ser de hacer igualmente en justicia, que reitero en lugar y fecha ut supra.

Por ser de Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
