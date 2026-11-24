---
name: oferta-motivada-aseguradora-perjudicado-sin-civ-0745
description: "Oferta motivada de la aseguradora al perjudicado sin reclamación previa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oferta motivada de la aseguradora al perjudicado sin reclamación previa

> Formulario **CIV-0745** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oferta motivada de la aseguradora al perjudicado sin reclamación previa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oferta motivada de la aseguradora al perjudicado sin reclamación previa” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:oferta-motivada-aseguradora-perjudicado-sin-civ-0745`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (17 veces)
- [ ] AÑO (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] ASEGURADORA (2 veces)
- [ ] DÍA (2 veces)
- [ ] MARCA/MODELO (2 veces)
- [ ] MATRÍCULA (2 veces)
- [ ] MES (2 veces)
- [ ] MOTIVO (2 veces)
- [ ] DIRECCIÓN
- [ ] DNI/NIE
- [ ] DOCUMENTOS ACREDITATIVOS
- [ ] FECHA
- [ ] LUGAR
- [ ] OTROS DATOS

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

Compañía de Seguros [ASEGURADORA]

A la atención de:

D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Referencia: siniestro nº [DNI/NIE]

Muy Sr. Mío:

Habiendo tenido conocimiento el día [DÍA] de [MES] de [AÑO] por [OTROS DATOS] del accidente en el que Ud. resultó perjudicado, ocurrido el día [FECHA] en [DIRECCIÓN] y en el que se vio involucrado el vehículo modelo [MARCA/MODELO], matrícula [MATRÍCULA] asegurado en esta Compañía, procedemos a realizarle la siguiente OFERTA DE INDEMNIZACIÓN por los perjuicios sufridos:

— Por los daños en el vehículo modelo [MARCA/MODELO], matrícula [MATRÍCULA], la cantidad de [IMPORTE] euros, en atención [MOTIVO]. Esta cantidad se ha calculado teniendo en cuenta la siguiente documentación [DOCUMENTOS ACREDITATIVOS], cuya copia se une a esta propuesta.

— Por las lesiones padecidas, en aplicación del anexo de la Ley de responsabilidad civil y seguro en la circulación de vehículos a motor y del baremo del año [AÑO]

. TABLA 3: INDEMNIZACIONES POR LESIONES TEMPORALES:

Perjuicio Personal Básico: [IMPORTE] euros

Perjuicio Personal Particular: [IMPORTE] euros

Perjuicio Patrimonial: [IMPORTE] euros

. TABLA 2.A.1: Indemnización del perjuicio personal básico: [IMPORTE] euros

. TABLA 2.A.2: Baremo económico: [IMPORTE] euros

. TABLA 2.B: Perjuicio personal particular: [IMPORTE] Euros

. TABLA 2.C: Indemnizaciones por secuelas: [IMPORTE] euros

. TABLA 2.C.2: Horas diarias de necesidad de ayuda de tercera persona: [IMPORTE] euros.

. TABLA 2.C.3: Indemnizaciones de ayuda de tercera persona: [IMPORTE] euros

. TABLA 2.C.4: Lucro cesante por incapacidad para realizar cualquier trabajo o actividad profesional (absoluta): [IMPORTE] euros.

. TABLA 2.C.5: Lucro cesante por incapacidad para realizar su trabajo o actividad profesional (total): [IMPORTE] euros

. TABLA 2.C.6: Lucro cesante por incapacidad que de origen a una disminución parcial de ingresos en el ejercicio de su trabajo o actividad habitual (parcial): [IMPORTE] euros.

. TABLA 2.C.7: Lucro cesante por incapacidad absoluta de lesionados pendientes de acceder al mercado laboral: [IMPORTE] euros.

. TABLA 2.C.8: Lucro cesante por incapacidad total de lesionados pendientes de acceder al mercado laboral: [IMPORTE] euros.

— Por los gastos médicos y sanitarios, la cantidad de [IMPORTE] euros en atención a [MOTIVO]

El valor total de la oferta de indemnización asciende a [IMPORTE] euros, que serán abonados al momento de la aceptación por la parte reclamante.

Se hace constar expresamente que la aceptación y efectivo pago de la cantidad antedicha supone la renuncia de D./Dña. [NOMBRE Y APELLIDOS] a todas las acciones que respecto a D./Dña. [NOMBRE Y APELLIDOS] y a la Compañía de Seguros [ASEGURADORA] pudieran corresponderle por el siniestro de referencia, salvo que se acreditara que la indemnización sea inferior a la que en derecho pueda corresponderle.

[ELEGIR UNA OPCIÓN: Previa aceptación y de forma simultánea a la firma del finiquito / Consignación en la cuenta del Tribunal]

A la espera de sus noticias, reciba un saludo:

========================================================================
