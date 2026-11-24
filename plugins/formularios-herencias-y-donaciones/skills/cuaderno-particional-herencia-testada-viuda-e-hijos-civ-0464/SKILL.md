---
name: cuaderno-particional-herencia-testada-viuda-e-hijos-civ-0464
description: "Cuaderno particional de herencia testada con viuda e hijos, gananciales y conmutación de usufructo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Cuaderno particional de herencia testada con viuda e hijos, gananciales y conmutación de usufructo

> Formulario **CIV-0464** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Cuaderno particional de herencia testada con viuda e hijos, gananciales y conmutación de usufructo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Cuaderno particional de herencia testada con viuda e hijos, gananciales y conmutación de usufructo” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:cuaderno-particional-herencia-testada-viuda-e-hijos-civ-0464`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (15 veces)
- [ ] LOCALIDAD (14 veces)
- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] NÚMERO (13 veces)
- [ ] PORCENTAJE (7 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] FOLIO (2 veces)
- [ ] LIBRO (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DE LA CALLE (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL NOTARIO (2 veces)
- [ ] PARAJE (SITIO) (2 veces)
- [ ] REFERENCIA CATASTRAL (2 veces)
- [ ] TOMO (2 veces)
- [ ] FECHA
- [ ] NOMBRE DE LA SUCURSAL
- [ ] NOMBRE DEL NOTARIO

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

CUADERNO PARTICIONAL DE HERENCIA TESTADA CONCURRIENDO VIUDA E HIJOS Y LIQUIDANDO EL RÉGIMEN ECONÓMICO-MATRIMONIAL DE GANANCIALES Y CONMUTACIÓN DEL USUFRUCTO VIUDAL

En la ciudad de [LOCALIDAD] a [DÍA] de [MES] de [AÑO]

BASES

Del fallecimiento del/la causante, de su estado civil y de su descendencia

Don/Doña [NOMBRE Y APELLIDOS] falleció en [LOCALIDAD] el día [DÍA] de [MES] de [AÑO] en estado de casado/a en primeras nupcias con Don/Doña [NOMBRE Y APELLIDOS] y de cuyo matrimonio dejó para sucederle a sus cuatro citados hijos Don/Doña [NOMBRE Y APELLIDOS] Don/Doña [NOMBRE Y APELLIDOS] Don/Doña [NOMBRE Y APELLIDOS] y Don/Doña [NOMBRE Y APELLIDOS]

Del testamento del/la causante

El/La causante otorgó testamento abierto el día [FECHA] ante el Ilmo. Notario de [LOCALIDAD] Don [NOMBRE DEL NOTARIO] bajo el número [NÚMERO] de su protocolo, y en el cual legó

El/La causante nombró Albaceas Comisarios Contadores Partidores solidarios con plenitud de facultades a Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS] pero sólo entrarían en el desempeño de tales cargos cuando lo pidiere fehacientemente algún interesado en la sucesión.

INVENTARIO Y AVALÚO

Activo

INMUEBLES

1. FINCA URBANA EN [LOCALIDAD] REGISTRO DE LA PROPIEDAD DE [LOCALIDAD] Parcela de terreno en término de V sitio de [PARAJE (SITIO)] señalada con el número [NÚMERO] del plano parcelario, con una superficie de V metros cuadrados.

Linda: al Norte, con parcela nº [NÚMERO] Sur, con parcela nºV Este, con parcela nº [NÚMERO] y Oeste, con calle de [NOMBRE DE LA CALLE]

TÍTULO.- Fue adquirida por el/la causante don/doña [NOMBRE Y APELLIDOS] para su sociedad conyugal con don/doñaV en virtud de escritura de compraventa otorgada ante el Notario de [LOCALIDAD] don [NOMBRE Y APELLIDOS DEL NOTARIO] en fecha V obrante al número [NÚMERO] de su protocolo.

INSCRIPCIÓN.- Figura inscrita en el Registro de la Propiedad de [LOCALIDAD] al Tomo [TOMO] Libro [LIBRO] del Ayuntamiento de [LOCALIDAD] Folio [FOLIO] Finca nº [NÚMERO] inscripción

CARGAS.- Se encuentra libre de cargas y gravámenes.

SITUACIÓN ARRENDATICIA.- Se encuentra libre de arrendatarios.

DATOS CATASTRALES.- Figura en el Impuesto sobre Bienes Inmuebles (Urbana) con la referencia catastral [REFERENCIA CATASTRAL]

VALOR [IMPORTE]: euros.

2. FINCA URBANA EN [LOCALIDAD] REGISTRO DE LA PROPIEDAD DE [LOCALIDAD] Parcela de terreno en término de V sitio de [PARAJE (SITIO)] señalada con el número [NÚMERO] del plano parcelario, con una superficie de V metros cuadrados.

Linda: al Norte, con parcela nº [NÚMERO] Sur, con parcela nºV Este, con parcela nº [NÚMERO] y Oeste, con calle de [NOMBRE DE LA CALLE]

TÍTULO.- Fue adquirida por el/la causante don/doña [NOMBRE Y APELLIDOS] para su sociedad conyugal con don/doñaV en virtud de escritura de compraventa otorgada ante el Notario de [LOCALIDAD] don [NOMBRE Y APELLIDOS DEL NOTARIO] en fecha V obrante al número [NÚMERO] de su protocolo.

INSCRIPCIÓN.- Figura inscrita en el Registro de la Propiedad de [LOCALIDAD] al Tomo [TOMO] Libro [LIBRO] del Ayuntamiento de [LOCALIDAD] Folio [FOLIO] Finca nº [NÚMERO] inscripción

CARGAS.- Se encuentra libre de cargas y gravámenes.

SITUACIÓN ARRENDATICIA.- Se encuentra libre de arrendatarios.

DATOS CATASTRALES.- Figura en el Impuesto sobre Bienes Inmuebles (Urbana) con la referencia catastral [REFERENCIA CATASTRAL]

VALOR [IMPORTE]: euros.

CUENTAS BANCARIAS

3. Libreta de Ahorro número [NÚMERO] en la entidad bancaria [ENTIDAD BANCARIA] Sucursal [NOMBRE DE LA SUCURSAL] de [LOCALIDAD] cuyo saldo a la fecha de fallecimiento del/la causante era deV euros.

Pasivo

1. Préstamo hipotecario a favor de la entidad bancaria [ENTIDAD BANCARIA] identificado con el número [NÚMERO] Cantidad pendiente a la fecha del fallecimiento del/la causante de [IMPORTE] euros.

[ELEGIR UNA OPCIÓN: Liquidación de la herencia / Conmutación mediante adjudicación de bienes / Conmutación mediante asignación de renta vitalicia / Conmutación mediante pago en metálico / — y además elegir: Adjudicación en pago de haberes / ADJUDICACIONES EN PAGO DE HABERES / Conmutación mediante adjudicación de bienes / Conmutación mediante asignación de renta vitalicia / Conmutación mediante pago en metálico]

ADJUDICACIÓN PARA PAGOS DE DEUDAS

Deuda correspondiente al/la viudo/a don/doña...

Corresponde al/la viudo/a, don/doña [NOMBRE Y APELLIDOS] por su mitad de gananciales, la mitad del préstamo pendiente de pago descrito bajo el número 1 del pasivo del inventario, Sección Primera de este cuaderno particional, por importe [IMPORTE] euros.

Para pago de dicha deuda se le adjudican en pleno dominio:

1. Una participación indivisa de [PORCENTAJE] de la finca por valor de [IMPORTE] €

2. Metálico por importe de [IMPORTE] €

Total €

Deuda correspondiente al/la hijo/a y heredero/a don/doña...

Corresponde al/la hijo/a y heredero/a, don/doña [NOMBRE Y APELLIDOS]

Por herencia de su difunto/a padre/madre, el [PORCENTAJE] % del préstamo descrito bajo el número 1 del pasivo del inventario, por importe de [IMPORTE] euros.

Para pago de dicha deuda se le adjudica en pleno dominio:

1. Una participación indivisa de [PORCENTAJE] de la finca por valor de [IMPORTE] €

2. Metálico por importe de [IMPORTE] €

Total €

Deuda correspondiente al/la hijo/a y heredero/a don/doña...

Corresponde al/la hijo/a y heredero/a, don/doña [NOMBRE Y APELLIDOS]

Por herencia de su difunto/a padre/madre, el [PORCENTAJE] % del préstamo descrito bajo el número 1 del pasivo del inventario, por importe de [IMPORTE] euros.

Para pago de dicha deuda se le adjudica en pleno dominio:

1. Una participación indivisa de [PORCENTAJE] de la finca por valor de [IMPORTE] €

2. Metálico por importe de [IMPORTE] €

Total €

Deuda correspondiente al/la hijo/a y heredero/a don/doña..

Corresponde al/la hijo/a y heredero/a, don/doña [NOMBRE Y APELLIDOS]

Por herencia de su difunto/a padre/madre, el [PORCENTAJE] % del préstamo descrito bajo el número 1 del pasivo del inventario, por importe de [IMPORTE] euros.

Para pago de dicha deuda se le adjudica en pleno dominio:

1. Una participación indivisa de [PORCENTAJE] de la finca por valor de [IMPORTE] €

2. Metálico por importe de [IMPORTE] €

Total €

[ELEGIR UNA OPCIÓN: Comprobación de adjudicacióin para pago de deudas / COMPROBACIÓN DE ADJUDICACIÓN PARA PAGOS DE DEUDAS / General / Detallada]

Mención de obligada observancia, tanto en documentos públicos como en privados, en los términos previstos en los artículos 50 y siguientes de la Ley 13/1996, de 30 de diciembre, de Medidas Fiscales, Administrativas y del orden social.

En el caso de documentos notariales, habría que hacer constar que se incorpora para su unión a la matriz, por testimonio, y su constancia en las copias que se expidan, el documento relativo a la referencia catastral; Véanse artículos 50 y 51 de la Ley 13/1996

========================================================================
