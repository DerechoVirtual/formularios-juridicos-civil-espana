---
name: decreto-admite-demanda-separacion-contenciosa-medidas-civ-1847
description: "Decreto que admite demanda de separación contenciosa con medidas previas de otro tribunal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Decreto que admite demanda de separación contenciosa con medidas previas de otro tribunal

> Formulario **CIV-1847** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Decreto del Letrado de la Administración de Justicia por el que se admite a trámite una demanda contenciosa de separación matrimonial, cuando previamente otro Tribunal ha adoptado medidas provisionales previas (arts. 753, 771 y 772 LEC); se da traslado al Fiscal y al demandado y se acuerda unir testimonio de las actuaciones de medidas provisionales.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Decreto que admite demanda de separación contenciosa con medidas previas de otro tribunal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Decreto que admite demanda de separación contenciosa con medidas previas de otro tribunal” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:decreto-admite-demanda-separacion-contenciosa-medidas-civ-1847`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (4 veces)
- [ ] AÑO (2 veces)
- [ ] DENOMINACIÓN DE LA SECCIÓN (2 veces)
- [ ] DÍA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (2 veces)
- [ ] SEDE (2 veces)
- [ ] DOMICILIO
- [ ] DOMICILIO PROFESIONAL
- [ ] FIRMA
- [ ] GRUPO
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE CUENTA
- [ ] NÚMERO

## Normas que cita el formulario

- art. 6 LEC
- art. 37 LEC
- art. 769.1 LEC
- art. 753 LEC
- art. 770 LEC
- art. 496.1 LEC
- art. 750 LEC
- art. 772.1 LEC

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

DECRETO DEL LETRADO/A DE LA ADMINISTRACIÓN DE JUSTICIA

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Sr./Sra. Letrado/a de la Administración de Justicia [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

PRIMERO.– Por el/la Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], según acredita con el poder que acompaña, se ha presentado demanda de separación del matrimonio, a la que adjunta [NÚMERO] documentos, frente a su cónyuge D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO]. De lo expuesto en la demanda se desprende que existe [ELEGIR: un hijo menor / hijos menores] en el matrimonio.

SEGUNDO.– Se señala en la demanda como domicilio último del matrimonio el de la localidad de [LOCALIDAD], [DOMICILIO], y se proporciona domicilio subsidiario de emplazamiento del demandado.

TERCERO.– Por la Sección [DENOMINACIÓN DE LA SECCIÓN] del Tribunal de Instancia de [SEDE] se acordaron, en auto de [DÍA] de [MES] de [AÑO], medidas provisionales previas, de revocación de poderes con anotación registral, y concesión de derechos de comunicación y estancias con el hijo común, así como la formación de inventario de cara a la liquidación del régimen económico matrimonial.

FUNDAMENTOS DE DERECHO

PRIMERO.– Examinada la anterior demanda, se estima, a la vista de los datos y documentos aportados, que la parte demandante reúne los requisitos de capacidad, representación y postulación procesales necesarios para comparecer en juicio conforme a lo determinado en los arts. 6, 7 y 750 LEC.

SEGUNDO.– Asimismo, vistas las pretensiones formuladas en la demanda y el partido al que extiende su competencia territorial este Tribunal, tiene jurisdicción y competencia objetiva para conocer de las mismas, según los arts. 37, 38 y 45 LEC, y se respeta el fuero necesario del art. 769.1 LEC.

TERCERO.– Por lo que respecta a la clase de juicio, procede, conforme a lo ordenado en el art. 753 LEC, sustanciar el proceso por los trámites del juicio verbal, pero con las especialidades previstas en el mismo precepto y las del art. 770 LEC.

CUARTO.– Por lo expuesto, procede la admisión a trámite de la demanda y, como ordena el art. 753 LEC precitado, dar traslado de la demanda al Fiscal y a D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], emplazándoles con los apercibimientos y advertencias legales, para que la contesten en el plazo de veinte días hábiles computados desde el siguiente al emplazamiento.

PARTE DISPOSITIVA

1.– Se admite a trámite la demanda de separación matrimonial presentada por el/la Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], figurando como parte demandada D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO] y el Ministerio Fiscal, sustanciándose la demanda por los trámites del juicio verbal, con las especialidades previstas en el art. 753 LEC.

2.– Dése traslado de la demanda al Fiscal y a la parte demandada D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], haciéndoles entrega de copia de la misma y de los documentos acompañados, emplazándoles para que la contesten en el plazo de veinte días hábiles, computados desde el siguiente al emplazamiento.

Apercíbase a la parte demandada que, si no comparece dentro de plazo, se le declarará en situación de rebeldía procesal (art. 496.1 LEC). Adviértasele asimismo que la comparecencia en juicio debe realizarse por medio de procurador y con asistencia de abogado (art. 750 LEC).

3.– Llévese a efecto el emplazamiento del demandado en el primer domicilio señalado por la parte actora, a través del Servicio Común de Actos de Comunicación, y si no fuera positivo, en el domicilio profesional de [DOMICILIO PROFESIONAL].

4.– De acuerdo con lo dispuesto en el art. 772.1 LEC, únase a los presentes autos testimonio de las actuaciones sobre medidas provisionales previas tramitadas en la Sección [DENOMINACIÓN DE LA SECCIÓN] del Tribunal de Instancia de [SEDE], solicitándose a tal efecto del referido Tribunal, y cuyo testimonio quedará incorporado en pieza separada.

Devuélvase el poder presentado, previo su testimonio en autos.

Contra esta resolución cabe interponer recurso de reposición, mediante escrito ante el LAJ que se presentará dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, y sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesaria la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [Nº DE CUENTA], indicando en el campo concepto del resguardo de ingreso que se trata de un «Recurso» código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Así lo acuerdo y firmo.

Firma del Letrado/a de la Administración de Justicia: [FIRMA]
