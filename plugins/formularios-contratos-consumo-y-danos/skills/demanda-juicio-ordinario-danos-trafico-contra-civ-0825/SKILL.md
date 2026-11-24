---
name: demanda-juicio-ordinario-danos-trafico-contra-civ-0825
description: "Demanda de juicio ordinario por daños de tráfico contra conductor, propietario y aseguradora. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario por daños de tráfico contra conductor, propietario y aseguradora

> Formulario **CIV-0825** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en reclamación de indemnización por daños en las personas y en los bienes derivados de la circulación de vehículos de motor, interpuesta por el conductor y por el propietario del vehículo perjudicado frente al otro conductor, el propietario de su vehículo y la aseguradora (acción directa del art. 76 LCS), con reclamación de intereses del art. 20 LCS.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario por daños de tráfico contra conductor, propietario y aseguradora» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario por daños de tráfico contra conductor, propietario y aseguradora” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-danos-trafico-contra-civ-0825`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- `formulario.md`: el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `marco.md`: la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (16 veces)
- [ ] Nº (15 veces)
- [ ] Nº DE DOCUMENTO (14 veces)
- [ ] NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDANTE (12 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO (10 veces)
- [ ] AÑO (8 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDADO (7 veces)
- [ ] DÍA (6 veces)
- [ ] MES (6 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA ASEGURADORA (5 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO CAUSANTE (5 veces)
- [ ] CALLE Y NÚMERO (4 veces)
- [ ] MARCA Y MODELO (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº/AÑO (3 veces)
- [ ] MATRÍCULA (2 veces)
- [ ] SEDE (2 veces)
- [ ] CONCESIONARIO
- [ ] CUERPO POLICIAL QUE INSTRUYÓ EL ATESTADO
- [ ] DENOMINACIÓN
- [ ] DIRECCIÓN
- [ ] FECHA
- [ ] FECHAS
- [ ] MARCA
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRES
- [ ] Nº DE INSCRIPCIÓN
- [ ] Nº DE PÓLIZA
- [ ] PORCENTAJE
- [ ] PUNTO KILOMÉTRICO
- [ ] TIPO DE VEHÍCULO
- [ ] VÍA

## Normas que cita el formulario

- art. 85 LOPJ
- art. 52.1.9.º LEC
- art. 6.1.1.º LEC
- art. 7.1 LEC
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 10 LEC
- art. 76 Ley 50/1980
- art. 253.1 LEC
- art. 251 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.089 Código Civil
- art. 1.902 Código Civil
- art. 1.903 Código Civil
- art. 76 LCS
- art. 1.100 Código Civil
- art. 20.4.ª LCS
- art. 394.1 LEC

---

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

- Junto a «…amente contra el conductor y el propietario del vehículo causante del accidente.»: el apartado VIII.2 (cuantificación de las lesiones) sigue la estructura del antiguo baremo de la Ley 30/1995 (tablas III, IV, V y VI). Para accidentes ocurridos desde el 1 de enero de 2016 debe adaptarse al sistema de valoración vigente tras la Ley 35/2015 (texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor, RDLeg 8/2004: comprobar los artículos y tablas aplicables, así como la numeración actual de los preceptos citados sobre intereses de demora y oferta motivada).
- Junto a «…mora y oferta motivada).] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE USO: Si la cuantía de la demanda supera los 15.000 euros se sigue el cauce del juicio ordinario y si es inferior el del juicio verbal. Presentada la demanda se examinará por el Letrado de la Administración de Justicia, que dictará decreto admitiéndola a trámite y dando traslado a los demandados para que contesten en veinte días. No obstante, el LAJ dará cuenta al Tribunal para que resuelva por auto sobre la admisión cuando estime falta de jurisdicción o competencia o que la demanda adolece de defectos formales y no se hubiesen subsanado por el actor en el plazo que se le concediera. La reclamación de cuantía superior a 2.000 euros requiere la intervención de Abogado y Procurador. Los documentos a los que tenga acceso el actor y, en su caso, el informe pericial, deben presentarse con la demanda. Es imprescindible que en el informe pericial se recojan los requisitos incluidos en el artículo 335.2 de la LEC.

La Ley de Contrato de Seguro regula la reclamación de intereses de la siguiente manera. Se entiende que el asegurador incurre en mora cuando no hubiere cumplido su prestación en el plazo de tres meses desde la producción del siniestro o no hubiere procedido al pago del importe mínimo de lo que pueda deber dentro de los cuarenta días a partir de la recepción de la declaración del siniestro. La indemnización por mora se impondrá de oficio por el juzgador y consistirá en el pago de un interés anual igual al del interés legal del dinero vigente en el momento en que se devengue incrementado en el 50 por 100. Transcurridos dos años desde la producción del siniestro el interés anual no podrá ser inferior al 20 por 100. Hay que tener en cuenta que la STS, Sala Primera, 251/2007, de 1 de marzo, ha interpretado este polémico precepto sentando la doctrina jurisprudencial de que el interés de demora debe calcularse durante los dos primeros años siguientes al siniestro al tipo legal más el 50%, y a partir de ese momento, al tipo del 20%, si aquél no resulta superior. El término inicial del cómputo de los intereses es la fecha del siniestro y el final, en los casos de falta de pago del importe mínimo de lo que el asegurador pueda deber, el día en que comiencen a devengarse intereses por el importe total de la indemnización, salvo que con anterioridad sea pagado por el asegurador el importe mínimo, en cuyo caso será término final la fecha de este pago. Será término final del plazo de la obligación de abono de intereses de demora por la aseguradora en los restantes supuestos el día en que efectivamente satisfaga la indemnización mediante pago, reparación o reposición al asegurado, beneficiario o perjudicado. No habrá lugar a la indemnización por mora del asegurador si la falta de satisfacción de la indemnización o pago del importe mínimo está fundada en una causa justificada o que no le fuere imputable.

La Ley 18/2011, de 5 de julio, regula el expediente judicial electrónico, el documento judicial electrónico, las copias y archivos de documentos electrónicos y el registro electrónico. La Ley 35/2015 modificó el texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor dando una nueva redacción al artículo 7. Tras su entrada en vigor se exige con carácter previo a la interposición de la demanda que se dirija reclamación extrajudicial a la aseguradora, suponiendo la no aportación de los documentos que acrediten la presentación de la reclamación al asegurador y la oferta o respuesta motivada, si se hubiere emitido por el asegurador, causa de inadmisión de la demanda. Este requisito se aplica a los accidentes acaecidos con posterioridad al 1 de enero de 2016, fecha de entrada en vigor de la reforma, como vienen declarando varias Audiencias, de las que a título de ejemplo se cita el Auto de la AP de Madrid, Sección 9.ª, n.º 199/2017. Sin embargo, no está claro que este requisito previo sea exigible cuando la demanda en reclamación de daños materiales se dirija acumuladamente contra el conductor y el propietario del vehículo causante del accidente.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee `formulario.md` entero y la parte de `marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
