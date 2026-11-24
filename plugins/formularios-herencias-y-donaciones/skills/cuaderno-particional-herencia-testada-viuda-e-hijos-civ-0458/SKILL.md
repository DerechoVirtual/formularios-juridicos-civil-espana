---
name: cuaderno-particional-herencia-testada-viuda-e-hijos-civ-0458
description: "Cuaderno particional de herencia testada con viuda e hijos y liquidación de gananciales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Cuaderno particional de herencia testada con viuda e hijos y liquidación de gananciales

> Formulario **CIV-0458** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Cuaderno particional privado de una herencia testada en la que concurren el cónyuge viudo (legatario del usufructo vitalicio) y cuatro hijos herederos, que además liquida la sociedad de gananciales. Contiene bases, inventario y avalúo, liquidación, adjudicaciones en pago de haberes y de deudas, comprobaciones y estipulaciones finales, y se protocoliza después ante notario. Adaptar el número de hijos y de bienes al caso.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Cuaderno particional de herencia testada con viuda e hijos y liquidación de gananciales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Cuaderno particional de herencia testada con viuda e hijos y liquidación de gananciales” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:cuaderno-particional-herencia-testada-viuda-e-hijos-civ-0458`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (50 veces)
- [ ] NOMBRE Y APELLIDOS (42 veces)
- [ ] LOCALIDAD (23 veces)
- [ ] Nº DE FINCA (13 veces)
- [ ] Nº (10 veces)
- [ ] PORCENTAJE (8 veces)
- [ ] PARTICIÓN (6 veces)
- [ ] DNI/NIE (5 veces)
- [ ] DOMICILIO (5 veces)
- [ ] PARTICIPACIÓN (5 veces)
- [ ] CALLE (4 veces)
- [ ] ESTADO CIVIL (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] ENTIDAD (3 veces)
- [ ] FECHA (3 veces)
- [ ] LETRA (3 veces)
- [ ] NOMBRE DEL NOTARIO (3 veces)
- [ ] Nº DE PROTOCOLO (3 veces)
- [ ] PISO (3 veces)
- [ ] SUPERFICIE (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] FOLIO (2 veces)
- [ ] IMPORTE EN LETRA (2 veces)
- [ ] LIBRO (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL CAUSANTE (2 veces)
- [ ] Nº DE PRÉSTAMO (2 veces)
- [ ] REFERENCIA CATASTRAL (2 veces)
- [ ] TOMO (2 veces)
- [ ] FECHA EN QUE SE OTORGÓ LA ESCRITURA DE OBRA NUEVA
- [ ] INDICAR SI ES VIVIENDA DE PROTECCIÓN OFICIAL
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE VIUDO
- [ ] Nº DE INSCRIPCIÓN
- [ ] SITIO
- [ ] SUCURSAL

## Normas que cita el formulario

- art. 50 Ley 13/1996

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

- Junto a «…a en las copias que se expidan, el documento relativo a la referencia catastral.»: comprobar el artículo equivalente en el texto refundido de la Ley del Catastro Inmobiliario (Real Decreto Legislativo 1/2004), que regula actualmente la obligación de consignar la referencia catastral.

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

CUADERNO PARTICIONAL DE HERENCIA TESTADA CONCURRIENDO VIUDA E HIJOS Y LIQUIDANDO EL RÉGIMEN ECONÓMICO-MATRIMONIAL DE GANANCIALES

En la ciudad de [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, viudo/a, vecino/a de [LOCALIDAD], con domicilio en la calle [DOMICILIO], y con D.N.I. número [DNI/NIE].

Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, [ESTADO CIVIL], vecino/a de [LOCALIDAD], con domicilio en la calle [DOMICILIO], y con D.N.I. número [DNI/NIE].

Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, [ESTADO CIVIL], vecino/a de [LOCALIDAD], con domicilio en la calle [DOMICILIO], y con D.N.I. número [DNI/NIE].

Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, [ESTADO CIVIL], vecino/a de [LOCALIDAD], con domicilio en la calle [DOMICILIO], y con D.N.I. número [DNI/NIE].

Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, [ESTADO CIVIL], vecino/a de [LOCALIDAD], con domicilio en la calle [DOMICILIO], y con D.N.I. número [DNI/NIE].

Reconociéndose recíprocamente la capacidad legal necesaria para la formalización del CUADERNO PARTICIONAL correspondiente a la herencia causada por el fallecimiento de Don/Doña [NOMBRE Y APELLIDOS DEL CAUSANTE], cónyuge de Don/Doña [NOMBRE Y APELLIDOS DEL CÓNYUGE VIUDO] y padre/madre de los demás comparecientes, llevan a efecto las operaciones divisorias del caudal hereditario, que articulan del siguiente modo:

BASES

Del fallecimiento del/la causante, de su estado civil y de su descendencia

Don/Doña [NOMBRE Y APELLIDOS DEL CAUSANTE] falleció en [LOCALIDAD], el día [DÍA] de [MES] de [AÑO], en estado de casado/a en primeras nupcias con Don/Doña [NOMBRE Y APELLIDOS DEL CÓNYUGE], y de cuyo matrimonio dejó para sucederle a sus cuatro citados hijos Don/Doña [NOMBRE Y APELLIDOS], Don/Doña [NOMBRE Y APELLIDOS], Don/Doña [NOMBRE Y APELLIDOS] y Don/Doña [NOMBRE Y APELLIDOS].

Del testamento del/la causante

El/La causante otorgó testamento abierto el día [FECHA], ante el Ilmo. Notario de [LOCALIDAD] Don [NOMBRE DEL NOTARIO], bajo el número [Nº DE PROTOCOLO] de su protocolo, y en el cual legó [CONTENIDO DE LOS LEGADOS: p. ej., al cónyuge viudo el usufructo vitalicio de la herencia].

El/La causante nombró Albaceas Comisarios Contadores Partidores solidarios con plenitud de facultades a Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS], pero sólo entrarían en el desempeño de tales cargos cuando lo pidiere fehacientemente algún interesado en la sucesión.

SECCIÓN PRIMERA: INVENTARIO Y AVALÚO

ACTIVO

INMUEBLES

1. FINCA URBANA EN [LOCALIDAD], REGISTRO DE LA PROPIEDAD DE [LOCALIDAD].– Parcela de terreno en término de [LOCALIDAD], sitio de [SITIO], señalada con el número [Nº] del plano parcelario, con una superficie de [SUPERFICIE] metros cuadrados. Linda: al Norte, con parcela nº [Nº]; Sur, con parcela nº [Nº]; Este, con parcela nº [Nº]; y Oeste, con calle de [CALLE].

TÍTULO.– Fue adquirida por el/la causante don/doña [NOMBRE Y APELLIDOS], para su sociedad conyugal con don/doña [NOMBRE Y APELLIDOS], en virtud de escritura de compraventa otorgada ante el Notario de [LOCALIDAD] don [NOMBRE DEL NOTARIO], en fecha [FECHA], obrante al número [Nº DE PROTOCOLO] de su protocolo.

INSCRIPCIÓN.– Figura inscrita en el Registro de la Propiedad de [LOCALIDAD], al Tomo [TOMO], Libro [LIBRO] del Ayuntamiento de [LOCALIDAD], Folio [FOLIO], Finca nº [Nº DE FINCA], inscripción [Nº DE INSCRIPCIÓN].

CARGAS.– Se encuentra libre de cargas y gravámenes.

SITUACIÓN ARRENDATICIA.– Se encuentra libre de arrendatarios.

DATOS CATASTRALES.– Figura en el Impuesto sobre Bienes Inmuebles (Urbana) con la referencia catastral [REFERENCIA CATASTRAL].

VALOR: [IMPORTE] euros.

2. FINCA URBANA EN [LOCALIDAD], REGISTRO DE LA PROPIEDAD Nº [Nº] DE [LOCALIDAD].– PISO [PISO], LETRA [LETRA] de la casa en [LOCALIDAD], calle [CALLE], nº [Nº]. Tiene una superficie construida aproximada de [SUPERFICIE] metros [NÚMERO] centímetros cuadrados, siendo la superficie útil de [SUPERFICIE] metros [NÚMERO] centímetros cuadrados.

CUOTA.– Tiene asignada una cuota de participación en los elementos comunes del inmueble de [NÚMERO] enteros [NÚMERO] centésimas por ciento.

TÍTULO.– Fue adquirida por el/la causante don/doña [NOMBRE Y APELLIDOS], en estado de casado/a con don/doña [NOMBRE Y APELLIDOS], en virtud de compra a don/doña [NOMBRE Y APELLIDOS] formalizada en escritura otorgada en fecha [FECHA] ante el Notario de [LOCALIDAD] don [NOMBRE DEL NOTARIO], nº [Nº DE PROTOCOLO] de orden de su protocolo.

INSCRIPCIÓN.– Inscrita en el Registro de la Propiedad Número [Nº] de [LOCALIDAD], Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], Finca nº [Nº DE FINCA].

ANTIGÜEDAD DE LA EDIFICACIÓN: [FECHA EN QUE SE OTORGÓ LA ESCRITURA DE OBRA NUEVA].

BENEFICIOS FISCALES: [INDICAR SI ES VIVIENDA DE PROTECCIÓN OFICIAL].

CARGAS Y GRAVÁMENES.– Se encuentra gravada con una hipoteca a favor de la entidad bancaria [ENTIDAD], en garantía de un préstamo de [IMPORTE] euros, identificado con el número [Nº DE PRÉSTAMO].

SITUACIÓN ARRENDATICIA.– Se encuentra libre de arrendatarios.

DATOS CATASTRALES.– Figura en el Impuesto sobre Bienes Inmuebles (Urbana) con la referencia catastral [REFERENCIA CATASTRAL].

VALOR: [IMPORTE] euros.

CUENTAS BANCARIAS

3. Libreta de Ahorro número [Nº] en la entidad bancaria [ENTIDAD], Sucursal [SUCURSAL] de [LOCALIDAD], cuyo saldo a la fecha de fallecimiento del/la causante era de [IMPORTE] euros.

SECCIÓN SEGUNDA: PASIVO

1. Préstamo hipotecario a favor de la entidad bancaria [ENTIDAD], identificado con el número [Nº DE PRÉSTAMO].– Cantidad pendiente a la fecha del fallecimiento del/la causante: [IMPORTE] euros.

SECCIÓN TERCERA: LIQUIDACIÓN DE LA HERENCIA

1. Importa el caudal hereditario [IMPORTE] euros.

2. Distribución del caudal.

a) Corresponde AL VIUDO/A LA VIUDA:

1. Por su mitad de gananciales, [IMPORTE] euros.

2. Por su legado en usufructo vitalicio, [IMPORTE] euros.

Total [IMPORTE] euros.

b) Remanente en la herencia, [IMPORTE] euros. Y dividido entre los cuatro hijos y herederos del causante, dará un haber para cada uno de ellos de [IMPORTE] euros.

SECCIÓN CUARTA: ADJUDICACIONES EN PAGO DE HABERES

En pago de sus respectivas cuotas, se adjudica:

1) Al viudo/viuda Don/Doña [NOMBRE Y APELLIDOS]:

a) [PARTICIÓN] partes indivisas, en pleno dominio, de la finca [Nº DE FINCA], por su valor de [IMPORTE] euros.

b) [PARTICIÓN] partes indivisas, en usufructo vitalicio, de la finca [Nº DE FINCA], por su valor de [IMPORTE] euros.

Suma el TOTAL adjudicado al viudo/a Don/Doña [NOMBRE Y APELLIDOS] [IMPORTE] euros, igual a su haber, el que con la presente adjudicación se da totalmente por pagado en cuantos derechos le correspondieran en esta partición, sin que tenga que hacer reclamación alguna.

2) Al hijo/a Don/Doña [NOMBRE Y APELLIDOS]: una [PARTICIÓN] parte indivisa, en nuda propiedad, de la finca [Nº DE FINCA], por su valor de [IMPORTE] euros.

3) Al hijo/a Don/Doña [NOMBRE Y APELLIDOS]: una [PARTICIÓN] parte indivisa, en nuda propiedad, de la finca [Nº DE FINCA], por su valor de [IMPORTE] euros.

4) Al hijo/a Don/Doña [NOMBRE Y APELLIDOS]: una [PARTICIÓN] parte indivisa, en nuda propiedad, de la finca [Nº DE FINCA], por su valor de [IMPORTE] euros.

5) Al hijo/a Don/Doña [NOMBRE Y APELLIDOS]: una [PARTICIÓN] parte indivisa, en nuda propiedad, de la finca [Nº DE FINCA], por su valor de [IMPORTE] euros.

COMPROBACIÓN DE ADJUDICACIÓN DE HABERES

Suman los bienes adjudicados a los cuatro citados herederos Don/Doña [NOMBRE Y APELLIDOS], Don/Doña [NOMBRE Y APELLIDOS], Don/Doña [NOMBRE Y APELLIDOS] y Don/Doña [NOMBRE Y APELLIDOS], [IMPORTE] euros, con lo que queda también pagada su cuota hereditaria y cuantos derechos les corresponden en la presente partición, sin que tengan que hacerse reclamación alguna entre sí, por ningún concepto.

ADJUDICACIÓN PARA PAGOS DE DEUDAS

Deuda correspondiente al/la viudo/a don/doña [NOMBRE Y APELLIDOS]

Corresponde al/la viudo/a, don/doña [NOMBRE Y APELLIDOS], por su mitad de gananciales, la mitad del préstamo pendiente de pago descrito bajo el número 1 del pasivo del inventario, Sección Segunda de este cuaderno particional, por importe de [IMPORTE] euros.

Para pago de dicha deuda se le adjudican en pleno dominio:

1. Una participación indivisa de [PARTICIPACIÓN] de la finca [Nº DE FINCA], por valor de [IMPORTE] €.

2. Metálico por importe de [IMPORTE] €.

Total [IMPORTE] €.

Deuda correspondiente al/la hijo/a y heredero/a Don/Doña [NOMBRE Y APELLIDOS]

Corresponde al/la hijo/a y heredero/a, don/doña [NOMBRE Y APELLIDOS], por herencia de su difunto/a padre/madre, el [PORCENTAJE] % del préstamo descrito bajo el número 1 del pasivo del inventario, por importe de [IMPORTE] euros.

Para pago de dicha deuda se le adjudica en pleno dominio:

1. Una participación indivisa de [PARTICIPACIÓN] de la finca [Nº DE FINCA], por valor de [IMPORTE] €.

2. Metálico por importe de [IMPORTE] €.

Total [IMPORTE] €.

Deuda correspondiente al/la hijo/a y heredero/a don/doña [NOMBRE Y APELLIDOS]

Corresponde al/la hijo/a y heredero/a, don/doña [NOMBRE Y APELLIDOS], por herencia de su difunto/a padre/madre, el [PORCENTAJE] % del préstamo descrito bajo el número 1 del pasivo del inventario, por importe de [IMPORTE] euros.

Para pago de dicha deuda se le adjudica en pleno dominio:

1. Una participación indivisa de [PARTICIPACIÓN] de la finca [Nº DE FINCA], por valor de [IMPORTE] €.

2. Metálico por importe de [IMPORTE] €.

Total [IMPORTE] €.

Deuda correspondiente al/la hijo/a y heredero/a don/doña [NOMBRE Y APELLIDOS]

Corresponde al/la hijo/a y heredero/a, don/doña [NOMBRE Y APELLIDOS], por herencia de su difunto/a padre/madre, el [PORCENTAJE] % del préstamo descrito bajo el número 1 del pasivo del inventario, por importe de [IMPORTE] euros.

Para pago de dicha deuda se le adjudica en pleno dominio:

1. Una participación indivisa de [PARTICIPACIÓN] de la finca [Nº DE FINCA], por valor de [IMPORTE] €.

2. Metálico por importe de [IMPORTE] €.

Total [IMPORTE] €.

Deuda correspondiente al/la hijo/a y heredero/a don/doña [NOMBRE Y APELLIDOS]

Corresponde al/la hijo/a y heredero/a, don/doña [NOMBRE Y APELLIDOS], por herencia de su difunto/a padre/madre, el [PORCENTAJE] % del préstamo descrito bajo el número 1 del pasivo del inventario, por importe de [IMPORTE] euros.

Para pago de dicha deuda se le adjudica en pleno dominio:

1. Una participación indivisa de [PARTICIPACIÓN] de la finca [Nº DE FINCA], por valor de [IMPORTE] €.

2. Metálico por importe de [IMPORTE] €.

Total [IMPORTE] €.

COMPROBACIÓN DE ADJUDICACIÓN PARA PAGO DE DEUDAS

Adjudicado al/la viudo/a, don/doña [NOMBRE Y APELLIDOS], para pago de la mitad de la deuda a ella correspondiente por gananciales, descrita bajo el número 1 del pasivo del inventario, la cantidad de [IMPORTE] €.

Adjudicado al/la hijo/a y heredero/a, don/doña [NOMBRE Y APELLIDOS], para pago del [PORCENTAJE] % de la deuda descrita bajo el número 1 del pasivo del inventario, la cantidad de [IMPORTE] €.

Adjudicado al/la hijo/a y heredero/a, don/doña [NOMBRE Y APELLIDOS], para pago del [PORCENTAJE] % de la deuda descrita bajo el número 1 del pasivo del inventario, la cantidad de [IMPORTE] €.

Adjudicado al/la hijo/a y heredero/a, don/doña [NOMBRE Y APELLIDOS], para pago del [PORCENTAJE] % de la deuda descrita bajo el número 1 del pasivo del inventario, la cantidad de [IMPORTE] €.

Adjudicado al/la hijo/a y heredero/a, don/doña [NOMBRE Y APELLIDOS], para pago del [PORCENTAJE] % de la deuda descrita bajo el número 1 del pasivo del inventario, la cantidad de [IMPORTE] €.

Total adjudicaciones.– [IMPORTE] €. Son [IMPORTE EN LETRA] euros. Cantidad igual al pasivo inventariado.

Por tanto:

Suma de adjudicaciones de haberes.– [IMPORTE] €.

Suma de adjudicaciones para pago de deudas.– [IMPORTE] €.

Total adjudicaciones.– [IMPORTE] €. Son [IMPORTE EN LETRA] euros. Cantidad igual al importe bruto del caudal inventariado.

ESTIPULACIONES Y MANIFESTACIONES FINALES

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— General

Comprobada la coincidencia de las adjudicaciones con el importe total del caudal hereditario, los comparecientes dan por finalizadas y aprueban las operaciones de liquidación y partición efectuadas, y acuerdan protocolizar en la Notaría de [LOCALIDAD] el presente cuaderno particional, quedando comisionado el heredero/a Don/Doña [NOMBRE Y APELLIDOS] para que tramite la correspondiente escritura y gestione, por sí o por persona que designe, las liquidaciones tributarias pertinentes, tanto en la parte que a él se adjudica como al resto de los comparecientes.

De conformidad con todo ello, firman el presente cuaderno particional en el lugar y fecha indicados.

— Detallada

PRIMERA.– Los interesados en estas operaciones particionales quedan recíprocamente obligados a la evicción y saneamiento conforme a las disposiciones legales, confiriendo la presente partición la propiedad exclusiva de los bienes que a cada uno le han sido adjudicados desde que sea protocolizada notarialmente.

SEGUNDA.– Se han inventariado, como pertenecientes a este caudal, todos los bienes, deudas y cargas de que se ha tenido conocimiento y, si aparecieren otros bienes, derechos o deudas y cargas, hoy desconocidos, serán distribuidos entre todos los herederos con arreglo a su cuota hereditaria, realizándose al efecto la oportuna escritura adicional.

TERCERA.– En cualquier caso, los intervinientes juran bajo su responsabilidad que con el causante, en la fecha de su fallecimiento, no figuraban como cotitulares en operación alguna contratada de forma indistinta que no esté comprendida en el inventario de su herencia, ni se han retirado a partir de dicho día bienes o valores depositados de cualquier forma a su nombre que no se encuentren incluidos en dicho inventario.

CUARTA.– Dado que el dinero en metálico adjudicado tanto a la viuda como a los hijos lo ha sido para pago de la deuda que grava uno de los bienes inventariados, todos ellos acuerdan en este acto dejar el referido dinero en la cuenta en que se encontraba al fallecimiento del causante y donde se encuentra al momento de firmar este cuaderno particional, cuenta en la que está domiciliado el pago de los vencimientos periódicos de tal deuda.

QUINTA.– A efectos del Impuesto sobre Sucesiones, manifiestan los intervinientes que el patrimonio preexistente de cada uno de los herederos es inferior a [IMPORTE] euros.

SEXTA.– Valor del ajuar doméstico.– Aunque no se incluye en este cuaderno particional por ser el valor de tal ajuar cero, a los efectos de fijar el valor del mismo para liquidación del Impuesto sobre Sucesiones, conforme establecen los artículos 15 de la Ley reguladora de tal Impuesto y 34 de su Reglamento, se hace constar que el valor catastral de la vivienda habitual del matrimonio al fallecimiento del/la causante, sita en la calle [CALLE], nº [Nº], piso [PISO], letra [LETRA], de [LOCALIDAD], es de [IMPORTE] euros.

SÉPTIMA.– La presente partición incluye la vivienda habitual del/la causante, sita en la calle [CALLE], nº [Nº], piso [PISO], letra [LETRA], de [LOCALIDAD], que por virtud de este documento ha sido adjudicada al/la viudo/a e hijos/as de aquél/aquélla. Lo que se manifiesta a efectos de aplicar la reducción prevista en el artículo 20.2.c) de la Ley del Impuesto sobre Sucesiones.

NOTA: es mención de obligada observancia la referencia catastral de los inmuebles, tanto en documentos públicos como en privados, en los términos previstos en los artículos 50 y siguientes de la Ley 13/1996, de 30 de diciembre, de Medidas Fiscales, Administrativas y del Orden Social. En el caso de documentos notariales, habría que hacer constar que se incorpora para su unión a la matriz, por testimonio, y su constancia en las copias que se expidan, el documento relativo a la referencia catastral.
