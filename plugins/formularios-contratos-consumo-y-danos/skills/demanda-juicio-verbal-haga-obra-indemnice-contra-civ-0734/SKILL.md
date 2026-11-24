---
name: demanda-juicio-verbal-haga-obra-indemnice-contra-civ-0734
description: "Demanda de juicio verbal para que se haga una obra y se indemnice, contra fontanero y aseguradora. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal para que se haga una obra y se indemnice, contra fontanero y aseguradora

> Formulario **CIV-0734** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda sucinta al Tribunal de Instancia sobre reclamación de hacer y de daños y perjuicios contra el fontanero y la compañía aseguradora por no haber el primero reparado la fuga de agua para lo que se le contrató verbalmente, lo que ocasionó filtraciones en el piso inmediato inferior quien sufrió daños por cuantía inferior a 2.000 euros.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal para que se haga una obra y se indemnice, contra fontanero y aseguradora» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal para que se haga una obra y se indemnice, contra fontanero y aseguradora” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-verbal-haga-obra-indemnice-contra-civ-0734`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] IMPORTE (5 veces)
- [ ] ASEGURADORA (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] DIRECCIÓN (3 veces)
- [ ] CALLE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] DENOMINACIÓN DEL EDIFICIO
- [ ] DNI/NIE
- [ ] IMPORTE EN CIFRA
- [ ] LUGAR
- [ ] Nº
- [ ] PISO
- [ ] PROFESIÓN

## Normas que cita el formulario

- art. 304 LEC
- art. 329 LEC
- art. 437.1 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA Q.P.T.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Se indicarán todos los domicilios del deudor que se conozcan, y si no, el del lugar donde pueda ser hallado a efectos del requerimiento.

[NOTA DE REVISIÓN: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).]


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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA Q.P.T.C.

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, casado, provisto con DNI [DNI/NIE], de profesión [PROFESIÓN], y domiciliado en esta localidad (código postal), calle [CALLE], n.º [NÚMERO], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito vengo a formular DEMANDA DE JUICIO VERBAL en reclamación por cantidad contra D./Dña. [NOMBRE Y APELLIDOS] domiciliado en [DOMICILIO], c./ [DIRECCIÓN] n.º [NÚMERO], y contra la compañía anónima de seguros [ASEGURADORA], domiciliada en [DOMICILIO] c./ [DIRECCIÓN] n.º [NÚMERO], con base en los siguientes:

Que soy dueño de la vivienda sita en el piso [PISO] de [DENOMINACIÓN DEL EDIFICIO], calle [CALLE] (si fuera negado de contrario, se designan los libros del Registro de la Propiedad de [LOCALIDAD]) habiendo contratado verbalmente con el demandado D./Dña. [NOMBRE Y APELLIDOS], la reparación de la fuga de agua del plato de ducha de uno de los servicios de la vivienda.

Que D./Dña. [NOMBRE Y APELLIDOS], que ejecutó su labor la mañana del día [FECHA], no sólo no ha procedido a reparar la avería a mi satisfacción, cobrando por el trabajo ejecutado la cantidad de [IMPORTE] euros, sino que, consecuencia de su malhacer se han producido filtraciones en el piso inmediato inferior, propiedad de D./Dña. [NOMBRE Y APELLIDOS], quien ha sufrido daños por cuantía de [IMPORTE] euros que le he tenido que abonar.

Que el demandado se ha negado a volver a ejecutar debidamente la reparación, y a compensarme por el perjuicio de haber tenido que resarcir a la vecina D./Dña. [NOMBRE Y APELLIDOS], siendo infructuosas las gestiones realizadas amistosamente para conseguirlo, así como con quien manifiesta ser aseguradora de la responsabilidad profesional [ASEGURADORA].

En virtud de lo anteriormente expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con sus copias, se digne admitir uno y otras, y en mérito a lo alegado, seguido que sea todo el pertinente procedimiento, se venga a dictar en su día definitiva Sentencia que condene a D./Dña. [NOMBRE Y APELLIDOS] a la ejecución de la adecuada reparación de la fuga de agua del plato de la ducha del servicio de la vivienda del actor, sita en [LOCALIDAD], c./ [DIRECCIÓN], n.º [NÚMERO], por el precio alzado de [IMPORTE], así como condene a D./Dña. [NOMBRE Y APELLIDOS], conjunta y solidariamente con la compañía de seguros anónima [ASEGURADORA] a indemnizar al actor en la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), con todo lo demás que sea procedente en Justicia de hacerse en [LUGAR], a [FECHA].

OTROSI PRIMERO DIGO: Que interesa al derecho de esta parte valerse para el acto de la vista de los siguientes medios de PRUEBA

I.- INTERROGATORIO DE LA PARTE CONTRARIA, en las personas de D./Dña. [NOMBRE Y APELLIDOS] y del representante legal la demandada compañía de seguros [ASEGURADORA], quienes deberán ser citado con los apercibimientos legales de tener por admitidos los hechos del interrogatorio en caso de injustificada incomparecencia, conforme al art. 304 LEC.

II.- DOCUMENTAL, consistente en que se requiera a la demandada compañía de seguros para que aporte al acto de la vista la póliza de seguro de responsabilidad civil profesional contratada con D./Dña. [NOMBRE Y APELLIDOS], bajo apercibimientos de las consecuencias previstas en el art. 329 LEC

III.- TESTIFICAL, que se articulará oportunamente.

OTROSÍ SEGUNDO DIGO: Que la cuantía de la obra que ha de ejecutar el demandado D./Dña. [NOMBRE Y APELLIDOS], asciende a la cantidad de [IMPORTE], conforme al precio pactado y abonado.

Por lo expuesto,

SUPLICO AL TRIBUNAL que, teniendo por causadas las anteriores manifestaciones, se sirva ordenar lo legalmente oportuno y admitir la prueba propuesta por anticipado, ordenando todo lo conducente a su recta y rápida práctica.

Reitero Justicia en lugar y fecha arriba indicados.

OTROSÍ TERCERO DIGO: Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II en relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

En virtud de lo expuesto,

AL TRIBUNAL NUEVAMENTE SUPLICO que, teniendo por hecha la afirmación anterior, se admita y provea en consecuencia.

Firma del Abogado/a	Firma del Procurador/a
